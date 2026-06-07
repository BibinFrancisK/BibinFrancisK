![header](https://capsule-render.vercel.app/api?type=waving&color=0:1e3a5f,100:2496ED&height=160&section=header&text=Bibin%20Francis&fontSize=40&fontColor=ffffff&fontAlignY=38&desc=Senior%20Backend%20%26%20Cloud%20Engineer%20%C2%B7%20LLM%20Systems&descSize=16&descAlignY=60)

# Bibin Francis

<p align="center">
  <a href="https://linkedin.com/in/bibin-francis"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=flat-square&logo=linkedin&logoColor=white" alt="LinkedIn" /></a>
  <img src="https://komarev.com/ghpvc/?username=BibinFrancisK&style=flat-square&color=0A66C2&label=Profile+views" alt="Profile views" />
</p>

**Senior backend & cloud engineer. I build Java/Spring Boot services on AWS - and lately the LLM systems that sit on top of them.**

I've spent 4+ years building microservices for financial-services platforms, where a wrong number is a real problem, so correctness, observability, and clean failure modes matter more than novelty. For the last while I've been shipping production LLM features into that same environment: retrieval over internal docs, agents that review code and triage incidents. I care about the unglamorous parts - guardrails, structured output, cost, and what happens when the model is wrong.

I'm looking for remote or visa-sponsored backend engineering roles in the **the Netherlands or Ireland**.

### Stack

**Backend & Languages**

![Java](https://img.shields.io/badge/Java-ED8B00?style=flat-square&logo=openjdk&logoColor=white)
![Spring Boot](https://img.shields.io/badge/Spring%20Boot-6DB33F?style=flat-square&logo=springboot&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
![NestJS](https://img.shields.io/badge/NestJS-E0234E?style=flat-square&logo=nestjs&logoColor=white)

**Cloud & Infra**

![AWS](https://img.shields.io/badge/AWS-232F3E?style=flat-square&logo=amazonwebservices&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![Kubernetes](https://img.shields.io/badge/Kubernetes-326CE5?style=flat-square&logo=kubernetes&logoColor=white)
![Terraform](https://img.shields.io/badge/Terraform-844FBA?style=flat-square&logo=terraform&logoColor=white)

**Data & Streaming**

![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)
![Apache Kafka](https://img.shields.io/badge/Apache%20Kafka-231F20?style=flat-square&logo=apachekafka&logoColor=white)
![pgvector](https://img.shields.io/badge/pgvector-4169E1?style=flat-square)
![Snowflake](https://img.shields.io/badge/Snowflake-29B5E8?style=flat-square&logo=snowflake&logoColor=white)

**AI / LLM**

![LangChain4j](https://img.shields.io/badge/LangChain4j-1C3C3C?style=flat-square&logo=langchain&logoColor=white)
![LangGraph4j](https://img.shields.io/badge/LangGraph4j-1C3C3C?style=flat-square)
![Claude](https://img.shields.io/badge/Claude-D97757?style=flat-square&logo=claude&logoColor=white)
![Gemini](https://img.shields.io/badge/Gemini-8E75B2?style=flat-square&logo=googlegemini&logoColor=white)

## What I work on

**Backend & Cloud**
- Java 21, Spring Boot 3, microservices, event-driven design (Kafka, SNS/SQS)
- AWS - Lambda, ECS Fargate, API Gateway, RDS/DynamoDB, CDK, CloudFormation
- PostgreSQL, IBM DB2, Snowflake; Docker; GitHub Actions CI/CD
- The stuff that keeps services up: distributed tracing, anomaly detection, incident response, 90%+ coverage

**AI / LLM Engineering**
- RAG pipelines - LangChain4j + pgvector: chunking, embeddings, retrieval that's actually grounded
- Multi-agent orchestration with LangGraph4j
- Structured LLM output with schema validation, so malformed JSON never reaches a caller
- Built day-to-day with Claude Code, MCP servers, and the Anthropic + Gemini SDKs

## Selected projects

<p align="center">
  <a href="https://github.com/BibinFrancisK/ai-code-review-agent">
    <img src="https://github-readme-stats.vercel.app/api/pin/?username=BibinFrancisK&repo=ai-code-review-agent&theme=tokyonight&hide_border=true" alt="AI Code Review Agent" />
  </a>
  <a href="https://github.com/BibinFrancisK/ai-cloud-architecture-advisor">
    <img src="https://github-readme-stats.vercel.app/api/pin/?username=BibinFrancisK&repo=ai-cloud-architecture-advisor&theme=tokyonight&hide_border=true" alt="AI Cloud Architecture Advisor" />
  </a>
</p>

### AI Code Review Agent - [repo](https://github.com/BibinFrancisK/ai-code-review-agent)
A bot that reviews GitHub PRs automatically and posts inline comments.
- **Problem:** manual review is slow and keeps missing the same bug classes - SQL injection, N+1 queries, swallowed exceptions.
- **Stack:** Java, Spring Boot, LangChain4j, Google Gemini, PostgreSQL + Flyway, AWS EC2 via CDK.
- **Result:** ~50% faster review cycles and ~30% more issues caught than manual review alone. HMAC-verified webhooks, async processing, ~0% false positives on the test PR set.

### AI Cloud Architecture Advisor - [repo](https://github.com/BibinFrancisK/ai-cloud-architecture-advisor)
Asks the right clarifying questions, then generates a grounded AWS architecture and the CDK to deploy it.
- **Problem:** early architecture decisions are slow and easy to get wrong.
- **Stack:** NestJS, TypeScript, LangChain.js, pgvector, AWS CDK → ECS Fargate.
- **Result:** ~40% less architecture-design time. RAG over a curated AWS knowledge base; CDK generation is gated behind an explicit approval step, so it can't emit infra you didn't sign off on.

### Enterprise RAG Knowledge Base - *[open source version in progress]*
Natural-language search over internal financial-services documentation.
- **Problem:** institutional knowledge walks out the door at every team transition.
- **Stack:** Spring Boot, LangChain4j, pgvector.
- **Result:** cut developer onboarding ~50%. *Built at work - needs a public, sanitized version living here.*

### Multi-Agent Incident Response - *[open source version in progress]*
Agents that correlate logs and traces across services, assess impact, and draft the postmortem.
- **Problem:** during an incident, the slow part is working out what actually broke, and where.
- **Stack:** LangGraph4j, Spring Boot.
- **Result:** ~60% lower mean-time-to-resolution, with auto-generated structured postmortems. *Built at work - the public LangGraph4j version is my next repo.*

## Currently building
- A public LangGraph4j multi-agent project (above) - the repo I most want to exist.
- An AI test-generation engine (LangChain4j) that writes JUnit tests from diffs - ~85% valid-generation rate so far.
- A Kafka + anomaly-detection batch monitor that flags processing deviations in minutes instead of hours (99.9%+ batch accuracy in production).

## By the numbers

<p align="center">
  <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=BibinFrancisK&layout=compact&theme=tokyonight&hide_border=true&langs_count=8&hide=css,html,dockerfile" alt="Top languages" />
  <img src="https://github-readme-stats.vercel.app/api?username=BibinFrancisK&show_icons=true&theme=tokyonight&hide_border=true&include_all_commits=true&hide=stars" alt="GitHub stats" />
</p>

## Reach me
- **LinkedIn** - https://linkedin.com/in/bibin-francis
- Based in India · open to relocation · targeting **the Netherlands/ Ireland**
