# Algolex Solutions AI Customer Assistant

**One More Milestone in My AI Development Journey!**

An intelligent AI-powered Customer Assistant built and tested using open-source AI technologies. Designed to understand customer enquiries and provide information about Algolex Solutions' services.

![n8n + Ollama](https://img.shields.io/badge/n8n-Workflow-orange?logo=n8n) ![Ollama](https://img.shields.io/badge/Ollama-Local%20LLM-black) ![Llama 3.2](https://img.shields.io/badge/Llama-3.2-blue)

## Project Overview

This is my second AI Agent project. It demonstrates practical integration of local LLMs, workflow automation, and tool use for customer interaction.

- Understands customer enquiries
- Provides information about Algolex Solutions services
- Uses local AI model (no external API costs for inference)
- Integrates tools for enhanced capabilities (Calculator)

## Technology Stack

| Component | Purpose |
|-----------|---------|
| **n8n** | Workflow Automation |
| **Ollama** | Local AI Model Execution |
| **Llama 3.2** | Large Language Model |
| **AI Agent** | Intelligent customer interaction |
| **Calculator** | Tool Integration |

## Workflow Architecture

```
Customer Message → Chat Trigger → AI Agent → Ollama LLM + Calculator → AI Response
```

### Nodes Used
- **When chat message received** (Chat Trigger)
- **AI Agent**
- **Ollama Chat Model** (Llama 3.2)
- **Calculator** (Tool)

## Quick Start with Docker

```bash
# Clone the repo
git clone https://github.com/kmukesh1/algolex-ai-customer-assistant.git
cd algolex-ai-customer-assistant

# Start n8n + Ollama
docker compose up -d

# Pull Llama 3.2 (first time only)
docker exec -it ollama ollama pull llama3.2

# Open n8n
open http://localhost:5678
```

See **[SETUP.md](SETUP.md)** for detailed instructions, troubleshooting, and alternative setups.

## Import the Workflow

1. In n8n: **Menu → Import from File**
2. Select the workflow JSON from the `workflows/` folder
3. Configure the Ollama node base URL to `http://ollama:11434`
4. Test with sample customer messages

> **Note:** Exported n8n workflows may contain credential IDs. Clean sensitive information before sharing publicly.

## Learning Outcomes

This project has strengthened practical understanding of:
- AI agents
- LLM integration (local with Ollama)
- Tool connectivity
- No-code / low-code automation with n8n

**Learning AI. Building AI. Implementing AI.**

## Author

**Mukesh Kumar Singh**  
Assistant Professor (CSE) at SMIT | Quantum AI Researcher | Founder, Algolex Solutions  

- GitHub: [kmukesh1](https://github.com/kmukesh1)
- Company: Algolex Solutions

---

*This is another milestone in my AI development journey!*
