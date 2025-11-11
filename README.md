# 🏗️ Serverless Chat Application – Deployment Architecture

![AWS](https://img.shields.io/badge/AWS-Cloud-orange?logo=amazon-aws&logoColor=white)
![Serverless](https://img.shields.io/badge/Serverless-Architecture-blue)
![OpenAI](https://img.shields.io/badge/OpenAI-LLM-green)
![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)

This repository showcases the **deployment architecture and infrastructure setup** for a **serverless AI-powered chat application**, leveraging **AWS services**, **Amazon Bedrock**, and **OpenAI LLMs** for intelligent conversational experiences.  
The design prioritizes scalability, low latency, and minimal operational overhead using a fully managed cloud-native approach.


## Architecture Overview

The architecture consists of the following components:

### Frontend – S3 + CloudFront  
- A **static web application** hosted in **Amazon S3**.  
- Distributed globally through **Amazon CloudFront** for high performance, caching, and SSL-secured access.

###  API Gateway  
- Serves as the **entry point** for all client requests.  
- Manages routing, authentication, and rate-limiting to backend services.

### AWS Lambda – Business Logic Layer  
- Contains the **core logic** for handling chat interactions.  
- Processes user input, integrates with both **OpenAI** and **Bedrock** models, and manages responses.  
- Implements lightweight orchestration and memory handling.

### LLM Engines – Bedrock & OpenAI  
- **Amazon Bedrock**: Provides access to foundational models for enterprise-grade AI.  
- **OpenAI LLM (e.g., GPT-4)**: Enhances conversational capabilities with advanced natural-language understanding and reasoning.  
- Lambda dynamically routes requests to the most appropriate model based on context or configuration.

### S3 Storage – Memory Layer  
- Stores **conversation history** and session metadata for persistence.  
- Enables contextual continuity across chat sessions.


