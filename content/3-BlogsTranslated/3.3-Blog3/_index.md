---
title: "Blog 3"
date: "2025-10-10"
weight: 1
chapter: false
pre: " <b> 3.3. </b> "
---

# Qwen models are now available in Amazon Bedrock

**by Danilo Poccia on 18 SEP 2025 in Amazon Bedrock, Amazon Machine Learning, Announcements, Artificial Intelligence, Featured, Launch, News, Open Source, Serverless**

[▶️ Listen to audio](/images/da4b9237bacccdf19c0760cab7aec4a8359010b0amazon_polly_99109.mp3) Voiced by Polly

Today we are adding Qwen models from Alibaba in Amazon Bedrock. With this launch, Amazon Bedrock continues to expand model choice by adding access to Qwen3 open weight foundation models (FMs) in a full managed, serverless way. This release includes four models: Qwen3-Coder-480B-A35B-Instruct, Qwen3-Coder-30B-A3B-Instruct, Qwen3-235B-A22B-Instruct-2507, and Qwen3-32B (Dense). Together, these models feature both mixture-of-experts (MoE) and dense architectures, providing flexible options for different application requirements.

Amazon Bedrock provides access to industry-leading FMs through a unified API without requiring infrastructure management. You can access models from multiple model providers, integrate models into your applications, and scale usage based on workload requirements. With Amazon Bedrock, customer data is never used to train the underlying models. With the addition of Qwen3 models, Amazon Bedrock offers even more options for use cases like:

- Code generation and repository analysis with extended context understanding
- Building agentic workflows that orchestrate multiple tools and APIs for business automation
- Balancing AI costs and performance using hybrid thinking modes for adaptive reasoning

### Qwen3 models in Amazon Bedrock

These four Qwen3 models are now available in Amazon Bedrock, each optimized for different performance and cost requirements:

- **Qwen3-Coder-480B-A35B-Instruct** – This is a mixture-of-experts (MoE) model with 480B total parameters and 35B active parameters. It's optimized for coding and agentic tasks and achieves strong results in benchmarks such as agentic coding, browser use, and tool use. These capabilities make it suitable for repository-scale code analysis and multistep workflow automation.
- **Qwen3-Coder-30B-A3B-Instruct** – This is a MoE model with 30B total parameters and 3B active parameters. Specifically optimized for coding tasks and instruction-following scenarios, this model demonstrates strong performance in code generation, analysis, and debugging across multiple programming languages.
- **Qwen3-235B-A22B-Instruct-2507** – This is an instruction-tuned MoE model with 235B total parameters and 22B active parameters. It delivers competitive performance across coding, math, and general reasoning tasks, balancing capability with efficiency.
- **Qwen3-32B (Dense)** – This is a dense model with 32B parameters. It is suitable for real-time or resource-constrained environments such as mobile devices and edge computing deployments where consistent performance is critical.

### Architectural and functional features in Qwen3

The Qwen3 models introduce several architectural and functional features:

**MoE compared with dense architectures** – MoE models such as Qwen3-Coder-480B-A35B, Qwen3-Coder-30B-A3B-Instruct, and Qwen3-235B-A22B-Instruct-2507, activate only part of the parameters for each request, providing high performance with efficient inference. The dense Qwen3-32B activates all parameters, offering more consistent and predictable performance.

**Agentic capabilities** – Qwen3 models can handle multi-step reasoning and structured planning in one model invocation. They can generate outputs that call external tools or APIs when integrated into an agent framework. The models also maintain extended context across long sessions. In addition, they support tool calling to allow standardized communication with external environments.

**Hybrid thinking modes** – Qwen3 introduces a hybrid approach to problem-solving, which supports two modes: thinking and non-thinking. The thinking mode applies step-by-step reasoning before delivering the final answer. This is ideal for complex problems that require deeper thought. Whereas the non-thinking mode provides fast and near-instant responses for less complex tasks where speed is more important than depth. This helps developers manage performance and cost trade-offs more effectively.

**Long-context handling** – The Qwen3-Coder models support extended context windows, with up to 256K tokens natively and up to 1 million tokens with extrapolation methods. This allows the model to process entire repositories, large technical documents, or long conversational histories within a single task.

### When to use each model

The four Qwen3 models serve distinct use cases. Qwen3-Coder-480B-A35B-Instruct is designed for complex software engineering scenarios. It's suited for advanced code generation, long-context processing such as repository-level analysis, and integration with external tools. Qwen3-Coder-30B-A3B-Instruct is particularly effective for tasks such as code completion, refactoring, and answering programming-related queries. If you need versatile performance across multiple domains, Qwen3-235B-A22B-Instruct-2507 offers a balance, delivering strong general-purpose reasoning and instruction-following capabilities while leveraging the efficiency advantages of its MoE architecture. Qwen3-32B (Dense) is appropriate for scenarios where consistent performance, low latency, and cost optimization are important.

### Getting started with Qwen models in Amazon Bedrock

To begin using Qwen models, in the Amazon Bedrock console, I can use the Chat/Text Playground section of the navigation pane to quickly test the new Qwen models with a few prompts.

To integrate Qwen3 models into my applications, I can use any AWS SDKs. The AWS SDKs include access to the Amazon Bedrock InvokeModel and Converse API. I can also use these model with any agentic framework that supports Amazon Bedrock and deploy the agents using Amazon Bedrock AgentCore. For example, here's the Python code of a simple agent with tool access built using Strands Agents:

```python
from strands import Agent
from strands_tools import calculator

agent = Agent(
    model="qwen.qwen3-coder-480b-a35b-v1:0",
    tools=[calculator]
)

agent("Tell me the square root of 42 ^ 9")

with open("function.py", 'r') as f:
    my_function_code = f.read()

agent(f"Help me optimize this Python function for better performance:\n\n{my_function_code}")
```
### Now available

Qwen models are available today in the following AWS Regions:

- **Qwen3-Coder-480B-A35B-Instruct** is available in the US West (Oregon), Asia Pacific (Mumbai, Tokyo), and Europe (London, Stockholm) Regions.

- **Qwen3-Coder-30B-A3B-Instruct, Qwen3-235B-A22B-Instruct-2507, and Qwen3-32B** are available in the US East (N. Virginia), US West (Oregon), Asia Pacific (Mumbai, Tokyo), Europe (Ireland, London, Milan, Stockholm), and South America (São Paulo) Regions.

Check the full Region list for future updates. You can start testing and building immediately without infrastructure setup or capacity planning. To learn more, visit the [Qwen in Amazon Bedrock product page](https://aws.amazon.com/bedrock/features/qwen/) and the [Amazon Bedrock pricing page](https://aws.amazon.com/bedrock/pricing/).

Try Qwen models on the Amazon Bedrock console now, and offer feedback through [AWS re:Post for Amazon Bedrock](https://repost.aws/tags/TAxZAJ5PL9qHTYFdH8yKBPBw/amazon-bedrock) or your typical AWS Support channels.

— Danilo

**Updated on September 18, 2025** — Removed the model access section. Amazon Bedrock will simplify access to all serverless foundation models, and any new models, by automatically enabling them for every AWS account, eliminating the need to manually activate access through the Bedrock console. The model access page will be retired in October 8, 2025. Account administrators retain full control over model access through AWS IAM policies and Service Control Policies (SCPs) to restrict model access as needed.

---

![Profile Image](/images/danilo.png)

**Danilo Poccia**

Danilo works with startups and companies of any size to support their innovation. In his role as Chief Evangelist (EMEA) at Amazon Web Services, he leverages his experience to help people bring their ideas to life, focusing on serverless architectures and event-driven programming, and on the technical and business impact of machine learning and edge computing. He is the author of AWS Lambda in Action from Manning.