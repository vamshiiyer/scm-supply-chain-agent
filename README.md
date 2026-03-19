cat > ~/cloudshell_open/easy-alloydb-setup-0/scm-memory-agent/README.md << 'EOF'
# 🏭 Supply Chain Orchestrator

> Built with Google ADK, AlloyDB, and Vertex AI Memory Bank

A multi-agent AI system that provides real-time supply chain intelligence using natural language.

## 🏗️ Architecture

User Query → GlobalOrchestrator (Gemini 2.5 Flash)
                ├── InventorySpecialist → AlloyDB (via MCP Toolbox)
                └── LogisticsManager   → AlloyDB (via MCP Toolbox)
                         ↕
            Vertex AI Memory Bank (Long-term memory)

## 🚀 Tech Stack

| Component | Purpose |
|---|---|
| **AlloyDB for PostgreSQL** | 50,000+ supply chain records + vector search |
| **MCP Toolbox** | Middleware exposing DB as agent tools |
| **Google ADK** | Multi-agent framework |
| **Vertex AI Memory Bank** | Long-term memory across sessions |
| **Flask** | Web UI |

## 🤖 Agents

- **GlobalOrchestrator** — Root agent, delegates tasks, manages memory
- **InventorySpecialist** — Stock levels, product search
- **LogisticsManager** — Shipment tracking, risk analysis

## 🛠️ Setup

1. Clone the repo
2. Create .env file with your values
3. Install: pip install -r requirements.txt
4. Run: python app.py

## 💬 Example Queries

- "Stock level for Premium Ice Cream?"
- "Any delayed shipments in EMEA?"
- "Analyze supply chain risk for port strike impact"
- "Give me a full supply chain health report"

## 📚 Based on

Google Codelab: https://codelabs.developers.google.com/scm-alloydb-adk-memorybank
EOF

git add README.md
git commit -m "Add detailed README"
git push origin main
