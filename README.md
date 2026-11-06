# Algolex Solutions AI Customer Assistant

**One More Milestone in My AI Development Journey!**

An intelligent AI-powered Customer Assistant built and tested using open-source AI technologies. Designed to understand customer enquiries and provide information about Algolex Solutions' services.

## Project Overview

This is my second AI Agent project. It demonstrates practical integration of local LLMs, workflow automation, and tool use for customer interaction.

- Understands customer enquiries
- Provides information about Algolex Solutions services
- Uses local AI model (no external API costs for inference)
- Integrates tools for enhanced capabilities

## Technology Stack

- **n8n** – Workflow Automation
- **Ollama** – Local AI Model Execution
- **Llama 3.2** – Large Language Model
- **AI Agent** – Intelligent customer interaction
- **Calculator** – Tool Integration

## Workflow Architecture

```
Customer Message → Chat Trigger → AI Agent → Ollama LLM + Calculator → AI Response
```

### Nodes Used
- **When chat message received** (Chat Trigger)
- **AI Agent**
- **Ollama Chat Model** (Llama 3.2)
- **Calculator** (Tool)

Successfully connected, tested the workflow, integrated a locally running AI model, tested customer enquiries, and published the workflow in n8n.

## How to Use / Import

1. Ensure you have **n8n** running (self-hosted or cloud).
2. Have **Ollama** installed and running locally with the `llama3.2` model pulled:
   ```bash
   ollama pull llama3.2
   ollama serve
   ```
3. Export the workflow from your n8n instance (Menu → Download) as JSON, or use the workflow file in this repo (once added).
4. In n8n: Menu → Import from File, then configure credentials/connections for Ollama if needed.
5. Test with sample customer messages.

> **Note:** Exported n8n workflows may contain credential IDs. Clean sensitive information before sharing publicly.

## Learning Outcomes

This project has strengthened practical understanding of:
- AI agents
- LLM integration (local with Ollama)
- Tool connectivity
- No-code / low-code automation with n8n

Every project brings a new learning experience, a new challenge, and another opportunity to innovate.

**Learning AI. Building AI. Implementing AI.**

## Author

**Mukesh Kumar Singh**  
Assistant Professor (CSE) at SMIT | Quantum AI Researcher | Founder, Algolex Solutions  

- LinkedIn: [Mukesh kumar singh](https://www.linkedin.com/in/)
- GitHub: [kmukesh1](https://github.com/kmukesh1)
- Company: Algolex Solutions

---

*This is another milestone in my AI development journey!*
