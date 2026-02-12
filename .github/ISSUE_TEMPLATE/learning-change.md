---
name: Learning / Change (Agent Service + MCP)
about: Track a learning-driven change, experiment, or feature while working through WRK540
title: "[Learning] <short, clear title>"
labels: ["learning"]
assignees: []
---

## Context
- **Workshop / Lab**: WRK540 – Unlock Your Agents’ Potential with MCP
- **Area**: Agent Service / MCP / PostgreSQL / RLS / Deployment / Other
- **Mode**:
  - [ ] Copilot Agent Mode
  - [ ] Copilot (suggestions only)
  - [ ] No Copilot

## Goal
What are you trying to learn or validate with this change?

> Example: Understand how the agent behaves when an MCP tool returns no results due to RLS.

## Approach
Briefly describe how you plan to explore or implement this.

- What will you change?
- Where (files / folders)?
- Why this approach?

## Changes (High-Level)
List *what* changed (not full code).

- Agent instructions updated to clarify empty MCP responses
- MCP tool contract clarified (inputs / outputs)
- SQL query adjusted to rely fully on RLS

## Agent + MCP Considerations
- **Agent behavior impact**:
  - How does this affect reasoning, tool selection, or failure modes?
- **MCP tool contract**:
  - Single responsibility?
  - Expected inputs / outputs?
  - What happens on empty or partial results?

## Security & Platform Constraints
- **RLS impact**:  
  Does Row Level Security affect visibility or results?
- **Platform constraints**:  
  Any Agent Service / model / deployment limitations discovered?

## What I Learned
Capture *specific* insights (not generic).

> Example:
> - Agent Service does not retry MCP tools automatically.
> - Empty results are valid outcomes, not errors.
> - Security boundaries belong in the database, not agent logic.

## Customer / Demo Takeaway
How would you explain this learning to:
- a customer?
- a teammate?
- a workshop audience?

## Open Questions / Next Steps
Anything still unclear or worth exploring later?

- [ ] Follow-up experiment
- [ ] Document in README
- [ ] Convert to demo talking point

## Learning Log
- [ ] Entry added to `LEARNING_LOG.md`
- Date:
- Summary (1–2 lines):