# Introduction to AI for Developers

### 10-บท Course Outline

2026-09-19 · @Someone

> **Change note:** The original บทที่ 3–4 (Machine Learning Quickstart, Deep Learning Essentials) were removed; materials archived in `archive/`. Their slots were refilled with new content: บทที่ 2 is now Prompt Engineering for general users via Cline, บทที่ 3 is now **Basic Prompt Engineering — Techniques & Frameworks for Developers** (GSD, GitHub Spec Kit, and a third framework pending name confirmation — see `week_03/`), and บทที่ 4 is now **Developing AI Skills** (writing `SKILL.md` files that define Objective/Input/Process/Output for a specialized, reusable agent capability, then Test & Iterate). บทที่ 4 has been rewritten twice before landing here -- it briefly held Python & Essential Libraries content, then a "Systematic Prompt Engineering Skill Development" framing -- Python is now purely a course Prerequisite, not taught in any chapter. บทที่ 5 has separately been rewritten from **NLP for Developers** to **Model Context Protocol (MCP)** -- tokenization/embeddings/BERT/GPT are no longer taught anywhere in the course; บทที่ 6's HuggingFace-recap content and prerequisites should be checked against this. All 10 chapter slots (1–10) now have live content, so the course is back to a full **10-บท** outline.

## Course Overview

This course introduces AI concepts, tools, and hands-on techniques tailored for software developers and IT professionals with little to no prior AI experience.

| Item | Detail |
| --- | --- |
| Audience | IT professionals and software developers |
| Format | Lecture (1 hr) + Workshop (1.5-2 hr) ต่อบท |
| Duration | 10 บท (บทที่ 1–10; the original ML/DL บทที่ 3–4 were replaced with new content — see change note above; original materials kept in `archive/`) |
| Outcome | Build a working Agentic AI project by บทที่ 10 |

### Prerequisites

Participants should have before starting:

- Basic Python programming (variables, loops, functions)
- Familiarity with command line / terminal
- Access to Google Colab or a local Python environment (Jupyter Notebook)

> **Note for instructors:** Run a short Python pre-test or share a pre-course warm-up notebook in บทที่ 0 to align skill levels before บทที่ 1.

## บทที่ 1: AI Fundamentals for Developers

Participants leave understanding what AI, ML, and DL are, and where they fit in the modern developer toolkit.

**Lecture (1 hr)**

1. What is AI? -- AI vs. ML vs. Deep Learning, and why the distinction matters for developers
2. Why AI matters for developers -- automating routine tasks, boosting productivity, enabling new products
3. AI ecosystem overview -- ChatGPT, GitHub Copilot, HuggingFace, TensorFlow, PyTorch
4. Responsible AI basics -- hallucination, bias, and when not to trust the model

**Workshop (1.5 hr)**

1. Demo: use GitHub Copilot to write a Python data-cleaning function
2. Exercise: participants write their own cleaning function with Copilot assistance
3. Discussion: share one pain point in current workflow that AI might address

## บทที่ 2: Prompt Engineering for General Users

Participants understand what prompt engineering is and can use AI through Cline (VS Code extension) for everyday work -- writing effective prompts, drafting documents, analyzing images, building tables, and summarizing information -- while knowing AI's limitations and how to use it safely.

**Lecture (1 hr)**

1. What is prompt engineering? -- how LLMs work with text (next-token prediction), why input quality determines output quality
2. Techniques for effective prompts -- be specific, give context, set a role, specify output format, provide examples (few-shot), break big tasks into steps
3. Applying AI via Cline -- drafting documents (email/reports/meeting notes), describing and analyzing images, creating tables, summarizing long content -- working directly on files in the project
4. AI limitations and safe use -- hallucination/bias recap from บทที่ 1, training-cutoff knowledge, no personal or confidential data, always verify before use

**Workshop (1.5 hr)**

1. Demo: live improvement of a bad prompt into a good one in Cline
2. Exercise: participants write prompts for 3 scenarios (draft a document, summarize content, analyze an image or table), iterating at least twice per scenario
3. Discussion: share prompts that worked or failed, and which technique helped most

## บทที่ 3: Basic Prompt Engineering (Techniques & Frameworks for Developers)

Participants extend the prompt engineering techniques from บทที่ 2 into software development work, and learn the concept of spec-driven / agentic development frameworks -- using GSD, GitHub Spec Kit, and a third framework (pending name confirmation) to structure how they direct AI coding agents on larger tasks.

**Lecture (1 hr)**

1. Prompt engineering for software development -- system prompts, instruction files (e.g. CLAUDE.md), context engineering
2. What is spec-driven / agentic development -- why a single prompt isn't enough for complex work; the spec -> plan -> execute -> verify idea
3. Framework: GSD (Get Shit Done) -- phase-based workflow (research -> plan -> discuss -> execute -> verify)
4. Framework: GitHub Spec Kit (+ intro to the third framework) -- specify -> plan -> tasks -> implement; compare with GSD and the third framework

**Workshop (1.5 hr)**

1. Demo: use GSD to plan a small feature phase-by-phase
2. Exercise: write a spec with GitHub Spec Kit for a mini-feature of the participant's own
3. Discussion: compare GSD vs. Spec Kit vs. the third framework vs. plain prompting -- when to use which

## บทที่ 4: Developing AI Skills

Participants build **AI Skills** -- reusable, well-scoped capability packages that let an AI agent perform a specialized task consistently, instead of re-typing a prompt from scratch every time. This is done by writing a specification file (e.g. `SKILL.md`) that states the Objective, a three-part Structure (Input / Process / Output), and then running the skill through a Test & Iterate loop until it's reliable.

**Lecture (1 hr)**

1. What is an AI Skill -- how it differs from a one-off prompt; why repeatable specialized tasks benefit from a packaged capability
2. Defining the Objective -- stating clearly what the AI should do, when to use the skill, and when not to (e.g. summarizing reports, analyzing data)
3. Structuring the skill -- breaking it into Input (what data it takes), Process (the steps it follows), and Output (the result format)
4. Test & Iterate -- running the skill for real, catching errors, and refining the SKILL.md conditions until the output is accurate

**Workshop (1.5 hr)**

1. Demo: write a SKILL.md live (Objective -> Structure), test it, and iterate based on the result
2. Exercise: participants write their own SKILL.md for a specialized task from their own work, test it against a real AI agent, and iterate at least twice
3. Discussion: share the skill each person built and what broke during testing

> **Note:** บทที่ 4 no longer teaches Python/NumPy/Pandas/Matplotlib (its earlier content, briefly here after the บทที่ 3-4 ML/DL removal) -- see the change note at the top of this document. Python is treated purely as a course Prerequisite from here on; no chapter re-teaches it. Connecting an AI Skill to external systems (MCP, databases) is only introduced at a high level here -- full tool-use/API integration is covered in บทที่ 8-9.

## บทที่ 5: Model Context Protocol (MCP)

Participants understand what the Model Context Protocol (MCP) is, why an open standard for connecting LLMs to external data and tools matters, the Host-Client-Server architecture and its three core primitives (Tools, Resources, Prompts), and build + connect their first MCP Server to an MCP Host such as Claude Desktop.

**Lecture (1 hr)**

1. MCP overview -- an open standard from Anthropic (the "USB port for AI"), and the Host / Client (1:1) / Server architecture
2. The three MCP primitives -- Tools (actions to invoke), Resources (read-only data), Prompts (reusable templates) -- and who decides to invoke each
3. Getting started building an MCP Server -- define the goal, pick a language + SDK, test the connection to an MCP Host (with a pointer toward connecting a real database such as PostgreSQL)

**Workshop (1.5-2 hr)**

1. Build your first MCP Server: write a simple Tool and Resource using the MCP SDK (Python or TypeScript)
2. Connect to an MCP Host (e.g. Claude Desktop): configure `claude_desktop_config.json`, restart, and have the AI call your Tools for real
3. Extend + Discussion: connect a real data source (e.g. a file, or a read-only PostgreSQL database) and discuss permission scoping for Tools

> **Note:** บทที่ 5 no longer teaches NLP/tokenization/embeddings/BERT/GPT (its earlier content) -- that material was replaced by MCP. บทที่ 6's HuggingFace/API-access content and its prerequisite check should not assume participants already covered tokenization or pretrained NLP models in this course.

## บทที่ 6: Generative AI Basics

Participants understand how LLMs work, write effective prompts, and build a simple chatbot using an API.

**Lecture (1 hr)**

1. LLMs explained -- how they are trained, why they are probabilistic, and what that means for reliability
2. Prompt engineering principles -- clear instructions, role-setting, chain-of-thought, few-shot examples
3. HuggingFace Transformers and API access -- calling a model vs. running one locally

**Workshop (1.5-2 hr)**

1. Prompt design exercise: iteratively improve a prompt for a summarization task
2. Build a simple Q&A chatbot using an LLM API (OpenAI or Anthropic Claude)
3. Evaluate outputs: spot hallucinations and discuss mitigation strategies

## บทที่ 7: Advanced Generative AI

Participants understand when and how to fine-tune a model, and explore multimodal generation (text-to-image, text-to-speech) at the API level.

> **Scope note:** Fine-tuning in บทนี้ means parameter-efficient methods (LoRA / QLoRA) runnable on Google Colab -- full GPU training is out of scope. Participants who want to go deeper are pointed to Hugging Face PEFT documentation.

**Lecture (1 hr)**

1. Fine-tuning vs. prompting vs. RAG -- choosing the right adaptation strategy
2. Parameter-efficient fine-tuning -- LoRA and QLoRA concepts; cost and data requirements
3. Multimodal models -- text-to-image (Stable Diffusion), text-to-speech APIs

**Workshop (1.5-2 hr)**

1. Fine-tuning demo: adapt a small model on a custom dataset with PEFT/LoRA on Colab
2. Text-to-speech exercise: generate audio with an open TTS API
3. Stable Diffusion prompt exploration: compare outputs across prompt variations

## บทที่ 8: Agentic AI & RAG Fundamentals

Participants build their first AI agent that can retrieve information from documents and answer questions -- the pattern used in most real-world production AI tools today.

**Lecture (1 hr)**

1. What is Agentic AI? -- autonomous decision-making, tool use, memory, planning
2. RAG (Retrieval-Augmented Generation) -- why it matters and how it works (embed > store > retrieve > generate)
3. Frameworks overview -- LangChain and LlamaIndex: when to use each

**Workshop (1.5-2 hr)**

1. Build a RAG pipeline: load PDFs > chunk > embed > store in a vector DB (Chroma or FAISS)
2. Wire an LLM to answer questions from the retrieval results
3. Demo: query an internal document and compare RAG vs. plain LLM accuracy

## บทที่ 9: Multi-Agent Systems & Automation

Participants orchestrate multiple agents that collaborate, call external APIs, and trigger automated workflows -- bridging AI with existing IT systems.

**Lecture (1 hr)**

1. Multi-agent collaboration -- roles, handoffs, and shared memory
2. Tool use and API integration -- giving agents access to databases, calendars, ticketing systems
3. Automation patterns -- event-driven triggers, human-in-the-loop checkpoints, error recovery

**Workshop (1.5-2 hr)**

1. Build a research agent: search the web > summarize > store results
2. Automation demo: agent monitors a data source and sends an alert email on threshold breach
3. Discuss: failure modes, reliability, and how to add human approval steps

## บทที่ 10: Capstone Project

Each participant (or pair) presents a working Agentic AI system built for a real use case from their own domain -- the course's primary deliverable.

**Lecture / Briefing (30 min)**

1. Recap: from AI fundamentals to agentic systems -- the full-course arc
2. Project guidelines and grading rubric (functionality, code quality, presentation, responsible AI consideration)
3. Example capstone ideas:

- DevOps Assistant: monitors logs and opens tickets automatically (Agent + API + Automation)
- Internal Knowledge Bot: answers HR/IT questions from company docs (RAG + LLM)
- Data Analyst Agent: reads a CSV and generates insights + charts (ML + GenAI + Tool use)
- Marketing Copy Generator: drafts content by brand voice from a brief (Fine-tuning + Prompting)

**Workshop / Presentation (1.5 hr)**

1. Project work time with instructor and peer feedback
2. Live demos: each team presents their agent (5 min demo + 3 min Q&A)
3. Group reflection: what worked, what you would do differently, what comes next

## Notes for Instructors

**Pacing and depth**

- บทที่ 8-9 (RAG and multi-agent) are where the course pays off. Budget extra time here if the schedule allows.

**Tools and environment**

- บทที่ 1: participants need GitHub Copilot enabled in their editor (VS Code or JetBrains) before class -- confirm licenses/access ahead of time
- บทที่ 2 onward: Cline (VS Code extension) connected to the course's model/API key, used as the primary AI assistant for the rest of the course
- บทที่ 3: additionally requires the GSD plugin (Claude Code) and GitHub Spec Kit (`specify` CLI) installed
- บทที่ 5: requires an MCP Host (e.g. Claude Desktop) installed, plus a Python 3.10+/`uv` or Node.js 18+ environment for the MCP SDK
- Default environment: Google Colab (free tier is sufficient through บทที่ 6; Colab Pro recommended for บทที่ 7 fine-tuning)
- บทที่ 6 onward: participants need API keys for at least one LLM provider (OpenAI or Anthropic Claude) -- Q&A chatbot exercise in บทที่ 6 is the first hard requirement
- Vector DB for บทที่ 8: Chroma (local, zero setup) is recommended; FAISS as an alternative

**Responsible AI thread**

Do not treat responsible AI as a standalone topic. Weave it in:

- บทที่ 1: hallucination and bias intro
- บทที่ 6: evaluating LLM outputs
- บทที่ 10: capstone rubric includes a responsible AI consideration section

**Capstone evaluation rubric**

- Functionality (agent works end-to-end): 40%
- Code quality and documentation: 25%
- Presentation clarity: 20%
- Responsible AI consideration: 15%
