# Ollama

> Instructions for integrating Ollama's open-source language models with PraisonAI, including configuration and usage examples

# Add Ollama to Praison AI

## Code

<AccordionGroup>
  <Accordion title="Ollama Integration" defaultOpen>
    **Standard OpenAI SDK Environment Variables (Recommended):**

    ```bash
    export OPENAI_BASE_URL=http://localhost:11434/v1
    export MODEL_NAME=deepseek-r1:14b
    export OPENAI_API_KEY=NA
    ```

    **Alternative Environment Variable Patterns:**

    ```bash
    # Community recommended pattern
    export OLLAMA_API_BASE=http://localhost:11434
    export MODEL_NAME=gemma3:4b
    export OPENAI_API_KEY=fake-key

    # Legacy pattern (still supported)
    export OPENAI_API_BASE=http://localhost:11434/v1
    export OPENAI_MODEL_NAME=llama2
    export OPENAI_API_KEY=not-needed
    ```

    **Usage with praisonai --init:**

    ```bash
    # Make sure Ollama is running
    ollama serve

    # Pull your desired model
    ollama pull deepseek-r1:14b

    # Set environment variables
    export OPENAI_BASE_URL=http://localhost:11434/v1
    export MODEL_NAME=deepseek-r1:14b
    export OPENAI_API_KEY=NA

    # Initialize agents
    praisonai --init "Create a story about AI"
    ```
  </Accordion>
</AccordionGroup>

## No Code

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
      model: "ollama/llama3"
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
