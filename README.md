# Multi-Agent Systems and Frameworks

**Multi-agent systems** empower AI to work collaboratively on complex tasks that go beyond a single model’s capacity.  Recent frameworks provide infrastructure so language‑model agents can plan and reason about tasks, call external tools and APIs, maintain memory across long interactions, manage workflows with error handling, and even cooperate with other agents【737265182014936†L40-L60】.  This repository explores these capabilities and summarises several leading frameworks to help developers get started building their own agentic applications.

## Why Multi‑Agent Frameworks Matter

As developers move from simple LLM chatbots to autonomous systems that perform research, code, or customer support, they need scaffolding to structure the agent’s actions.  Modern frameworks provide:

- **Planning and reasoning**: support for decomposing complex problems into sub‑tasks and reasoning about them【737265182014936†L55-L60】.
- **Tool usage**: functions or APIs can be invoked to fetch data, call services, or execute code【737265182014936†L55-L60】.
- **Memory and context management**: persistent state allows agents to reference previous steps or summarise long conversations【737265182014936†L55-L60】.
- **Workflow orchestration**: flows, DAGs, or event‑driven architectures manage the order of actions, error handling, and retries【737265182014936†L55-L60】.
- **Multi‑agent collaboration**: frameworks allow multiple agents with different roles to interact and coordinate on a task【737265182014936†L55-L60】.
- **Data‑augmented generation**: connectors to vector stores and databases enable retrieval‑augmented generation (RAG)【737265182014936†L55-L60】.

Developing robust multi‑agent systems also requires careful **context engineering** – designing prompts and memory structures so each agent receives the right information at the right time.  Without clear objectives and context, agents duplicate work or miss critical information【1725787987300†L26-L72】.

## Overview of Notable Frameworks (May 2025)

The following open‑source frameworks illustrate different approaches to building agentic systems.  Each entry notes the language, agent style and key features based on current documentation【737265182014936†L68-L90】 【737265182014936†L96-L117】 【737265182014936†L123-L157】 【737265182014936†L161-L181】 【737265182014936†L187-L200】.

| Framework | Key characteristics | Why it’s interesting |
|---|---|---|
| **AG2 (AutoGen 2)** | Python‑based framework that frames everything as an asynchronous conversation between specialized agents; supports multi‑agent collaboration, tool integration and code execution【737265182014936†L68-L90】. | Event‑driven architecture allows agents (e.g., planning, user proxy, coding) to work concurrently, reducing bottlenecks and supporting human‑in‑the‑loop interactions【737265182014936†L81-L84】. |
| **CrewAI** | Role‑based orchestration where agents are assigned roles like **Researcher**, **Writer** and **Critic**【737265182014936†L96-L108】.  Supports self‑organizing crews or explicit flows【737265182014936†L110-L113】. | Intuitive “crew” metaphor makes complex interactions approachable; widely adopted with a large community and growing ecosystem【737265182014936†L115-L117】. |
| **LangChain & LangGraph** | LangChain provides a component library and extensive tools; LangGraph represents agent reasoning as a Directed Acyclic Graph for deterministic flows【737265182014936†L123-L148】. | Graph‑based execution enables parallelism, conditional branches and explicit error handling; used in production by companies like Replit, Uber and Klarna【737265182014936†L146-L154】. |
| **OpenAI Agents SDK** | Official framework for building agents that use function‑calling and agent handoffs; emphasises lightweight runtime and guardrails for safety【737265182014936†L161-L176】. | Designed for seamless integration with OpenAI models, offering content filtering and output validation; quickly becoming a standard for production deployments【737265182014936†L169-L181】. |
| **Google Agent Development Kit (ADK)** | Provides constructs for sequential, loop and parallel agents; integrates with Google Cloud and supports OpenAPI tools【737265182014936†L187-L200】. | Offers explicit workflow control and enterprise integration, including support for the emerging Model Context Protocol (MCP) and Agent‑to‑Agent (A2A) protocols【737265182014936†L193-L199】. |
| **Microsoft Semantic Kernel (SK)** | Multi‑language SDK (C#, Python, Java) treating AI agents as skills and plugins; focuses on type safety and enterprise integration【737265182014936†L214-L236】. | Leverages conventional programming paradigms and planning to orchestrate reusable skills across projects【737265182014936†L223-L236】. |
| **Hugging Face SmolAgents** | Minimal (~1 k LOC) framework where agents “think in Python code” by generating and executing code snippets; integration with Hugging Face Hub【737265182014936†L241-L263】. | Extreme simplicity facilitates rapid prototyping and experimentation; can import any Python library within generated code【737265182014936†L247-L257】. |
| **LlamaIndex** | Data‑centric framework focusing on retrieval‑augmented generation; provides query engines, vector stores and connectors【737265182014936†L268-L287】. | Excels at connecting language models to data sources, enabling agents to answer questions from custom datasets【737265182014936†L270-L287】. |
| **Pydantic AI** | Schema‑driven framework bringing type safety to LLM outputs; emphasises structured I/O with validation【737265182014936†L293-L304】. | Output schema enforcement reduces parsing errors and ensures consistent formats, making it valuable for production applications【737265182014936†L293-L304】. |

## Using this Repository

This repository contains:

- `README.md` – this overview of multi‑agent systems and frameworks with citations.
- Example code (to be added) demonstrating how to set up a simple multi‑agent workflow using one or more frameworks.

Contributions are welcome!  Feel free to open issues or pull requests to discuss improvements, add examples, or share insights about building agentic applications.
