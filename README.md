# Build an AI-powered Restaurant Booking Assistant with Amazon Bedrock & Strands Agents

Built an AI-powered restaurant booking assistant that understands natural-language requests, retrieves contextual restaurant data, and performs booking actions (create, read, delete) by orchestrating LLM reasoning with simple cloud tools. This project demonstrates how to design, implement, and scale the agent using the Strands Agents SDK running on a Bedrock foundation model, Bedrock Knowledge Bases for retrieval, DynamoDB for bookings, and optional serverless or container deployments (Lambda or Fargate) for production scale.

## Overview

The goal of this project is not to ship a full production application, but to:
* Showcase a **real-world AI agent use case**
* Explain **AWS architectural decisions** clearly
* Provide **reproducible code and visuals** for readers
* Serve as a reference implementation for developers building agent-based systems

---

## Focus Areas

1. **Problem & Solution**
   Why traditional rule-based systems fail for conversational workflows and how AI agents solve this using reasoning and tools.

2. **Technical Implementation**
   How Amazon Bedrock, Strands Agents, DynamoDB, and supporting AWS services work together.

3. **Scaling Strategy**
   How the system performs today and how it can scale using AWS-native patterns.

---

## Architecture

**Core components:**

* **Amazon Bedrock** – Foundation model inference
* **Strands Agents SDK** – Agent orchestration and tool calling
* **Amazon DynamoDB** – Persistent storage for agent actions
* **Amazon S3** – Knowledge base documents
* **AWS Lambda / Fargate** – Agent runtime
* **OpenTelemetry / CloudWatch** – Observability

The agent uses natural language reasoning to decide **when to retrieve knowledge** and **when to invoke tools**, keeping business logic explicit and auditable.

---

## Repository Structure

```
.
├── 01-tutorials/
│   ├── 01-fundamentals/
│   │   ├── 01-first-agent/
│   │   ├── 02-model-providers/
│   │   ├── 03-connecting-with-aws-services/
│   │   ├── 04-tools/
│   │   ├── 05-advance-processing-agent-response/
│   │   ├── 06-guardrail-integration/
│   │   ├── 07-memory-persistent-agents/
│   │   ├── 08-observability-and-evaluation/
│   │   └── 09-bidirectional-streaming/
│   │               
│   ├── 02-multi-agent-systems/
│   │   ├── 01-agent-as-tool/
│   │   ├── 02-swarm-agent/
│   │   └── 03-graph-agent/
│   │
│   └── 03-deployments/
│       ├── 01-lambda-deployment/
│       ├── 02-fargate-deployment/
│       └── 03-agentcore-deployment/
│
├── 02-samples/
│   ├── 01-restaurant-assistant/
│   └── 05-personal-assistant/
│                      
└── README.md                   
```

---

## How This Repo Is Meant to Be Used

This repository is intentionally **lightweight and educational**:
* Code snippets are optimized for **clarity**, not feature completeness
* Infrastructure is optional and kept minimal

Readers are encouraged to:
* Fork the repo
* Modify tools and prompts
* Swap in their own use cases

---

## Scaling & Production Notes

While this project is a prototype, the blog explains how to scale it using:
* AWS Fargate auto-scaling
* DynamoDB on-demand capacity
* Caching for retrieval results
* Cost controls for LLM inference
* Guardrails and IAM-based security

---

## Disclaimer

This project is for **educational and demonstration purposes** only. It is not an official AWS product and should not be used in production without proper security, testing, and cost controls.

---
