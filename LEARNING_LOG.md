# Learning Log – WRK540 (Agent Service + MCP)

This log tracks **intentional learning** while working through the  
**Microsoft AI Tour 2026 – WRK540: Unlock Your Agents’ Potential with Model Context Protocol (MCP)** workshop.

The goal is to capture:
- What changed
- Why it was changed
- What was learned about **Agent Service, MCP, PostgreSQL RLS, and platform constraints**
- How the learning translates to **customer demos, architecture decisions, and best practices**

Each entry maps to a GitHub Issue and a focused change (branch + commits).

---

## 📌 How to Use This Log

For **every meaningful change**:
1. Create a GitHub Issue (Learning / Feature / Experiment)
2. Create a branch from that issue
3. Implement the change (with or without Copilot Agent Mode)
4. Commit with intent-based messages
5. **Append one entry below**

---

## 🧠 Learning Entries

---

### 📅 Date:
**YYYY-MM-DD**

**Issue:** #<issue-number> – <short title>

**Area:**  
Agent Service | MCP | PostgreSQL / RLS | Deployment | Instructions | Other

**Mode:**  
Copilot Agent Mode / Manual (Copilot suggestions only) / No Copilot

---

### 🔧 What Changed
Brief, high-level summary (no code dump).

Example:
- Updated agent instructions to handle empty MCP tool responses
- Clarified MCP tool contract inputs/outputs
- Adjusted SQL query relying fully on PostgreSQL RLS

---

### 💡 What I Learned
Concrete insight(s). This is the most important section.

Example:
- Agent Service treats empty MCP responses as valid outcomes, not failures
- MCP enforces strict trust boundaries; agents must not “fill gaps”
- Security belongs at the database (RLS), not in agent logic
- Some models are available in Foundry playground but not deployable via Agent Service

---

### 🧩 Agent + MCP Insight
(Optional but recommended)

- How did the agent’s reasoning change?
- Did tool boundaries become clearer?
- Any hallucination or overreach risks identified?

---

### 🔐 Security / Platform Constraints
- RLS impact observed?
- Agent Service / model / region limitations discovered?
- Any constraints that would affect production design?

---

### 🎯 Customer / Demo Takeaway
How would you explain this learning to:
- A customer
- A teammate
- A workshop audience

Example:
> “MCP ensures agents can only act on what tools explicitly return—this is critical for enterprise trust.”

---

### ➡️ Next Steps / Open Questions
- Follow-up experiment?
- Document in README?
- Turn into a demo talking point?

---

---

## ✅ Patterns Emerging (Optional Section)

Use this section over time to summarize repeated learnings.

- Agents should **ask clarifying questions** rather than assume
- MCP tools should remain **stateless and minimal**
- RLS + MCP is a powerful enterprise boundary
- Platform constraints shape architecture more than code

---

## 🏁 Why This Matters

This log:
- Builds **agentic intuition**, not just code
- Creates reusable **customer-ready insights**
- Helps compare **Copilot Agent Mode vs manual reasoning**
- Turns workshop work into **architecture storytelling**
### Customer Takeaway
How this learning translates to a customer, stakeholder, or workshop audience:

- **What problem this solves:**  
  (e.g., Prevents agents from hallucinating when data is restricted or unavailable)

- **Why it matters to customers:**  
  (e.g., Ensures enterprise-grade trust, security, and predictable behavior in regulated environments)

- **How Microsoft’s approach helps:**  
  (e.g., Azure AI Foundry Agent Service + MCP enforce clear tool boundaries and governance)

- **One‑line customer explanation:**  
  “This design ensures the agent only answers using governed data sources and responds safely when data isn’t accessible.”

- **Where this shows up in demos / architecture reviews:**  
  (e.g., Agent asks clarifying questions instead of fabricating answers when MCP returns no data)
``