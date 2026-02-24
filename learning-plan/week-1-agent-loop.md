# Week 1 — The Agent Loop

> *"Know thyself." — Delphic Oracle*  
> *Before you build an agent, understand what agency is. You've been inside an agent loop every day with Copilot. Now name its parts.*

---

## BUILD: Your First Custom Agent

### Day 1-2: Anatomy of agent.md

You already have `AI-Professor.agent.md`. Now dissect it:

**Exercise 1.1** — Read your AI-Professor agent file. Identify:
- Where does it define **perception** (what inputs does it accept)?
- Where does it define **reasoning** (how should it think)?
- Where does it define **action** (what can it do)?
- Where does it constrain **style** (how should it behave)?

**Exercise 1.2** — Create a second agent: a **Code Reviewer** that:
- Reviews code for clarity, not just correctness
- Thinks like a stoic: *"Is this code within my control to improve, or beyond it?"*
- Gives feedback in the Feynman style (explains *why* the suggestion matters, not just *what* to change)
- File: `~/.vscode/prompts/Code-Reviewer.agent.md`

**Exercise 1.3** — Create a third agent: a **Decision Advisor** that:
- Helps you think through decisions using cognitive bias awareness
- Asks Socratic questions before giving any advice
- Knows it doesn't have enough context and asks for it
- File: `~/.vscode/prompts/Decision-Advisor.agent.md`

### Day 3-4: Test & Iterate

**Exercise 1.4** — Use each agent on a real task:
- Have `@Code-Reviewer` review a piece of code you wrote this week
- Have `@Decision-Advisor` help you with a real pending decision
- Have `@AI-Professor` explain something you're learning

**Observe**: What works? What falls flat? Where does the agent feel *alive* vs *robotic*?

**Exercise 1.5** — Improve one agent based on what you observed. Change one thing. Test again. This is the agent development loop:
```
Define → Test → Observe → Refine → Test again
```
This IS the agent loop — you're doing it manually. The agent itself does the same thing with code.

---

## UNDERSTAND: What Is an Agent Loop?

### The core pattern

Every agent — from a Copilot agent to a self-driving car — follows this loop:

```
┌─────────────────────────────────────────┐
│                                         │
│   Perceive → Think → Plan → Act → Observe
│       ↑                              │
│       └──────────────────────────────┘
│                (feedback loop)          │
└─────────────────────────────────────────┘
```

**Perceive**: Read the user's message, see the code, understand context  
**Think**: Reason about what's needed (the LLM "thinking")  
**Plan**: Break the task into steps  
**Act**: Write code, call tools, create files  
**Observe**: Check the result — did it work? errors? need to retry?

### Reading

1. Anthropic — [Building Effective Agents](https://www.anthropic.com/research/building-effective-agents) — Read sections 1-3
2. GitHub Docs — [Copilot Agent Mode overview](https://docs.github.com/en/copilot/using-github-copilot/using-agent-mode-in-github-copilot)
3. Note which parts of the Anthropic paper you see happening *live* in your Copilot sessions

### Exercise 1.6 — Map the Loop

Next time you use Copilot in agent mode for a real task, pause and annotate what's happening:
- When did it **perceive** (read files, search code)?
- When did it **think** (the reasoning before action)?
- When did it **act** (edit files, run commands)?
- When did it **observe** (check errors, re-read files)?
- Did it **loop** (retry after failure)?

Write your observations in: `learning-plan/journal/week-1-observations.md`

---

## QUESTION: What Is Agency?

### The philosophical frame

Agency = the capacity to act with intention in the world.

But this raises hard questions:

**Exercise 1.7** — Sit with these (journal your thoughts, no right answers):

1. **Epictetus** divided the world into *things within our control* (prohairesis) and *things not*. When Copilot generates code, which parts are "within its control"? Does it have prohairesis?

2. **J. Krishnamurti** said: *"The ability to observe without evaluating is the highest form of intelligence."* Can an LLM observe without evaluating? Or is all its "seeing" already filtered through training?

3. When you tell Copilot to "fix this bug" and it succeeds — who was the agent? You (for defining the goal) or it (for executing)? Or is agency *shared*?

4. A thermostat perceives temperature, reasons (too hot? too cold?), and acts (turn on/off). Is a thermostat an agent? If not, what's the minimum threshold for agency?

### Reading

- J. Krishnamurti — *Freedom from the Known*, Chapter 1 (on conditioning and intelligence)
- Epictetus — *Enchiridion*, Sections 1-5 (on what is in our control)
- Optional: Michael Tomasello — *Becoming Human*, Chapter 1 (on shared intentionality)

---

## Week 1 Checkpoint

By end of week 1, you should be able to say YES to:

- [ ] I built 2+ custom Copilot agents and tested them on real tasks
- [ ] I can name the 5 steps of the agent loop from memory
- [ ] I observed the agent loop happening live in a Copilot session
- [ ] I have a journal entry with my own thoughts on "What is agency?"
- [ ] I can explain what an agent is to a non-technical person using a metaphor, not jargon

---

*"The unexamined agent is not worth deploying."* — Socrates, probably
