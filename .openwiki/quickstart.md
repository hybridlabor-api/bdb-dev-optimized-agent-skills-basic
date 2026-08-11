# Quickstart Guide

Welcome to the **bdb-dev-optimized-agent-skills-basic** core repository. This guide provides immediate orientation for configuring and utilizing the core skills pack, OpenWiki documentation daemon, RepoGraph code health dashboard, and memB memory layer.

---

## 🚀 Quick Setup

### 1. Global Installation via NPX
Run the interactive CLI installer to deploy skills, local MCP configurations, and background daemons:
```bash
npx -y @hybridlabor-api/bdb-dev-optimized-agent-skills-basic
```

### 2. Manual Setup via Git
```bash
git clone https://github.com/hybridlabor-api/bdb-dev-optimized-agent-skills-basic.git
cd bdb-dev-optimized-agent-skills-basic
npm install
node installer.js
```

---

## 🌐 OpenWiki & Code Health Daemon

### 1. Configure Multi-Provider LLM Backend
OpenWiki supports multiple LLM providers via environment variables:
```bash
# Example: Using Google Gemma 4 (Default)
export OPENWIKI_PROVIDER="google"
export GEMINI_API_KEY="your-gemini-key"

# Example: Using Groq (Ultra-Fast)
export OPENWIKI_PROVIDER="groq"
export GROQ_API_KEY="your-groq-key"

# Example: Using Local Ollama (Offline)
export OPENWIKI_PROVIDER="ollama"
export OPENWIKI_MODEL="llama3"
```

### 2. View Interactive Code Health Dashboard
Open the Repowise-grade Code Health dashboard in your default browser:
```bash
open .openwiki/code_health_dashboard.html
```
*Features 6 live visual panels with 60-second auto-refresh and integrated memB sync telemetry.*

---

## 🧠 memB Semantic Memory Synchronization

To ingest project context and architecture into the local SQLite vector database (`~/.MemBDB/memb.db`):
```bash
python mcps/memb-mcp/memb_ingest.py .openwiki --project "bdb-dev-optimized-agent-skills-basic" --category "Architecture_and_Wiki"
```

---
