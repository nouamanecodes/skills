# Letta Agent Architectures

## letta_v1_agent (Recommended - October 2025)

**Key Features:**
- Native reasoning via Responses API (encrypted across providers)
- Direct assistant message generation (no send_message tool)
- Works with ANY LLM (tool calling no longer required)
- Optimized for frontier models (GPT-5, Claude 4.5 Sonnet)

**Trade-offs:**
- No prompted reasoning for smaller models
- Limited tool rules on AssistantMessage
- May experience more frequent summarizations

**Memory Tools:**
- memory_insert, memory_replace, memory_rethink (same as v2)
- archival_memory_insert/search: opt-in (must explicitly attach)

## memgpt_v2_agent (Legacy)

**When to Use:**
- Maintaining existing agents
- Specific workflow requires v2 tool patterns

**Key Differences:**
- send_message tool for explicit message generation
- More flexible tool rules
- Better for smaller models requiring prompted reasoning

**Note:** Team recommends migrating to v1 for new projects.
