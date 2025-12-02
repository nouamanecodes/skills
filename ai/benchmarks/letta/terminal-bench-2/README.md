# Terminal Bench 2 - Learned Skills

Skills learned during [Terminal Bench 2.0](https://github.com/letta-ai/terminal-bench) benchmarking using [Skill Learning](https://www.letta.com/blog/skill-learning).

## What is Skill Learning?

Skill Learning enables agents to learn from their past experiences (trajectories) and improve over time. Rather than treating every task as isolated, agents can benefit from patterns discovered in previous work.

The learning process:
1. **Reflection**: Given an agent's trajectory, evaluate whether it solved the task, assess reasoning soundness, and identify patterns that could be abstracted
2. **Creation**: Generate a skill that provides approaches, common pitfalls, and verification strategies

## Directory Structure

```
terminal-bench-2/
  trajectory-only/      # Skills learned from trajectory alone
  trajectory-feedback/  # Skills learned from trajectory + verifier feedback
```

### trajectory-only vs trajectory-feedback

- **trajectory-only**: Skills generated using only the agent's execution trajectory
- **trajectory-feedback**: Skills generated using trajectory plus textual feedback from task verifiers (error logs, test failures, etc.)

Our research shows that feedback-informed skills better encode failure modes and unsuccessful approaches, making them more robust. Trajectory + feedback provided an additional 6.7% improvement over trajectory-only.

## Results

Skills learned from Terminal Bench 2.0 led to:
- **36.8% relative improvement** (15.7% absolute) over baseline
- **15.7% cost reduction**
- **10.4% fewer tool calls**

## Usage

These skills can be loaded by agents when encountering similar tasks. See [SKILLS.md](SKILLS.md) for a searchable index organized by domain.

## Learn More

- [Skill Learning Blog Post](https://www.letta.com/blog/skill-learning)
- [Terminal Bench Repository](https://github.com/letta-ai/terminal-bench)
- [Letta Code](https://github.com/letta-ai/letta-code)
