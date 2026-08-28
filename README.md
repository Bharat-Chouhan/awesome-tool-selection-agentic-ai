# Awesome Tool Selection in Multi-Tool Agentic AI Systems

A curated and research-oriented collection of papers, datasets, tools, GitHub implementations, and learning resources related to **tool selection in multi-tool Agentic AI systems**.

The main goal of this repository is to help researchers understand, implement, and evaluate how an AI agent decides **which tool to use, when to use it, how to call it, and how to select a sequence of tools** when multiple tools are available.

---

## Contents

- [Overview](#overview)
- [Why Tool Selection Matters](#why-tool-selection-matters)
- [AI-Assisted Research Paper](#ai-assisted-research-paper)
- [Citation Integrity Audit](#citation-integrity-audit)
- [Research Papers](#research-papers)
  - [Survey and Review Papers](#survey-and-review-papers)
  - [Foundational Papers](#foundational-papers)
  - [Tool Learning and Function Calling](#tool-learning-and-function-calling)
  - [Tool Selection and Retrieval](#tool-selection-and-retrieval)
  - [Planning and Decision Making](#planning-and-decision-making)
  - [Evaluation and Benchmarks](#evaluation-and-benchmarks)
  - [Recent Research](#recent-research)
- [Datasets and Benchmarks](#datasets-and-benchmarks)
- [Tools and Libraries](#tools-and-libraries)
- [GitHub Implementations](#github-implementations)
- [Tutorials and Learning Resources](#tutorials-and-learning-resources)
- [Evaluation Metrics](#evaluation-metrics)
- [Suggested Research Workflow](#suggested-research-workflow)
- [Curation and Verification Policy](#curation-and-verification-policy)
- [Repository Structure](#repository-structure)
- [License](#license)

---

## Overview

### What is Multi-Tool Agentic AI?

An Agentic AI system is an AI system that can interpret a user's task, reason about what needs to be done, choose actions, use external tools, observe their results, and continue until the task is completed.

A **multi-tool agent** has access to several possible tools. These tools may include search engines, calculators, databases, code interpreters, APIs, retrieval systems, weather services, file systems, or other specialized functions.

For example, consider an agent with these tools:

```text
Calculator
Search Engine
Weather API
Database
Translator
```

If the user asks:

> "What is the temperature in Delhi today?"

the agent should select the **Weather API**, rather than the Calculator or Translator.

Therefore, an important research question is:

> **How accurately can an AI agent select the correct tool from a set of available tools?**

### What is Tool Selection?

Tool selection is the decision-making process through which an AI agent identifies the most appropriate tool or sequence of tools for a given task.

A simplified pipeline is:

```text
User Task
    ↓
Understand the Task
    ↓
Identify Required Capability
    ↓
Retrieve / Consider Candidate Tools
    ↓
Select Tool
    ↓
Generate Tool Arguments
    ↓
Execute Tool
    ↓
Observe Result
    ↓
Select Next Tool (if required)
    ↓
Generate Final Answer
```

Tool selection should be evaluated separately from final-answer quality because an agent can sometimes produce a correct-looking answer even after choosing an inappropriate tool.

---

## Why Tool Selection Matters

Modern AI agents increasingly interact with external tools and APIs. As the number of available tools increases, selecting the correct tool becomes more difficult.

Important challenges include:

- Large numbers of candidate tools
- Similar or overlapping tool descriptions
- Ambiguous user instructions
- Incorrect or incomplete tool descriptions
- Multi-step tasks requiring several tools
- Dependencies between tool calls
- Incorrect tool arguments
- Noisy or misleading tool information
- Choosing whether a tool is required at all
- Maintaining state across multiple tool calls

A good evaluation system should therefore measure more than whether the final answer is correct.

---

## AI-Assisted Research Paper

### Paper Title

**Evaluating Tool-Selection Accuracy in Multi-Tool Agentic AI Systems**

This paper provides the starting point for this repository and connects the earlier AI-assisted research activity with the present GitHub curation activity.

The paper discusses the problem of evaluating whether an AI agent selects appropriate tools when several tools are available.

**Paper:** [View AI-Assisted Research Paper](paper/AI_Assisted_Research_Paper.pdf)

---

## Citation Integrity Audit

The citation-integrity audit was conducted to verify the scholarly references used during the earlier research activity.

The verification process checks:

- Paper title
- Authors
- Publication year
- Journal or conference
- DOI or persistent identifier
- Existence of the paper
- Whether the supplied link points to the claimed paper
- Relevance of the paper to the research topic

The main lesson is:

> **AI can help discover candidate references, but references must be independently verified before being included in a research collection.**

**Audit:** [View Citation Integrity Audit](citation-audit/Citation_Integrity_Audit.pdf)

---

# Research Papers

The repository contains a curated collection of **20+ verified scholarly papers** related to tool learning, tool selection, API retrieval, planning, function calling, robustness, calibration, and agent evaluation.

The complete research-paper collection is maintained in:

**[references/references.md](references/references.md)**

Each paper should contain:

- **Paper title**
- Authors
- Year
- Journal / Conference / Proceedings
- DOI, arXiv, ACL Anthology, or another persistent identifier where available
- Link to the paper
- One-line explanation of relevance

---

## Survey and Review Papers

Survey papers provide an overview of the field and are useful for understanding terminology, major approaches, datasets, and evaluation methods.

### 1. Tool Learning with Large Language Models: A Survey

**Authors:** Changle Qu et al.  
**Year:** 2024

Provides a systematic overview of tool learning, including task planning, tool selection, tool calling, response generation, and evaluation.

[Paper](https://arxiv.org/abs/2405.17935)

---

## Foundational Papers

### 1. ReAct: Synergizing Reasoning and Acting in Language Models

**Authors:** Shunyu Yao et al.  
**Year:** 2023

Introduces an approach that combines reasoning and actions in interactive environments, forming an important foundation for agentic tool use.

[Paper](https://arxiv.org/abs/2210.03629)

### 2. Toolformer: Language Models Can Teach Themselves to Use Tools

**Authors:** Timo Schick et al.  
**Year:** 2023

Studies how language models can learn to use external APIs and make decisions about when and how to call tools.

[Paper](https://arxiv.org/abs/2302.04761)

---

## Tool Learning and Function Calling

### ToolLLM: Facilitating Large Language Models to Master 16000+ Real-world APIs

**Authors:** Yujia Qin et al.  
**Year:** 2023

Introduces large-scale tool learning and the ToolBench ecosystem for training and evaluating models on many real-world APIs.

[Paper](https://arxiv.org/abs/2307.16789)

### API-Bank: A Comprehensive Benchmark for Tool-Augmented LLMs

**Year:** 2023

Provides a benchmark for studying tool-augmented language models and API usage.

[Paper](https://aclanthology.org/2023.emnlp-main.187/)

---

## Tool Selection and Retrieval

### AnyTool: Self-Reflective, Hierarchical Agents for Large-Scale API Calls

**Authors:** Yu Du et al.  
**Year:** 2024

Studies hierarchical API retrieval and self-reflection for agents operating over large tool collections.

[Paper](https://proceedings.mlr.press/v235/du24h.html)

### ToolGen: Unified Tool Retrieval and Calling via Generation

**Year:** 2024

Investigates unified tool retrieval and calling for large tool collections.

[Paper](https://arxiv.org/abs/2410.03439)

### ToolNet: Connecting Large Language Models with Massive Tools via Tool Graph

**Year:** 2024

Uses a tool-graph structure to organize and navigate large collections of tools.

[Paper](https://arxiv.org/abs/2403.00839)

---

## Planning and Decision Making

### ToolPlanner: A Tool Augmented LLM for Multi Granularity Instructions with Path Planning and Feedback

**Year:** 2024

Studies path planning and feedback for multi-step tool-augmented tasks.

[Paper](https://aclanthology.org/2024.emnlp-main.1018/)

---

## Evaluation and Benchmarks

Evaluation is the most important category for this repository because the research topic specifically concerns **tool-selection accuracy**.

### The Berkeley Function Calling Leaderboard (BFCL)

**Year:** 2025

Evaluates function calling and tool-use behavior, including more complex multi-step and agentic settings.

[Paper](https://proceedings.mlr.press/v267/patil25a.html)

### T-Eval: Evaluating the Tool Utilization Capability of Large Language Models Step by Step

**Year:** 2024

Provides fine-grained evaluation of different stages of tool utilization.

[Paper](https://aclanthology.org/2024.acl-long.515/)

### RoTBench

**Year:** 2024

Evaluates robustness in tool learning, including tool selection and parameter identification under noisy conditions.

[Paper](https://aclanthology.org/2024.emnlp-main.19/)

### ToolSandbox

**Year:** 2025

Provides a stateful, conversational and interactive benchmark for evaluating LLM tool-use capabilities.

[Paper](https://aclanthology.org/2025.findings-naacl.65/)

### AgentBench

**Year:** 2023

Evaluates language models as agents across multiple environments.

[Paper](https://arxiv.org/abs/2308.03688)

### GAIA

**Year:** 2024

Evaluates general AI assistants on real-world tasks involving reasoning and tool use.

[Paper](https://proceedings.iclr.cc/paper_files/paper/2024/hash/25ae35b5b1738d80f1f03a8713e405ec-Abstract-Conference.html)

---

## Recent Research

The repository also tracks newer work related to:

- Large-scale API retrieval
- Agentic function calling
- Stateful tool use
- Multi-turn tool selection
- Tool-use robustness
- Tool-use calibration
- Multi-agent tool selection
- Code-based tool learning
- Complex planning and execution

The complete and expanded list is available in **[references/references.md](references/references.md)**.

---

# Datasets and Benchmarks

Datasets and benchmarks are important for reproducible evaluation.

See the detailed collection:

**[datasets/datasets.md](datasets/datasets.md)**

Recommended resources include:

### 1. Berkeley Function Calling Leaderboard (BFCL)

Evaluates function/tool calling across different levels of complexity.

**Use:** Measuring function-call and tool-selection accuracy.

### 2. API-Bank

A benchmark for tool-augmented LLMs.

**Use:** Studying API retrieval, planning and tool calling.

### 3. ToolBench

Large-scale tool-learning resource containing many real-world APIs and tool-use tasks.

**Use:** Studying tool selection and retrieval when many candidate tools are available.

### 4. ToolTalk

Conversational tool-use benchmark with reference tool sequences.

**Use:** Evaluating tool selection across multi-turn conversations.

### 5. ToolSandbox

Stateful and interactive tool-use benchmark.

**Use:** Evaluating tool selection when tool choices depend on previous state and intermediate results.

---

# Tools and Libraries

See the complete collection:

**[tools/tools.md](tools/tools.md)**

### 1. LangGraph

Framework for building stateful and controllable agent workflows.

**Use in this research:** Implement explicit tool-routing and multi-step agent workflows.

### 2. LangChain

Framework for building LLM applications, tools and agents.

**Use in this research:** Create baseline multi-tool agents.

### 3. Microsoft AutoGen

Framework for building multi-agent and tool-enabled applications.

**Use in this research:** Study tool selection in collaborative agent systems.

### 4. LlamaIndex

Framework for agentic applications and data/tool integration.

**Use in this research:** Build agents that interact with external data and tools.

### 5. DSPy

Framework for programming and optimizing language-model pipelines.

**Use in this research:** Experiment with systematic optimization and evaluation of agent components.

---

# GitHub Implementations

See the detailed implementation collection:

**[implementations/github-repositories.md](implementations/github-repositories.md)**

Repositories should be selected based on:

- Documentation quality
- Source-code availability
- Recent activity
- Examples
- Reproducibility
- License
- Connection to a research paper or recognized project

Recommended implementation categories include:

### ToolBench / ToolLLM

Large-scale tool-learning ecosystem for real-world APIs.

[GitHub](https://github.com/OpenBMB/ToolBench)

### AnyTool

Hierarchical API retrieval and tool-use system.

[GitHub](https://github.com/dyabel/AnyTool)

### ToolTalk

Conversational tool-use benchmark implementation.

[GitHub](https://github.com/microsoft/tooltalk)

### RoTBench

Implementation/resources for robustness evaluation in tool learning.

[GitHub](https://github.com/Junjie-Ye/RoTBench)

### UltraTool

Research implementation associated with comprehensive tool-utilization evaluation.

[GitHub](https://github.com/JoeYing1019/UltraTool)

---

# Tutorials and Learning Resources

See:

**[tutorials/tutorials.md](tutorials/tutorials.md)**

Recommended learning resources:

1. **LangGraph Documentation** — Learn stateful agent workflows and orchestration.
2. **LangChain Documentation** — Learn tools, agents and retrieval patterns.
3. **OpenAI Function Calling Documentation** — Understand tool schemas, function calls and tool results.
4. **Anthropic Tool Use Documentation** — Understand tool definitions, calls and result handling.
5. **Hugging Face Agents Course** — Learn the foundations of AI agents and tool use.

---

# Evaluation Metrics

Tool selection should be evaluated using multiple metrics.

| Metric | What it measures |
|---|---|
| Tool Selection Accuracy | Whether the correct tool was selected |
| Top-k Tool Retrieval Recall | Whether the correct tool appears in the top k retrieved tools |
| Argument Accuracy | Whether correct parameters were generated |
| Tool Call Success Rate | Whether the selected tool was successfully executed |
| Sequence Accuracy | Whether the complete tool sequence is correct |
| State-dependent Success | Whether tool selection remains correct when previous state matters |
| Robustness | Whether tool selection remains correct under noise or perturbations |
| Abstention Accuracy | Whether the agent correctly decides that no tool should be used |

### Basic Tool Selection Accuracy

A simple metric is:

```text
Tool Selection Accuracy
=
Correct Tool Selections / Total Evaluation Tasks
```

For example, if an agent selects the correct tool for 90 out of 100 tasks:

```text
Tool Selection Accuracy = 90 / 100 = 90%
```

---

# Suggested Research Workflow

A researcher can use this repository to follow the workflow below:

```text
1. Understand Agentic AI
        ↓
2. Understand Tool Calling
        ↓
3. Study Tool Selection
        ↓
4. Study Tool Retrieval
        ↓
5. Study Planning
        ↓
6. Select a Benchmark
        ↓
7. Build a Multi-Tool Agent
        ↓
8. Record Tool Decisions
        ↓
9. Compare Decisions with Expected Tools
        ↓
10. Calculate Evaluation Metrics
        ↓
11. Analyze Failure Cases
        ↓
12. Improve Tool Selection
```

### Example Experiment

Assume an agent has five tools:

```text
Calculator
Search
Weather
Database
Translator
```

Give the agent 100 tasks.

For every task, record:

```text
Task
Available Tools
Expected Tool
Selected Tool
Arguments
Tool Result
Selection Correct?
Final Answer
```

Then calculate:

```text
Selection Accuracy
Argument Accuracy
Tool Call Success Rate
Sequence Accuracy
```

This separates **tool-selection performance** from the quality of the final answer.

---

# Curation and Verification Policy

This repository follows a verification-first approach.

Before adding a scholarly paper, check:

- Correct title
- Correct authors
- Correct publication year
- Correct venue
- DOI or persistent identifier
- Whether the paper actually exists
- Whether the provided link points to the same paper
- Whether the paper is genuinely relevant to tool selection, tool learning, planning, tool calling, or agent evaluation

### Core Principle

> **AI may help discover resources, but every important resource should be independently verified before inclusion.**

The repository does not intentionally include fabricated references.

For GitHub projects, the selection process also considers:

- Documentation
- Code availability
- Maintenance/activity
- Examples
- Reproducibility
- License
- Research relevance

---

# Copyright and Ethical Use

This repository contains curated research information and links.

External research papers should normally be linked to their official publisher, DOI, ACL Anthology, arXiv, or other authorized open-access source rather than copied into this repository.

Only material that can legally be redistributed should be uploaded.

The original student assignment paper and citation audit may be included as course/project material.

---

# Repository Structure

```text
awesome-tool-selection-agentic-ai/
│
├── README.md
│
├── paper/
│   └── AI_Assisted_Research_Paper.pdf
│
├── citation-audit/
│   └── Citation_Integrity_Audit.pdf
│
├── references/
│   └── references.md
│
├── datasets/
│   └── datasets.md
│
├── tools/
│   └── tools.md
│
├── implementations/
│   └── github-repositories.md
│
└── LICENSE
```

---

# Repository Goals

This repository aims to:

1. Provide a structured introduction to tool selection in Agentic AI.
2. Collect verified research papers in one place.
3. Organize research according to major subtopics.
4. Provide datasets and benchmarks for reproducible evaluation.
5. Identify useful tools and libraries.
6. Collect high-quality GitHub implementations.
7. Provide learning resources for new researchers.
8. Encourage citation verification and responsible research curation.
9. Provide a starting point for future research on tool-selection accuracy.

---

# How to Contribute

This repository is currently maintained as an academic research-curation project.

When adding a resource:

1. Verify the source.
2. Confirm the resource is relevant.
3. Add it to the appropriate category.
4. Include a short description.
5. Include an official source link.
6. Avoid duplicate resources.
7. Check that the link works.
8. Update the README if a major category changes.

---

# Acknowledgement

This repository was developed as part of the **AI Tools for Research** GitHub Research Curation and Documentation activity.

The repository extends an earlier AI-assisted research activity into a verified and organized research resource.

---

# License

The original material in this repository is provided under the license specified in [LICENSE](LICENSE).

External papers, datasets, software projects, and documentation remain subject to their respective licenses and terms.

---

## Status

**Research Topic:** Evaluating Tool-Selection Accuracy in Multi-Tool Agentic AI Systems

**Repository Type:** Academic Awesome-Style Research Repository

**Focus:** Agentic AI · Tool Selection · Tool Learning · Function Calling · API Retrieval · Planning · Evaluation · Benchmarks
