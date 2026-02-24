# Week 2 — Tools & Perception

> *"The hand that shapes the tool is shaped by the tool."*  
> *MCP is how agents gain hands. This week you build those hands.*

---

## BUILD: Your First MCP Server

### Day 1-2: Understanding MCP (Model Context Protocol)

MCP is the protocol that lets Copilot (and other agents) discover and use external tools. It's how an agent reaches beyond its own mind into the world.

**Exercise 2.1** — Examine the MCP tools already available to you:
- In Copilot Agent Mode, notice which tools it uses (file read, terminal, search, etc.)
- These are MCP-like tool interfaces. Each has: a **name**, a **description** (so the agent knows when to use it), **parameters** (what it needs), and a **return value** (what it gives back)
- Document 5 tools you see Copilot using. For each, write: Name, When it uses it, What it passes in, What it gets back

**Exercise 2.2** — Read the MCP specification:
- [MCP Documentation](https://modelcontextprotocol.io/introduction)
- [GitHub Copilot MCP support](https://docs.github.com/en/copilot/customizing-copilot/using-model-context-protocol)
- Key concept: MCP is a **standard** — like USB for AI tools. Any MCP server works with any MCP client.

### Day 3-4: Build an MCP Server

**Exercise 2.3** — Build a simple MCP server that provides a tool Copilot can use. Ideas:

**Option A — File summarizer**: A tool that takes a folder path and returns a natural-language summary of all files in it (names, sizes, types, structure)

**Option B — Decision journal**: A tool that logs decisions with context, alternatives considered, and reasoning — queryable later

**Option C — Quote server**: A tool that returns relevant philosophical quotes based on a topic (stoic, sufi, vedantic — draw from your own reading)

Steps:
1. Create a new project: `learning-plan/projects/my-first-mcp-server/`
2. Use Copilot Agent Mode to help you build it: *"Help me build an MCP server in Python/Node that provides a [tool-name] tool"*
3. Configure it in VS Code's `settings.json` under `mcp.servers`
4. Test it by invoking it through Copilot: *"@workspace use [tool-name] to..."*

**Exercise 2.4** — Add a SECOND tool to your MCP server. Observe:
- How does Copilot decide *which* tool to use?
- What happens if your tool descriptions are vague? Specific?
- Change a tool description and see if Copilot's behavior changes. The description IS the interface.

### Day 5: Iterate & Reflect

**Exercise 2.5** — Improve your MCP server based on testing:
- Better error handling (what happens when the tool fails?)
- Better descriptions (the description teaches the agent when/how to use the tool)
- Add input validation

---

## UNDERSTAND: Tools, Grounding, and the Boundary of Mind

### Key Concepts

**Tool-use** is what separates a chatbot from an agent. A chatbot thinks. An agent thinks *and acts*.

The pattern:
```
User request
  → Agent reasons about what tools might help
    → Agent calls tool with parameters
      → Tool returns result
        → Agent reasons about the result
          → Agent responds (or calls another tool)
```

**Grounding**: Without tools, an LLM only knows what's in its training data. Tools *ground* it in current reality — your files, your database, the live web, your specific context.

**The description is everything**: In MCP, the tool's description is how the agent *understands* the tool. A poorly described tool is like giving someone a gadget with no label — they won't know when to use it.

### Reading

1. [Anthropic — Tool Use patterns](https://docs.anthropic.com/en/docs/build-with-claude/tool-use) — How tool calling actually works under the hood
2. [MCP Specification](https://spec.modelcontextprotocol.io/) — Skim the architecture section
3. Lilian Weng — [LLM Agents](https://lilianweng.github.io/posts/2023-06-23-agent/) — Read the "Tool Use" section

### Exercise 2.6 — Tool Taxonomy

Categorize the tools an agent might use:

| Category | Examples | Why it matters |
|----------|----------|---------------|
| **Information retrieval** | File read, web search, database query | Grounds the agent in reality |
| **Action/mutation** | File write, API call, send email | Lets the agent change the world |
| **Computation** | Code execution, calculator, data transform | Extends beyond language |
| **Verification** | Lint, test, compile, error check | Agent can check its own work |
| **Human-in-the-loop** | Ask user, confirm action, get feedback | Maintains human agency |

Which category is most dangerous to give an agent unsupervised? Why?

---

## QUESTION: The Hand and the Hammer

### Philosophical exercises

**Exercise 2.7** — The tool shapes the user:

Marshall McLuhan said: *"We shape our tools, and thereafter our tools shape us."*

1. How has Copilot changed the way you write code? Not just speed — the way you *think* about code?
2. If the tool shapes the thinker, and the agent uses tools autonomously... is the agent being shaped by its tools? Is this wisdom or drift?
3. Kabir said: *"Chalti chakki dekh ke, diya Kabira roye — do paatan ke beech mein, saabut bacha na koy."* Watching the grinding stones, Kabir wept — nothing that enters between them survives intact. When data passes through an AI agent's tools... what gets ground away?

**Exercise 2.8** — The extension of self:

When you use a hammer, the hammer becomes an extension of your hand — you feel the nail through it. This is called "tool transparency" in phenomenology.

1. When you type in Copilot and it completes your thought — is the AI an extension of your mind? Or are you an extension of its training?
2. At what point does a tool stop being *your* tool and start being *its own agent*? Where is the line between "tool I use" and "entity that acts"?

### Reading

- Martin Heidegger — *Being and Time*, sections on "ready-to-hand" vs "present-at-hand" (a tool works best when you forget it's there)
- Optional: Andy Clark — *Supersizing the Mind* (the extended mind thesis — your phone IS part of your cognition)

---

## Week 2 Checkpoint

- [ ] I built an MCP server with 2+ tools and connected it to Copilot
- [ ] I can explain MCP to someone in one sentence without using the word "protocol"
- [ ] I observed how tool descriptions affect agent behavior
- [ ] I understand the 5 categories of agent tools
- [ ] I journaled on how tools shape the tool-user (and vice versa)
- [ ] I can explain why tool-use is the key differentiator between a chatbot and an agent

---

*"Give me a lever long enough and a fulcrum on which to place it, and I shall move the world."* — Archimedes  
*MCP is the fulcrum. The agent is the lever. The question is: who decides what to move?*
