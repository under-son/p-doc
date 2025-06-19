# Cohere

> Guide for integrating Cohere's language models with PraisonAI, including API setup and configuration examples

# Add COHERE to Praison AI

## No Code

```bash
pip install langchain-cohere
```

```bash
export COHERE_API_KEY=xxxxxxxxxx
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
      model: "cohere/command-r"
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
