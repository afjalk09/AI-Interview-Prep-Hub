# Agent Architecture & Core Components - Interview Questions and Answers

This document contains common interview questions asked for AI Agent,
Generative AI, LLM Engineer, and Agentic AI roles.

------------------------------------------------------------------------

# Table of Contents

1.  AI Agent Architecture
2.  Core Components
3.  Planning
4.  Memory
5.  Tool Calling
6.  Reasoning
7.  Reflection
8.  Agent Loop
9.  Architecture Design Questions
10. Rapid Fire Questions

------------------------------------------------------------------------

# 1. What is AI Agent Architecture?

## Interview Question

> What is AI Agent Architecture?

## Answer

AI Agent Architecture is the overall design that defines how an AI agent
receives a goal, reasons about it, plans the required steps, uses tools,
stores memory, executes actions, and produces a final response.

Typical architecture:

``` text
User
 │
 ▼
Goal / Prompt
 │
 ▼
Planning
 │
 ▼
LLM
 ├──────────────┐
 ▼              ▼
Memory      Tool Calling
 │              │
 ▼              ▼
Database      APIs
      │
      ▼
Observation
      │
      ▼
Reflection
      │
      ▼
Final Response
```

------------------------------------------------------------------------

# 2. What are the core components of an AI Agent?

## Answer

An AI Agent generally consists of:

-   LLM (Reasoning Engine)
-   Planning Module
-   Memory
-   Tool Calling
-   Reasoning
-   Reflection
-   Executor
-   Observation Module

Each component performs a specific responsibility to complete complex
tasks.

------------------------------------------------------------------------

# 3. Why is the LLM called the brain of an AI Agent?

## Answer

The LLM is responsible for understanding user intent, reasoning about
the problem, selecting tools, generating plans, and producing natural
language responses. It does not execute actions directly but decides
what actions should be taken.

------------------------------------------------------------------------

# 4. What is Planning?

## Answer

Planning is the process of breaking a complex goal into smaller
executable tasks.

Example:

Goal:

``` text
Plan my vacation.
```

Planning:

``` text
Search Flights
      ↓
Find Hotels
      ↓
Check Weather
      ↓
Estimate Budget
      ↓
Create Itinerary
```

Planning makes execution more reliable and organized.

------------------------------------------------------------------------

# 5. Why is planning important?

## Answer

Planning helps the agent:

-   Break down complex problems.
-   Execute tasks in order.
-   Reduce unnecessary tool calls.
-   Recover from failures.
-   Improve accuracy.

------------------------------------------------------------------------

# 6. What is Memory?

## Answer

Memory enables an AI agent to remember information across one or
multiple interactions.

Types:

### Short-Term Memory

Conversation history within the current session.

### Long-Term Memory

Persistent user preferences, facts, or knowledge.

### Working Memory

Temporary information used while solving the current task.

------------------------------------------------------------------------

# 7. Difference between Working Memory and Long-Term Memory?

## Answer

  Working Memory          Long-Term Memory
  ----------------------- ----------------------
  Temporary               Persistent
  Used during execution   Used across sessions
  Cleared after task      Stored permanently

------------------------------------------------------------------------

# 8. What is Tool Calling?

## Answer

Tool Calling allows an AI agent to interact with external systems such
as:

-   REST APIs
-   SQL Databases
-   Search Engines
-   Python
-   Email Services
-   Calendar
-   File System

Example Flow:

``` text
User
 ↓
LLM
 ↓
Weather API
 ↓
Temperature
 ↓
LLM
 ↓
Answer
```

------------------------------------------------------------------------

# 9. How does an AI Agent decide which tool to use?

## Answer

The LLM analyzes the user's request, available tool descriptions, and
required information. It selects the tool whose capability best matches
the task. After receiving the tool output, it decides whether another
tool or reasoning step is needed.

------------------------------------------------------------------------

# 10. What is Reasoning?

## Answer

Reasoning is the process of analyzing information, comparing options,
making decisions, and selecting the next action.

Example:

User asks:

"Which laptop is better under ₹70,000?"

The agent compares specifications before making a recommendation.

------------------------------------------------------------------------

# 11. What is Reflection?

## Answer

Reflection is the process of evaluating previous actions before
continuing.

It helps the agent answer questions like:

-   Did the task succeed?
-   Is more information needed?
-   Should another tool be used?
-   Has the user's goal been achieved?

------------------------------------------------------------------------

# 12. Explain the Agent Loop.

## Answer

Most AI agents follow this execution cycle:

``` text
Receive Goal
      ↓
Think
      ↓
Plan
      ↓
Choose Tool
      ↓
Execute
      ↓
Observe Result
      ↓
Reflect
      ↓
Need More Work?
      ↓
Yes → Repeat
No  → Return Final Answer
```

------------------------------------------------------------------------

# 13. What happens if a tool fails?

## Answer

A well-designed AI agent should:

-   Detect the failure.
-   Analyze the reason.
-   Retry if appropriate.
-   Use an alternative tool if available.
-   Inform the user when necessary.

------------------------------------------------------------------------

# 14. Single-Agent vs Multi-Agent

## Answer

### Single Agent

One agent performs every task.

Advantages: - Easy to build - Lower cost - Simple debugging

### Multi-Agent

Multiple specialized agents collaborate.

Example:

``` text
Manager Agent
      │
 ├─────────────┐
 ▼             ▼
Research    Coding
      │
      ▼
Reviewer
```

Advantages: - Better scalability - Specialized expertise - Parallel
execution

------------------------------------------------------------------------

# 15. Design Question

## Interview Question

Design an AI Travel Planner.

## Sample Answer

Architecture:

``` text
User Goal
     ↓
Planner
     ↓
Weather API
     ↓
Flight API
     ↓
Hotel API
     ↓
Budget Calculator
     ↓
Final Itinerary
```

The planner coordinates each service, gathers results, and generates a
complete travel plan.

------------------------------------------------------------------------

# Rapid Fire Questions

## Q. What is Agent Architecture?

Design of components that work together to accomplish user goals.

## Q. What is Planning?

Breaking a goal into smaller executable tasks.

## Q. What is Memory?

Storage of information for current or future interactions.

## Q. What is Tool Calling?

Using external systems such as APIs and databases.

## Q. What is Reflection?

Evaluating previous actions before continuing.

## Q. What is the Agent Loop?

Think → Plan → Execute → Observe → Reflect → Repeat.

## Q. Why do AI Agents need Memory?

To maintain context, personalize responses, and complete multi-step
tasks.

## Q. Name the core components of an AI Agent.

LLM, Planning, Memory, Tool Calling, Reasoning, Reflection, Executor.

------------------------------------------------------------------------

# Interview Tips

-   Explain concepts with diagrams whenever possible.
-   Use practical examples (travel planner, coding assistant, customer
    support).
-   Clearly distinguish LLM capabilities from AI Agent capabilities.
-   Mention planning, memory, and tool calling in most architecture
    answers.
