# AI Tools & Agentic Development Track

## Objective

Become an **AI-native/AI-leveraged software engineer** who can:

- Use coding assistants effectively without blindly trusting them
- Build LLM-enabled application features
- Understand RAG, embeddings, vector search, tool calling, agents, and evaluation
- Apply production considerations: security, cost, observability, reliability
- Demonstrate this skill through 5-6 small, focused projects/artifacts

This track deliberately prioritizes engineering judgment. AI should accelerate your work, but you remain responsible for requirements, architecture, security, tests, and correctness.

---

## Tool Stack

### Coding Assistants

- **Cursor**: Primary home IDE assistant; use codebase context, rules, agent/composer workflows, terminal actions, and code review.
- **GitHub Copilot**: Fast inline completion and chat; compare outputs with Cursor, especially for tests and boilerplate.
- **Claude / ChatGPT**: Design reviews, debugging, architecture discussions, teaching, mock interviews.
- **Perplexity**: Current documentation, comparisons, API research, and fact checks.

### AI Application Stack

- **Model APIs**: OpenAI, Anthropic, Gemini, or a local model for experimentation.
- **Java/Spring options**: Spring AI or LangChain4j.
- **Python exploration (optional)**: LangChain, LangGraph, LlamaIndex.
- **Embeddings/vector stores**: pgvector (recommended because you already use PostgreSQL), Chroma for local experiments, Pinecone/Weaviate for comparison.
- **Observability/evaluation**: LangSmith concepts, OpenTelemetry, structured logs, a small hand-written evaluation set.

---

## AI-First Development Rules

Use these rules for your Swiggy project and machine-coding practice:

1. **State the acceptance criteria before prompting.**
2. **Ask AI for a plan first, then approve/revise the plan.**
3. **Generate in small diffs**, not an entire application at once.
4. **Read every generated change** before accepting it.
5. **Run tests and add edge cases yourself.**
6. **Never paste company-private code or credentials into consumer AI tools.**
7. **Document the prompt, output, edits, and learning** for one meaningful task per week.
8. **Use AI to explain code only after you first attempt to understand it.**

### Prompt Template

```text
Context:
I have a Spring Boot 3 service using Java 21, PostgreSQL, Flyway, and JUnit 5.

Task:
Implement <specific feature>.

Constraints:
- Keep business logic in the service layer.
- Return the existing standardized error format.
- Do not change public API contracts.
- Prefer constructor injection.
- Do not introduce new dependencies without explaining why.

Acceptance criteria:
- <testable criterion 1>
- <testable criterion 2>
- Unit tests for success, validation failure, and error path.

First provide an implementation plan and assumptions. Do not write code yet.
```

---

# 16-Week AI/Agentic Roadmap

## Week 1: Cursor Setup and Safe Workflow

**Learn**
- Cursor installation, codebase indexing, chat vs agent/composer mode.
- Project rules/instructions, terminal commands, Git diff review.
- Difference between autocomplete and autonomous actions.

**Build/Practice**
- Create a small Spring Boot project through Cursor scaffolding.
- Review every generated package, dependency, and configuration.
- Create `AI_NOTES.md` in your project: prompt, output, changes you accepted/rejected, lessons.

**Deliverable:** Cursor configured; one documented AI-assisted change.

---

## Week 2: Copilot/Cursor Test Generation and Review

**Learn**
- Prompting for unit tests, mocks, edge cases, and negative paths.
- Detecting hallucinated APIs, incorrect assumptions, unnecessary dependencies.

**Build/Practice**
- Use Cursor or Copilot to propose tests for Auth service registration/login.
- Improve tests yourself: validation, duplicate user, invalid password, expired token.
- Ask a second model to review the generated tests, then compare feedback.

**Deliverable:** Better tests + a checklist for reviewing AI-generated code.

---

## Week 3: AI Code Review Assistant

**Learn**
- Structured outputs (JSON schema concept), prompting for severity/confidence.
- Why AI review complements—not replaces—static analysis and human review.

**Build**
- Small CLI or Spring endpoint: input a diff/text → LLM returns findings under categories: correctness, security, performance, test gaps, maintainability.
- Add a prompt that instructs the model to cite exact line snippets from the supplied diff only.

**Deliverable:** Mini AI project #1: code-review assistant.

---

## Week 4: RAG Fundamentals

**Learn**
- Tokens, embeddings, chunking, vector similarity, retrieval, reranking, context injection, hallucination.
- RAG is not simply "upload PDFs to an LLM": relevance, grounding, and evaluation matter.

**Build**
- Local document Q&A POC over your own Markdown notes.
- Use pgvector/Chroma; store document metadata and source paths.
- Return source chunks alongside every answer.

**Deliverable:** Mini AI project #2: local document Q&A with citations.

---

## Week 5: LLM Application Architecture

**Learn**
- LLM request lifecycle: React UI → Spring API → orchestration → model/tool/retrieval → response.
- Streaming responses, retries, timeouts, rate limits, token/cost tracking.
- API keys and secrets management.

**Build**
- Add a simple chat endpoint with Spring AI or LangChain4j.
- Add a React chat component with loading/error/streaming states.
- Use a narrow system prompt and explicit output format.

**Deliverable:** A minimal secure chat feature skeleton.

---

## Week 6: Tool Calling and Simple Agents

**Learn**
- Difference: chatbot vs workflow vs agent.
- Tool definitions, function calling, validation, tool authorization, deterministic workflows.
- Agent state, memory, termination conditions.

**Build**
- Create a **Project Documentation Assistant** that can retrieve project docs and use read-only tools: `searchArchitectureDocs`, `listServices`, `getApiContract`.
- Validate every tool argument server-side; never let an LLM run unrestricted shell/SQL commands.

**Deliverable:** Mini AI project #3: read-only documentation assistant.

---

## Week 7: RAG Quality and Evaluation

**Learn**
- Retrieval recall vs answer quality.
- Golden question set, groundedness, relevance, faithfulness, latency, cost.
- Chunk-size/overlap and metadata filtering trade-offs.

**Build**
- Create 15-20 questions about your Swiggy project docs.
- Test your RAG assistant and log answer quality, retrieved chunks, latency, and failure modes.
- Improve chunking or retrieval filters based on results.

**Deliverable:** RAG evaluation CSV/Markdown report.

---

## Week 8: RAG Assistant for Your Project

**Build**
- Ingest architecture docs, API specs, runbooks, and service READMEs.
- Add citations linking answers to document section/source.
- Add role-based scope if you expose it publicly (only public project docs).
- Deploy a limited demo or run locally; do not expose model keys to React.

**Deliverable:** Mini AI project #4: Swiggy project documentation assistant.

---

## Week 9: AI Feature for Food Discovery

**Learn**
- When structured filtering beats an LLM.
- Hybrid workflow: normal restaurant search/filter first, LLM for natural-language interpretation or explanation.

**Build**
- Implement a controlled "What should I eat?" assistant.
- The agent may call a **read-only restaurant search tool** with dietary preference, cuisine, budget, and rating filters.
- Model returns recommendations based only on tool results; show disclaimer and reasons.

**Deliverable:** AI feature #1 in Swiggy project.

---

## Week 10: Agent Workflows and LangGraph Concepts

**Learn**
- Multi-step workflows, state machines, routing, retries, human approval points.
- LangGraph concepts; implement equivalent deterministic state flow in Java if preferred.

**Build**
- Build a **Project Task Assistant**: input feature request → create plan → identify services affected → propose subtasks → ask for approval before generating a task list.
- Store only non-sensitive task content.

**Deliverable:** Mini AI project #5: planning agent.

---

## Week 11: AI Security and Safety

**Learn**
- Prompt injection, data exfiltration, insecure output handling, tool abuse, excessive agency, PII leakage.
- Rate limits, quotas, model fallback, audit logs, content boundaries.

**Build**
- Add test prompts designed to attack your RAG/tool system.
- Add defenses: system boundaries, document allow-list, tool allow-list, input/output validation, redacted logs.
- Document residual risks.

**Deliverable:** AI security checklist + adversarial test report.

---

## Week 12: Agentic Coding Workflow

**Learn/Practice**
- Issue → plan → implementation → tests → code review → pull request workflow.
- Human-in-the-loop checkpoints and how to avoid AI-generated overengineering.

**Build**
- Use Cursor agent mode on one bounded project issue.
- Require it to create a plan, make small commits/diffs, run tests, and draft PR notes.
- Audit its work manually and record defects it missed.

**Deliverable:** Case study: "AI-assisted feature delivery with verification."

---

## Week 13: Production LLM Concerns

**Learn**
- Cost controls, caching, streaming, fallbacks, model selection, structured output schemas.
- Observability: prompt/model version, token use, latency, tool calls, error rate.

**Build**
- Add request IDs, latency logs, and approximate usage/cost tracking to one AI endpoint.
- Set per-user rate limits and maximum tool calls.

**Deliverable:** LLM operations dashboard/logging design.

---

## Week 14: AI Architecture Decision Record

**Build**
- Write an ADR comparing:
  - API model vs local model
  - RAG vs fine-tuning
  - pgvector vs dedicated vector DB
  - agent vs deterministic workflow
  - synchronous vs asynchronous response
- Use your Swiggy AI feature as the example.

**Deliverable:** `docs/adr/ADR-001-ai-architecture.md`.

---

## Week 15: Job-Search Assistant (Safe, Personal Tool)

**Build**
- Create a personal utility that takes a job description + your approved achievement inventory and produces:
  - Skills match summary
  - Suggested truthful resume bullet ordering
  - Draft outreach message
  - Interview-topic checklist
- Never let it invent experience; require it to quote from your approved inventory.

**Deliverable:** Mini AI project #6: job-search assistant.

---

## Week 16: Portfolio and Interview Story

**Tasks**
- Write a 1-page AI/agentic engineering portfolio summary.
- Prepare answers for:
  - "How did you use AI safely in development?"
  - "Explain RAG end to end."
  - "When would you not use an agent?"
  - "How did you evaluate your AI feature?"
  - "How do you prevent prompt injection/tool abuse?"
- Publish a technical post or README section about one AI project.

**Deliverable:** Interview-ready AI/agentic development story.

---

## Mini Project Portfolio

| # | Project | Core Skill | Weeks |
|---|---------|------------|-------|
| 1 | AI Code Review Assistant | Structured prompting, review workflow | 3 |
| 2 | Local Document Q&A | Embeddings, retrieval, citations | 4 |
| 3 | Project Documentation Assistant | Tool calling, guardrails | 6 |
| 4 | Swiggy Documentation RAG | Evaluation, deployment | 8 |
| 5 | Food Recommendation Assistant | Controlled tools + structured data | 9 |
| 6 | Project Task Assistant | Agent workflow/state | 10 |
| 7 | Job Search Assistant | Safe AI automation, factual grounding | 15 |

---

## Resources

- Spring AI documentation
- LangChain4j documentation
- LangChain and LangGraph documentation (for concepts)
- Anthropic/OpenAI/Gemini API documentation
- OWASP Top 10 for LLM Applications
- Full Stack Deep Learning (LLM bootcamp materials)

## Success Metrics

- **Week 4**: Can explain RAG components and build a local POC.
- **Week 8**: Have a project-doc RAG assistant with a test set.
- **Week 12**: Have used safe tool calling/agentic workflow on real project tasks.
- **Week 16**: Can explain AI architecture, trade-offs, evaluation, and security in interviews.
