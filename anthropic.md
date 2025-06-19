# Anthropic

> Instructions for integrating Anthropic's Claude models with PraisonAI, including API setup and agent configuration

# Add Anthropic to Praison AI

## No Code

```bash
pip install langchain-anthropic
```

```bash
export ANTHROPIC_API_KEY=xxxxxxxxxx
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
    llm:  
      model: "anthropic/claude-3-haiku-20240307"
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
