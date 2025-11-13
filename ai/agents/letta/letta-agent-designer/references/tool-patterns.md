# Common Tool Configurations

## Memory-Only Agent

```python
tools = [
  "memory_insert",
  "memory_replace",
  "memory_rethink"
]
```

**Use cases:**

- Personal assistants
- Note-taking agents
- Context managers

## File System Agent

```
# Tools auto-attached when folder connected:
# - read_file
# - write_file
# - list_files
# - grep
# - search_files
```

**Use cases:**

- Code analysis
- Document processing
- Project management

## Database Agent

```
tools = [
  "memory_insert",
  "memory_replace",
  "query_database", # Custom tool
  "update_record" # Custom tool
]
```

**Use cases:**

- Data analysis
- Report generation
- Database management

## Multi-Agent System

```
# Supervisor agent:
tools = [
  "memory_insert",
  "send_message_to_agent_and_wait_for_reply"
]

# Worker agents:
tools = [
  "memory_insert",
  "domain_specific_tool"
]
```

**Note:** A2A messaging has known issues in v1 (November 2025). Community workaround available.

## Tool Rules

Constrain tool sequences without hardcoded workflows:

```
tool_rules = [
  {
    "tool_name": "answer_question",
    "children": [] # Must be terminal call
  },
  {
    "tool_name": "search_files",
    "children": ["search_files", "answer_question"]
  }
]
```

**Pattern:** Agent must search before answering, but can search multiple times.

## Custom Tool Development

**Critical requirements:**

- ALL imports must be INSIDE function body
- Tools execute in sandbox without top-level imports
- Use `from letta_client.client import BaseTool` (not `from letta`)

**Example:**

```
def my_custom_tool(param: str) -> str:
  """Tool description"""
  import requests # Import INSIDE function

  # Tool logic here
  return result
```
