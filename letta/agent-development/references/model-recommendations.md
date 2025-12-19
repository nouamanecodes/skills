# Model Selection Guide

## Production Recommendations

### High-Quality Reasoning
- **GPT-4o**: Best overall, reliable tool calling
- **Claude 4.5 Sonnet**: Excellent reasoning, strong with memory tools
- **Gemini 2.5 Pro**: Good performance, intermittent function calling issues

### Cost-Efficient
- **GPT-4o-mini**: Best balance of cost and capability
- **Claude Haiku 4.5**: Fast, lightweight, good for simple tasks

### Local/Self-Hosted
- **qwen3**: Strong local model
- **Mistral Small**: Good tool calling
- **gpt-oss**: Recommended by team for local deployment

## Avoid for Production

### Tool Calling Issues
- Ollama models < 7B parameters
- Gemini models older than 2.5 Pro
- Command R (team assessment: "bad model")

### Proxy Provider Issues
- OpenRouter: "playing Russian roulette" with tool calling
- Groq: Generally poor tool calling support

## Context Window Considerations

**Default: 32k tokens**
- Team recommends 32k as sweet spot
- Larger windows (100k+) cause two issues:
  1. Agent reliability decreases
  2. Response latency increases

**When to increase:**
- Specific use case requires larger context
- Willing to accept performance trade-offs
- Have tested reliability at target size

## Reasoning Models

**Native reasoning (v1 agents only):**
- GPT-5
- Claude 4.5 Sonnet with Responses API

**Prompted reasoning (v2 agents):**
- Better for smaller models
- Uses tool call arguments for "fake" reasoning

## Cost Management

**Self-hosted:**
- Pay per token directly to provider
- No Letta overhead

**Letta Cloud:**
- Per-message pricing (not per token)
- 1 credit = 1 standard model request
- Premium models have different multipliers
