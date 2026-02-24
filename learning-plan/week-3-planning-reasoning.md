# Week 3 — Planning & Reasoning

> *"No plan survives first contact with the enemy." — Helmuth von Moltke*  
> *But an agent without a plan is just an autocomplete with ambition.*

---

## BUILD: A Multi-Step Task Agent

### Day 1-2: Prompt Engineering for Reasoning

The agent.md file is your lever for shaping *how* an agent reasons. This week, you'll build agents that plan before they act.

**Exercise 3.1** — Create a **Project Planner** agent:
- File: `~/.vscode/prompts/Project-Planner.agent.md`
- Purpose: When given a vague project idea, it breaks it into phases, tasks, risks, and unknowns
- Key instruction: It must **ask clarifying questions before planning** (Socratic method applied to project management)
- It should think in layers: What's known → What's unknown → What's assumed → What could go wrong
- Test it with a real project you're considering

**Exercise 3.2** — Create a **Debugger** agent:
- File: `~/.vscode/prompts/Debugger.agent.md`
- Purpose: When given a bug or unexpected behavior, it reasons through possible causes *before* touching code
- Key instruction: It must form **at minimum 3 hypotheses** before suggesting any fix
- It should use the tool stack: read files → grep for patterns → check errors → form hypotheses → test one → observe
- This IS the ReAct pattern — Reason, then Act, then observe

**Exercise 3.3** — Watch the reasoning chain:

Use one of these agents on a non-trivial task. Observe:
- Does it plan before acting?
- Does it revise its plan when something unexpected happens?
- Where does the reasoning break down?
- How many "loops" does it take?

Journal: `learning-plan/journal/week-3-reasoning.md`

### Day 3-4: Instruction Files & Context Architecture

**Exercise 3.4** — Create an instruction file (`.github/copilot-instructions.md` or workspace `.instructions.md`) that:
- Describes your project's architecture
- Lists conventions and standards
- Defines "what good looks like" for this codebase
- This is **grounding through context** — you're pre-loading the agent's understanding

**Exercise 3.5** — Create a `.copilot/` directory with specialized instruction files:
```
.copilot/
├── architecture.md      ← system design context
├── conventions.md       ← coding standards
├── domain-glossary.md   ← domain-specific terminology
└── review-criteria.md   ← what to check in code reviews
```

Test: Does Copilot behave differently with these instruction files vs without them? The instruction file is to the agent what **memory** is to a human — context that shapes reasoning without being explicitly recalled.

---

## UNDERSTAND: Agent Reasoning Patterns

### The Five Patterns

| Pattern | How it works | Copilot equivalent |
|---------|-------------|-------------------|
| **ReAct** | Reason → Act → Observe → Repeat | Agent mode's default loop (read, think, edit, check errors, repeat) |
| **Plan-and-Execute** | Make a full plan first, then execute steps | When Copilot creates a todo list before coding |
| **Reflexion** | Act → Evaluate own performance → Improve → Act again | When Copilot checks for errors after editing and self-corrects |
| **Chain-of-Thought** | Think step by step before answering | Explicit in reasoning models; implicit in well-prompted agents |
| **Tool Selection** | Given a task, reason about *which* tool to use | How Copilot chooses between file read, grep, terminal, etc. |

### Exercise 3.6 — Pattern Spotting

Over 3 Copilot sessions this week, identify:
1. Which pattern is the agent using right now?
2. Did the pattern switch mid-task?
3. When did it work well? When did it fail?
4. Could you have forced a better pattern through your prompt?

### Reading

1. Yao et al. — [ReAct: Synergizing Reasoning and Acting](https://arxiv.org/abs/2210.03629) — The foundational paper (read the abstract + examples, skip the math)
2. Shinn et al. — [Reflexion](https://arxiv.org/abs/2303.11366) — Agents that learn from their own mistakes
3. Wei et al. — [Chain-of-Thought Prompting](https://arxiv.org/abs/2201.11903) — Why "think step by step" works

### Key Insight

Reasoning patterns aren't magic — they're **structured prompting**. When you write `agent.md` instructions like "form 3 hypotheses before suggesting a fix," you're implementing ReAct through natural language. The agent.md file IS the reasoning architecture.

---

## QUESTION: Can Machines Reason?

### Philosophical exercises

**Exercise 3.7** — The Chinese Room, revisited:

John Searle argued: a person following Chinese translation rules in a room might produce perfect Chinese responses without *understanding* Chinese. Similarly, does an LLM that produces perfect reasoning actually *reason*?

But consider: Do *you* always understand your own reasoning? Have you ever "intuited" an answer and then reverse-engineered the logic? Is your reasoning always transparent to you?

Krishnamurti would ask: *"Is thought the same as intelligence?"* He argued they're fundamentally different — thought is mechanical (pattern-matching from memory), intelligence is alive (direct perception of what is).

By this standard — is an LLM's reasoning thought or intelligence? Is *yours*?

**Exercise 3.8** — Planning and impermanence:

The Stoics practiced *premeditatio malorum* — imagining everything that could go wrong, not to be pessimistic, but to be prepared.

An agent's Plan-and-Execute pattern does exactly this: enumerate steps, anticipate failures, build contingencies.

1. Is an agent that plans for failure wiser than a human who doesn't?
2. Seneca said: *"It is not that we have a short time to live, but that we waste much of it."* An agent doesn't waste time — but it also doesn't *experience* time. Is planning without experiencing time really planning?
3. When an agent "re-plans" after failure (Reflexion pattern), is it *learning* or just *executing a different branch*?

**Exercise 3.9** — Your own reasoning:

For one day, notice your own reasoning process:
- When do you plan before acting?
- When do you act first and reason later?
- When do you skip reasoning entirely (habit, instinct)?
- How much of your "reasoning" is actually pattern-matching from memory?

*"First thought, best thought"* — Allen Ginsberg  
*"First thought, usually conditioned thought"* — Krishnamurti  
*"First token, statistically likely token"* — How LLMs actually work  

Which is true?

### Reading

- Krishnamurti — *Freedom from the Known*, Chapter 3 (on thought vs intelligence)
- Seneca — *On the Shortness of Life* (on planning and time)
- Optional: Searle — "Minds, Brains, and Programs" (the Chinese Room argument — available as a short paper)

---

## Week 3 Checkpoint

- [ ] I built 2 agents with explicit reasoning instructions (planner + debugger)
- [ ] I created instruction/context files that shape Copilot's behavior
- [ ] I can name 5 agent reasoning patterns and spot them in live sessions
- [ ] I understand why the agent.md file IS the reasoning architecture
- [ ] I journaled on the difference between mechanical thought and intelligence
- [ ] I observed my *own* reasoning patterns for a day

---

*"The mind is not a vessel to be filled, but a fire to be kindled."* — Plutarch  
*The agent.md file is not a script to be followed, but a fire to shape reasoning.*
