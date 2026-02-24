# Week 4 — Multi-Agent Systems

> *"Akele hain to kya gham hai, qafile bana ke chalna seekho."*  
> *If you're alone, why worry? Learn to walk as a caravan.*  
> *This week: agents that collaborate.*

---

## BUILD: Agent Orchestration

### Day 1-2: Multiple Agents, One Problem

You've built individual agents. Now make them work together.

**Exercise 4.1** — The Three-Agent Review:

Create three agents that tackle code review from different angles:

1. **Logic-Reviewer** (`Logic-Reviewer.agent.md`)
   - Focuses on correctness, edge cases, error handling
   - Thinks like a debugger — adversarial, looking for what breaks
   - Style: Feynman (explain *why* the logic matters)

2. **Clarity-Reviewer** (`Clarity-Reviewer.agent.md`)
   - Focuses on readability, naming, structure, simplicity
   - Thinks like a writer — every function should read like a clear sentence
   - Style: Strunk & White (omit needless code)

3. **Architecture-Reviewer** (`Architecture-Reviewer.agent.md`)
   - Focuses on design, coupling, cohesion, patterns, future maintenance
   - Thinks like a city planner — individual buildings matter less than the whole
   - Style: Stoic (is this within the module's concern, or outside it?)

**Exercise 4.2** — Run all three on the same piece of code:
- Note where they agree → these are likely genuine issues
- Note where they contradict → this is where you need human judgment
- Note what none of them catch → this is the gap

**Key insight**: Multi-agent systems aren't about having more agents. They're about having *diverse perspectives*. The same principle as cognitive diversity in human teams.

### Day 3-4: Delegation Patterns

**Exercise 4.3** — Build an **Orchestrator** agent:
- File: `Orchestrator.agent.md`
- Purpose: When given a complex task, it *delegates* to other agents rather than doing everything itself
- Instructions should include: "Before coding, determine which specialist agent would handle this best. If the task crosses domains, break it into sub-tasks and suggest which agent handles each."
- This agent doesn't write code — it thinks about *who* should

**Exercise 4.4** — Build a **Research-and-Write** pipeline:
- Agent 1: `Researcher.agent.md` — Given a topic, gathers information, finds relevant code/docs, produces structured notes
- Agent 2: `Writer.agent.md` — Given structured notes, produces clear documentation/reports
- Use Agent 1's output as Agent 2's input (manually for now — pass the output yourself)
- Observe: Does Agent 2 work better with Agent 1's pre-processed input vs raw information?

### Day 5: Conflict & Consensus

**Exercise 4.5** — Deliberate disagreement:

Create two agents with deliberately opposing perspectives on the *same* task:

- `Optimist.agent.md` — Focuses on possibilities, speed, innovation, "yes and..."
- `Critic.agent.md` — Focuses on risks, edge cases, failure modes, "yes but..."

Give them the same project proposal. Compare outputs. Where does the truth lie? This is the multi-agent equivalent of *dialectic* — thesis, antithesis, synthesis.

---

## UNDERSTAND: Coordination Architectures

### Patterns of Multi-Agent Collaboration

| Pattern | Description | Strength | Weakness |
|---------|-------------|----------|----------|
| **Sequential pipeline** | Agent A → Agent B → Agent C | Simple, predictable | Slow, no feedback loops |
| **Parallel specialists** | Multiple agents work independently, results merged | Fast, diverse views | May contradict |
| **Hierarchical delegation** | Orchestrator assigns tasks to specialists | Scalable, organized | Orchestrator is single point of failure |
| **Debate/adversarial** | Agents argue, human or meta-agent judges | Surfaces assumptions | Can be wasteful |
| **Collaborative refinement** | Agent A drafts, Agent B critiques, Agent A revises | High quality output | Slow, many rounds |

### Exercise 4.6 — Design an Architecture

For a real project you've worked on, design a multi-agent architecture:
- Which agents would you need?
- What pattern of coordination?
- Where does a human need to be in the loop?
- What could go wrong?

Sketch it (even on paper). The sketch IS the architecture.

### Reading

1. [AutoGen paper](https://arxiv.org/abs/2308.08155) — Multi-agent conversation framework (skim for patterns, ignore the API details)
2. [CrewAI concepts](https://docs.crewai.com/concepts/) — Role-based multi-agent design (read the concepts, not the code)
3. GitHub blog posts on Copilot Extensions — how third-party agents integrate into the ecosystem

### Key Insight

In the Copilot ecosystem, multi-agent collaboration currently happens through **you** — you invoke different agents, pass context between them, judge their outputs. You are the orchestrator. 

The question is: how much of that orchestration can (and should) be automated? And what happens to the quality of thinking when the human leaves the loop?

---

## QUESTION: Collective Intelligence

### Philosophical exercises

**Exercise 4.7** — Sufi circles and agent swarms:

In Sufi tradition, the *sema* (whirling) works because each dervish moves individually but is synchronized by shared intention and the music. No one commands — their emerges order from shared practice.

1. Can AI agents achieve something like this? What would "shared intention" mean for agents?
2. Ant colonies build complex structures with no architect. Each ant follows simple rules. This is *stigmergy* — coordination through the environment, not communication. Is a multi-agent AI system more like a human team or an ant colony?
3. Krishnamurti distrusted all organizations and collectives — he said they inevitably corrupt individual intelligence. *"Truth is a pathless land."* Does this apply to multi-agent systems? Can a collective of agents discover something no individual agent could?

**Exercise 4.8** — The wisdom of crowds vs the madness of crowds:

James Surowiecki showed that crowds are wise when: (a) individuals have diverse information, (b) they think independently, (c) their opinions are aggregated well.

1. Do your multi-agent reviews meet these criteria?
2. What happens when all agents are trained on the same data (same LLM)? Is that truly *diverse* perspective, or the illusion of diversity?
3. Bulleh Shah: *"Masjid dha de, mandir dha de, dha de jo kujh dainda — par kisi da dil na dhain."* Tear down structures, but don't break the heart. When agents disagree, there's no heart to break. Is that a feature or a bug?

**Exercise 4.9** — Human-agent teams:

The most powerful multi-agent system right now isn't a swarm of AIs — it's *you + multiple AI agents*. You provide:
- Goal-setting (what to work on)
- Judgment (which output is better)
- Values (what "good" means)
- Context (what matters in this situation)

The agents provide:
- Speed (rapid exploration of options)
- Breadth (multiple perspectives simultaneously)
- Consistency (no "off days")
- Patience (no ego, will iterate endlessly)

Write a one-paragraph manifesto: What is the ideal human-agent team? What does each party bring that the other can't? 

### Reading

- Surowiecki — *The Wisdom of Crowds*, Chapter 1 (conditions for collective intelligence)
- Michael Tomasello — *Becoming Human*, on shared intentionality (what makes human collaboration unique)
- Optional: Rumi — *Masnavi*, Book 1 (stories about cooperation and ego)

---

## Week 4 Checkpoint

- [ ] I built 3+ specialist agents and ran them on the same problem
- [ ] I built an orchestrator agent that delegates rather than executes
- [ ] I understand 5 multi-agent coordination patterns
- [ ] I observed where agent perspectives converge, diverge, and miss
- [ ] I can articulate what the *human* uniquely contributes to a human-agent team
- [ ] I journaled on collective intelligence — when it works, when it doesn't

---

*"If you want to go fast, go alone. If you want to go far, go together."* — African proverb  
*If you want to go fast AND far — go together with agents, but keep your hands on the wheel.*
