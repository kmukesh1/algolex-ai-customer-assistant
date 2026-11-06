# Detailed Setup Guide

## Option 1: Quick Local Setup (Recommended for Testing)

### Prerequisites
- Docker & Docker Compose installed
- At least 8GB RAM (16GB recommended for Llama 3.2)

### Steps

1. **Clone this repository**
   ```bash
   git clone https://github.com/kmukesh1/algolex-ai-customer-assistant.git
   cd algolex-ai-customer-assistant
   ```

2. **Start n8n + Ollama**
   ```bash
   docker compose up -d
   ```

3. **Pull the Llama 3.2 model** (first time only, takes a few minutes)
   ```bash
   docker exec -it ollama ollama pull llama3.2
   ```

4. **Open n8n**
   - Go to http://localhost:5678
   - Create your local account

5. **Import the workflow**
   - In n8n: Menu → Import from File
   - Select the workflow JSON from the `workflows/` folder

6. **Configure Ollama connection**
   - In the Ollama Chat Model node, set the base URL to:
     - `http://ollama:11434` (when both run in Docker)
     - or `http://host.docker.internal:11434` if Ollama is on the host

7. **Test**
   - Open the chat and try: "What services does Algolex Solutions offer?"

---

## Option 2: Run Ollama on Host + n8n in Docker

If you have a GPU and want better performance:

1. Install Ollama directly on your machine: https://ollama.com
2. Pull the model:
   ```bash
   ollama pull llama3.2
   ```
3. Run only n8n in Docker and set Ollama URL to `http://host.docker.internal:11434`

---

## Workflow Architecture

```
Customer Message 
    ↓
Chat Trigger (When chat message received)
    ↓
AI Agent
    ↓
Ollama Chat Model (Llama 3.2) + Calculator Tool
    ↓
AI Response
```

## Troubleshooting

| Issue | Solution |
|-------|----------|
| Ollama connection fails | Use `http://ollama:11434` inside Docker network |
| Model not found | Run `docker exec -it ollama ollama pull llama3.2` |
| n8n not starting | Check `docker compose logs n8n` |
| Low RAM | Use a smaller model like `llama3.2:1b` |

## Next Steps

- Add more tools (web search, database, email)
- Add conversation memory
- Deploy to a VPS for public access
- Connect to WhatsApp / Telegram / website chat
