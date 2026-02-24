# Week 6 — Synthesis & Mastery

> *"The master has failed more times than the beginner has tried."*  
> *This week: pull everything together. Build something real. Articulate what you've learned.*

---

## BUILD: Your Capstone Agent

### Day 1-3: Build Something That Matters

**Exercise 6.1** — Capstone project:

Build an agent (or agent system) that solves a **real problem you actually have**. Not a tutorial exercise — something you would use tomorrow.

Ideas calibrated to your profile:

**Option A — Workshop Facilitator Agent**
An agent that helps you design and run workshops like the Human-AI Interaction session. It:
- Takes a topic and audience profile, designs the session structure
- Generates provocative questions for each segment
- Suggests exercises that mix philosophy, psychology, and practice
- Creates handout materials with the right voice (multilingual, multi-style)

**Option B — Philosophy-Code Bridge Agent**
An agent for your unique intersection. Given a coding pattern/decision, it:
- Identifies the philosophical principle behind it (separation of concerns ↔ stoic focus on what's in your control)
- Draws parallels to cognitive biases (premature optimization ↔ anchoring bias)
- Suggests approaches from unexpected traditions (Sufi "polishing the mirror" ↔ refactoring)

**Option C — Multi-Agent Code Dojo**
An orchestrated system of 4+ agents that conduct a comprehensive code review:
- Architect, Debugger, Clarity-Reviewer, Security-Auditor, Performance-Critic, and a Synthesizer that merges their perspectives into a single coherent review
- You as the orchestrator decide which agents to invoke based on the code

**Option D — Your own idea**
What problem would you love an agent to solve? Build it.

### Requirements (regardless of which option):
- Must include an agent.md with thoughtful instructions
- Must use at least 2 tools (file read, search, terminal, MCP, etc.)
- Must have explicit reasoning instructions (not just "do X" — "think about X before doing Y")
- Must have at least one guardrail (self-checking, confirmation, confidence level)
- Must be tested on 3+ real scenarios

**Exercise 6.2** — Write a project brief before building:
```
CAPSTONE: [name]
PROBLEM: What problem does this solve?
USER: Who is it for?
AGENTS: What agents are involved?
TOOLS: What tools do they need?
REASONING: How should they think?
GUARDRAILS: What should they NOT do?
SUCCESS: How will I know it works?
```

### Day 4: Review & Refine

**Exercise 6.3** — Self-review:

Use your Code-Reviewer, Architecture-Reviewer, and Debugger agents to review your capstone. Yes — use the agents you built to evaluate the agents you built. Meta-level feedback.

**Exercise 6.4** — Break it:
- What's the worst prompt you could give this agent?
- What happens with contradictory instructions?
- Where does it give up? Where should it give up but doesn't?
- Fix what you find.

---

## UNDERSTAND: Architecture Review

### Day 5: Map Everything You've Built

**Exercise 6.5** — Create your personal agent architecture diagram:

```
YOUR AGENT ECOSYSTEM
│
├── General Purpose
│   ├── AI-Professor         ← Teaching & explanation
│   └── Decision-Advisor     ← Thinking companion
│
├── Code Quality
│   ├── Code-Reviewer        ← Multi-perspective review
│   ├── Logic-Reviewer       ← Correctness focus
│   ├── Clarity-Reviewer     ← Readability focus
│   ├── Architecture-Reviewer← Design focus
│   └── Debugger             ← Hypothesis-driven debugging
│
├── Process
│   ├── Project-Planner      ← Task decomposition
│   ├── Orchestrator         ← Delegation & coordination
│   ├── Researcher           ← Information gathering
│   └── Writer               ← Documentation & reports
│
├── Safety
│   ├── Self-Checking-Coder  ← Verified output
│   ├── Safe-Executor        ← Cautious action
│   ├── Optimist             ← Opportunity lens
│   └── Critic               ← Risk lens
│
├── Capstone
│   └── [Your project]       ← Real-world application
│
└── Infrastructure
    ├── MCP Server(s)        ← Custom tools
    ├── Instruction files    ← Workspace context
    └── Journal              ← Your observations & philosophy
```

Adapt this to what you actually built. Some agents may have been combined or renamed. The map reflects YOUR learning journey.

**Exercise 6.6** — Principles you've learned:

Write 5-10 principles about agent design that you've discovered through practice. Not things you read — things you *know* because you tested them.

Example format:
> **Principle**: The agent.md description is the most important line — it determines when the agent is invoked. An agent with a vague description is an agent that never gets used.

---

## QUESTION: Your Philosophy of Agency

### The synthesis

**Exercise 6.7** — The essay:

Write 500-1000 words: **"What is agency in the age of AI?"**

Draw from:
- Your philosophical foundations (stoic, sufi, vedantic, Krishnamurti)
- Your psychological knowledge (cognitive bias, awareness, conditioning)
- Your hands-on experience building and using agents
- Your journal entries from the past 6 weeks

This is not an academic essay. It's YOUR synthesis — expressed in your voice, with your metaphors, from your experience. No jargon. No buzzwords. Just truth as you see it.

Suggested thread: Start with Epictetus (*what is in our control?*) → move through Krishnamurti (*thought is not intelligence*) → arrive at your own position on human-AI agency.

Write it in: `learning-plan/journal/week-6-philosophy-of-agency.md`

**Exercise 6.8** — The elevator pitch:

Now compress your essay into 2 sentences. If you can say it in 2 sentences, you understand it. If you can't, keep refining.

**Exercise 6.9** — The teaching test:

Explain agentic AI to:
1. A non-technical Coforge leader (2 minutes, no jargon)
2. A junior developer (5 minutes, some technical detail)
3. A philosopher who's never used a computer (2 minutes, pure concepts)

If you can do all three, you truly understand this. Record your attempts (even just as notes).

### The final question

**Exercise 6.10** — The Socratic close:

Answer these, then question your own answers:

1. *"What can agents do that humans can't?"* — and is that a feature or a threat?
2. *"What can humans do that agents can't?"* — and how long will that remain true?
3. *"What should neither humans nor agents do alone?"* — and who decides?
4. Kabir's loom: *"Jab main tha tab Hari nahin, ab Hari hain main nahin — prem gali ati saankri, taa mein do na samahi."* When I was, God was not; now God is, I am not — the lane of love is narrow, two cannot walk it together. When the agent is good enough... does the human step aside? Should they?

These questions don't have answers. They have better questions inside them. That's the sign of a real education.

---

## Week 6 Checkpoint — Final Assessment

- [ ] I built a capstone agent that solves a real problem
- [ ] I tested it adversarially and fixed what I found
- [ ] I can draw my personal agent architecture from memory
- [ ] I wrote 5+ design principles from my own experience
- [ ] I wrote my philosophy of agency (500+ words)
- [ ] I can explain agentic AI to three different audiences
- [ ] I still have questions — good ones — and I know where to look

---

## What's Next?

This plan ends, but the learning doesn't. Suggested directions:

| Direction | If you're drawn to... |
|----------|----------------------|
| **Build MCP servers for Coforge** | Standardizing agent tools across the org |
| **Agent coaching/training** | Teaching others what you've learned |
| **Advanced patterns** | Autonomous coding agents, self-improving systems |
| **Philosophy of AI** | Publish your thinking, build a reading circle |
| **Copilot Extensions** | Building sharable agents for the ecosystem |
| **Evaluation frameworks** | Systematic agent quality measurement |

---

*Rumi said: "As you start to walk on the way, the way appears."*

The way has appeared. Keep walking.

*Khatam shud — but not really. It never is.*
