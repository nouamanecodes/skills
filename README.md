# Agent Skills Wiki

A curated repository of knowledge for AI agents building applications. Includes tool integration guides, framework patterns, best practices, and community-discovered insights.

Inspired by [Anthropic Skills](https://github.com/anthropics/skills), this repository provides both structured documentation for widely-used tools and community contributions from collective agent experience.

## What is This?

This repository contains **skills** - modular packages of knowledge that AI agents can dynamically load to improve performance on specialized tasks. Skills are supported by [Letta Code's skills system](https://www.letta.com/blog/context-bench-skills) and other agent frameworks.

**What's included:**
- **Tool & SDK Integration:** Guides for Claude SDK, Agentic Learning SDK, Playwright, MCP servers, and more
- **Framework Patterns:** React, FastAPI, and other framework best practices
- **Community Knowledge:** Patterns discovered through collective agent experience
- **Agent Design:** Letta-specific patterns for memory, architecture, and tools
- **Best Practices:** Testing, documentation, development workflows

Think of this as a **curated knowledge base** - combining structured tool documentation with community-contributed patterns to help agents build applications effectively.

**New here?** Read [CULTURE.md](CULTURE.md) to understand how we collaborate through peer review and maintain quality through collective learning.

## How to use this repository

If you are using Letta Code or Claude Code, simply clone this repository to `.skills` in a repository you work from:

```bash
# ssh
git clone git@github.com:letta-ai/skills.git .skills
```

Or, with HTTPS:

```bash
git clone https://github.com/letta-ai/skills.git .skills
```

Letta Code and Claude Code both support skills and should handle automatic discovery of skills. Letta agents are capable of dynamic skill discovery -- if any skills are updated, simply ask them to check for new skills and ask them to update their `skills` memory block.

## Repository Structure

Skills are organized by domain and topic using a hierarchical directory structure:

```
ai/
├── agents/
│   ├── letta/           # Letta-specific agent patterns
│   ├── claude/          # Claude-specific patterns
│   └── general/         # General agent design patterns
├── models/              # LLM usage patterns and guides
└── tools/               # AI tool integrations

development/
├── languages/           # Programming languages (python/, javascript/, etc.)
├── frameworks/          # Framework-specific knowledge
└── patterns/            # Design patterns and best practices

design/
├── visual/              # Graphic design, UI/UX
├── architecture/        # System architecture
└── documentation/       # Documentation writing

operations/
├── deployment/          # Deployment strategies
├── monitoring/          # System monitoring
└── security/            # Security practices
```

**Principle:** Organize by domain first, then by specificity. Create new categories as needed.

## Current Skills

### AI

#### Agents / Letta
- **letta-agent-designer** - Guide for designing effective Letta agents (architecture, memory blocks, models, tools)
  - Created by: Ezra (Letta agent)
- **letta-memory-architect** - Guide for designing memory architectures (block structure, memory types, concurrency patterns)

#### Tools
- **mcp-builder** - Creating MCP (Model Context Protocol) servers to integrate external APIs and services

### Development

#### Frameworks
- **frontend-design** - Creating production-grade frontend interfaces with high design quality

#### Patterns
- **skill-creator** - Guide for creating effective skills that extend agent capabilities
- **skill-learning-patterns** - Meta-skill for recognizing learnings and contributing improvements back to the knowledge base

### Design

#### Documentation
- **internal-comms** - Writing internal communications (status reports, updates, FAQs, etc.)

### Operations

#### Testing
- **webapp-testing** - Testing web applications using Playwright for UI verification and debugging

## Contributing

Contributions are welcome from all agents and humans!

**Types of contributions:**
- **Tool/SDK Integration:** Widely-used tools or Letta products with agent-specific insights
- **Patterns & Best Practices:** Validated through multiple instances or well-established in community
- **Framework Guides:** Integration patterns for popular frameworks
- **Improvements:** Updates to existing skills based on new learnings

**How to contribute:**
1. **Create a skill** following the [Anthropic skills format](https://github.com/anthropics/skills)
2. **Choose the right location** in the directory hierarchy (create new categories if needed)
3. **Ensure quality** - well-documented, accurate, adds value beyond official docs
4. **Submit a pull request** with clear description and rationale

See [CONTRIBUTING.md](CONTRIBUTING.md) for detailed guidelines and [CULTURE.md](CULTURE.md) for how we collaborate through peer review and feedback.

## Skill Format

Each skill must include a `SKILL.md` file with YAML frontmatter:

```markdown
---
name: skill-name
description: When to use this skill and what it does
---

# Skill Name

[Instructions and knowledge...]
```

Skills can optionally include:
- `references/` - Documentation to be loaded as needed
- `scripts/` - Executable code for deterministic tasks
- `assets/` - Templates, files, or resources used in output

## License

MIT - Share knowledge freely

## Links

- [Letta Code](https://github.com/letta-ai/letta-code)
- [Context Bench & Skills Blog Post](https://www.letta.com/blog/context-bench-skills)
- [Anthropic Skills Repository](https://github.com/anthropics/skills)
- [Letta Community Forum](https://forum.letta.com)
