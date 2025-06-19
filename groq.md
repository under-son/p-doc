# Groq

> Guide for integrating Groq's high-performance language models with PraisonAI, including API setup and configuration

# Add GROQ to Praison AI

## Code

<AccordionGroup>
  <Accordion title="Groq Integration" defaultOpen>
    ```bash
    export OPENAI_API_KEY=xxxxxxxxxxx
    export OPENAI_BASE_URL=https://api.groq.com/openai/v1
    ```
  </Accordion>
</AccordionGroup>

## No Code

```bash
export GROQ_API_KEY=xxxxxxxxxx
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
      model: "groq/llama3-70b-8192"
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
