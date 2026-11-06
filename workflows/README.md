# Workflows

Place your exported n8n workflow JSON file(s) here.

### Recommended filename
`algolex-ai-customer-assistant.json`

### How to export from n8n
1. Open the workflow in n8n.
2. Click the three-dot menu (or Workflow menu) in the top bar.
3. Select **Download**.
4. Save the JSON file and commit it to this folder.

### Importing
In a new n8n instance: Menu → **Import from File** and select the JSON.

### After Import
- Set the Ollama Chat Model base URL to `http://ollama:11434` (Docker) or `http://localhost:11434` (host).
- Make sure the `llama3.2` model is available in Ollama.
