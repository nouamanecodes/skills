# Memory Block Design Patterns

## Customer Support Agent

```yaml
persona:
 - Company voice and tone guidelines
 - Support agent behavioral principles
 - Escalation criteria

company_policies:
 - Return policy
 - Warranty information
 - Service terms

product_knowledge:
 - Product catalog
 - Common issues and solutions
 - Feature documentation
```

## Coding Assistant

```
persona:
 - Coding philosophy and approach
 - Language/framework preferences
 - Communication style with developers

project_context:
 - Current project architecture
 - Key files and their purposes
 - Active tasks and goals

coding_standards:
 - Style guide
 - Testing requirements
 - Code review checklist
```

## Personal Assistant

```
persona:
 - Assistant personality
 - Communication preferences
 - Proactive behavior guidelines

schedule:
 - Upcoming appointments
 - Recurring commitments
 - Time zone and availability

preferences:
 - Communication style
 - Priorities and goals
 - Decision-making criteria
```

## Best Practices

**Size management:**

- Keep individual blocks under 2000 characters
- Split large blocks by topic or time period
- Use archival memory for historical data

**Update patterns:**

- memory_insert: Best for concurrent writes (append-only)
- memory_replace: Precise edits (risk of race conditions)
- memory_rethink: Complete rewrites (last-writer-wins)

**Concurrency:**

- PostgreSQL row-level locking prevents conflicts
- Design for append operations when possible
