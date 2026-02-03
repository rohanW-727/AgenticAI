# AgenticAI

## Overview
Worked as Core AI Architect on a private project repository for UMD ACM’s Agentic AI system — a multi-tool LLM-driven agent framework enabling structured tool execution via chained LLM calls.

## My Responsibilities
- Contributed to system-level design discussions for a pre-existing agent execution loop developed by the project lead.
- Designed and implemented a short-term memory component for storing and retrieving recent queries and intermediate reasoning state.
- Integrated memory retrieval into the agent’s existing decision pipeline without modifying core execution semantics.

## Technical Details (Redacted)
- Memory sits in the request path before full agent reasoning: normalized query → memory lookup → hit/miss decision.
- On cache hit, Gemini is prompted to retrieve and return previously computed outputs or execution plans from memory rather than re-performing full reasoning.
- This reduces repeated reasoning and downstream tool execution while preserving agent behavior.
- Implemented lightweight indexing and retrieval for recent interactions; included logging instrumentation for latency evaluation.

## Results
- Reduced end-to-end agent latency by ~20% (1.25s → 1.01s) by avoiding repeated reasoning and tool execution through memory-based query reuse.

## What I Would Share If Public
- `agentic-logger` branch containing the memory module, integration points, and latency instrumentation.





