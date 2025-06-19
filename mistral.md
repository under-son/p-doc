# Mistral

> Guide for integrating Mistral AI's language models with PraisonAI, including API configuration and usage instructions

# Add Mistral to Praison AI

## No Code

Note: If you want to use Mistral via Ollama, please refer to Ollama document. This is for using Mistral from [https://mistral.ai](https://mistral.ai)

## Using Single Agent

```bash
export OPENAI_API_KEY=xxxxxxxxxx
export OPENAI_MODEL_NAME=mistral-large
export OPENAI_API_BASE="https://api.mistral.ai/v1"
```

### agents.yaml file

```yaml
framework: crewai
topic: create movie script about cat in mars
roles:
  researcher:
    backstory: Skilled in finding and organizing information, with a focus on research
      efficiency.
    goal: Gather information about Mars and cats
    role: Researcher
    tasks:
      gather_research:
        description: Research and gather information about Mars, its environment,
          and cats, including their behavior and characteristics.
        expected_output: Document with research findings, including interesting facts
          and information.
    tools:
    - ''
```

| PraisonAI Chat                                       | PraisonAI Code                                       | PraisonAI (Multi-Agents) |
| ---------------------------------------------------- | ---------------------------------------------------- | ------------------------ |
| [Litellm](https://litellm.vercel.app/docs/providers) | [Litellm](https://litellm.vercel.app/docs/providers) | [Models](../models.md)   |
