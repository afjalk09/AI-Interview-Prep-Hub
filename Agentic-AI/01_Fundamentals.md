# Fundamentals of Agentic AI

This guide covers the fundamental concepts of Agentic AI that are commonly asked in interviews. It is intended for beginners as well as experienced developers preparing for AI Agent, LLM Engineer, or Generative AI interviews.

---

# Table of Contents

1. What is Agentic AI?
2. AI Agent vs Traditional AI
3. AI Agent vs LLM
4. AI Agent vs RAG
5. Characteristics of an AI Agent
6. Components of an AI Agent
7. Agent Lifecycle
8. Types of AI Agents
9. Common Interview Questions

---

# 1. What is Agentic AI?

## Interview Question

> What is Agentic AI?

## Answer

Agentic AI refers to AI systems that can **autonomously plan, reason, make decisions, use tools, and execute tasks** to accomplish a specific goal with minimal human intervention.

Unlike traditional chatbots that simply generate responses, AI agents are capable of performing multiple actions, interacting with external systems, and adapting their behavior based on observations.

### Example

**User Request**

> Find the cheapest flight from Mumbai to Bangalore for tomorrow and email me the itinerary.

A traditional chatbot may provide flight suggestions.

An AI agent can:

* Search flight APIs
* Compare prices
* Select the cheapest option
* Ask for confirmation
* Book the ticket
* Send the itinerary via email

---

# 2. AI Agent vs Traditional AI

| Traditional AI            | AI Agent                                |
| ------------------------- | --------------------------------------- |
| Rule-based                | Goal-driven                             |
| Executes predefined logic | Plans dynamically                       |
| No reasoning              | Performs reasoning                      |
| Limited memory            | Can maintain memory                     |
| No tool usage             | Can use APIs, databases, search engines |
| Passive                   | Autonomous                              |

---

# 3. AI Agent vs Large Language Model (LLM)

Many interviewers ask this question.

## Large Language Model

An LLM predicts the next token based on the provided context.

Examples include GPT, Claude, Gemini, and Llama.

An LLM:

* Generates text
* Answers questions
* Summarizes documents
* Translates languages

It **does not inherently**:

* Plan tasks
* Call APIs
* Access databases
* Execute code
* Maintain long-term memory

---

## AI Agent

An AI Agent **uses an LLM as its reasoning engine** while adding capabilities such as:

* Planning
* Memory
* Tool Calling
* Decision Making
* Workflow Execution

Think of it like this:

```
LLM
 ↓
Brain

AI Agent
 ↓
Brain + Memory + Tools + Planning + Actions
```

---

# 4. AI Agent vs RAG

## RAG (Retrieval-Augmented Generation)

RAG improves LLM responses by retrieving relevant information before generating an answer.

Typical workflow:

```
User Question
      ↓
Retriever
      ↓
Vector Database
      ↓
Relevant Documents
      ↓
LLM
      ↓
Answer
```

---

## AI Agent

An AI Agent can:

* Retrieve information
* Decide what to do next
* Call multiple tools
* Perform calculations
* Execute workflows
* Re-plan when something fails

RAG is often one component inside an AI agent.

---

# 5. Characteristics of an AI Agent

A good interview answer should mention these characteristics.

* Goal-Oriented
* Autonomous
* Adaptive
* Uses External Tools
* Performs Reasoning
* Maintains Memory
* Supports Planning
* Learns from Observations

---

# 6. Components of an AI Agent

A typical AI agent consists of the following components:

```
                User
                  │
                  ▼
           Prompt / Goal
                  │
                  ▼
          Planning Module
                  │
                  ▼
              LLM Engine
                  │
        ┌─────────┴─────────┐
        ▼                   ▼
     Memory             Tool Calling
        │                   │
        ▼                   ▼
 Vector DB         APIs / Search / Database
        │                   │
        └─────────┬─────────┘
                  ▼
             Final Response
```

### Core Components

## 1. LLM

Responsible for reasoning and language generation.

---

## 2. Memory

Stores information across interactions.

Examples:

* Conversation history
* User preferences
* Long-term knowledge

---

## 3. Planning

Breaks complex goals into smaller executable tasks.

Example:

Goal:

```
Plan my vacation.
```

Planning:

* Find destinations
* Compare prices
* Book flights
* Reserve hotel
* Create itinerary

---

## 4. Tool Calling

Allows the agent to interact with external systems.

Examples:

* Search engines
* REST APIs
* SQL databases
* Python
* Email services
* Calendars

---

## 5. Reasoning

Determines:

* What to do
* Which tool to use
* Whether another step is needed

---

# 7. Agent Lifecycle

Most interviewers expect candidates to explain the complete workflow.

```
User Request
      │
      ▼
Understand Intent
      │
      ▼
Plan Tasks
      │
      ▼
Select Tools
      │
      ▼
Execute Actions
      │
      ▼
Observe Results
      │
      ▼
Reason Again
      │
      ▼
Generate Final Response
```

---

# 8. Types of AI Agents

## Reactive Agent

* No memory
* Reacts only to current input

Example:

A calculator.

---

## Goal-Based Agent

Works toward achieving a predefined objective.

Example:

Travel booking assistant.

---

## Utility-Based Agent

Chooses the action with the highest expected benefit.

Example:

Investment advisor selecting the best portfolio.

---

## Learning Agent

Improves performance over time using feedback.

Example:

Recommendation systems.

---

## Multi-Agent System

Multiple agents collaborate to solve a problem.

Example:

```
Planner Agent
      │
      ▼
Research Agent
      │
      ▼
Coding Agent
      │
      ▼
Reviewer Agent
```

---

# 9. Common Interview Questions

### Beginner

* What is Agentic AI?
* What is an AI Agent?
* AI Agent vs LLM?
* AI Agent vs RAG?
* Explain Tool Calling.
* Explain Planning.
* What is Memory?
* What are AI Agent components?

---

### Intermediate

* Explain the ReAct framework.
* What is Model Context Protocol (MCP)?
* How do AI agents use memory?
* What is reflection in AI agents?
* How do AI agents decide which tool to call?
* What is Human-in-the-Loop (HITL)?

---

### Advanced

* How would you build an autonomous customer support agent?
* How do you evaluate AI agents?
* How do you prevent hallucinations?
* How would you monitor AI agents in production?
* How do you debug an AI agent?

---

# Key Takeaways

* An AI Agent is more than just an LLM.
* Planning, reasoning, memory, and tool usage are the core capabilities of modern AI agents.
* RAG provides knowledge retrieval, while agents add autonomy and decision-making.
* Most production AI systems combine LLMs, RAG, memory, planning, and tool calling to build reliable autonomous workflows.
* Understanding these fundamentals is essential for technical interviews involving Agentic AI.
