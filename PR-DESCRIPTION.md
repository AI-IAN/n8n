# n8n Workflow Builder with Local LLM Support

## Summary

Add comprehensive n8n workflow automation tools powered by AI, with both cloud (Claude API) and local (RTX 5090) options.

### 🤖 Claude Code Skill (`.claude/skills/`)
- Expert n8n workflow builder using Claude 3.5 Sonnet
- References actual n8n documentation and 100+ example workflows
- Creates production-ready workflows through conversational interface
- ✅ Instant setup, no configuration needed

### 🎮 LangChain Local Agent (`langchain-agent/`)
- Run entirely locally on RTX 5090 32GB VRAM
- Zero API costs after hardware investment
- Supports Ollama, vLLM, and LlamaCpp backends
- Optimized for Qwen 2.5 72B, Llama 3.1 70B, DeepSeek Coder V2
- 🔒 100% privacy - all data stays local
- ⚡ No rate limits

### 🔄 Meta Workflow (`workflows/meta-workflow-generator.json`)
- n8n workflow that generates other n8n workflows
- Uses local Ollama LLM through LangChain nodes
- Interactive chat interface for workflow creation

---

## Features

**Both approaches provide:**
- 🔍 Search through 100+ example workflows
- 📚 Access to n8n node documentation
- ✅ Workflow JSON validation
- 🚀 Production-ready outputs
- ⭐ Best practices built-in

**Use Cases:**
- API integrations and data sync
- AI chat agents with Claude
- Scheduled automations
- Webhook workflows
- Business process automation

---

## Documentation

| File | Description |
|------|-------------|
| `.claude/README.md` | Claude Code skill guide |
| `.claude/QUICKSTART.md` | Quick start examples |
| `langchain-agent/README.md` | Local LLM setup for RTX 5090 |
| `langchain-agent/REPO-ORGANIZATION.md` | Repository organization guide |
| `COMPARISON-CLAUDE-VS-LOCAL.md` | Comparison and decision matrix |

---

## Setup

### Claude Code Skill (Immediate) ⚡
Already working - just use Claude Code!

### Local Agent (10-30 minutes) ⚙️
```bash
cd langchain-agent
./setup.sh
# Follow prompts to install Ollama and pull models
```

---

## Model Recommendations (RTX 5090 32GB)

| Model | Size | Quality | Speed | Best For |
|-------|------|---------|-------|----------|
| **Qwen 2.5 72B** | 72B | ⭐⭐⭐⭐⭐ | Medium | Coding, reasoning |
| **Qwen 2.5 Coder 32B** | 32B | ⭐⭐⭐⭐ | Fast | Quick iterations |
| **Llama 3.1 70B** | 70B | ⭐⭐⭐⭐⭐ | Medium | General purpose |
| **DeepSeek Coder V2** | 236B MoE | ⭐⭐⭐⭐ | Medium | Code specialized |

---

## Cost Analysis

| Approach | Cost per Workflow | Best For |
|----------|------------------|----------|
| **Claude API** | ~$0.02 | Development, prototyping |
| **Local LLM** | ~$0 (electricity only) | Production, high volume |

**Break-even**: >1,000 workflows/month → Local LLM wins

---

## Quick Examples

### Example 1: Simple API Integration
```
Create a workflow that fetches data from JSONPlaceholder API
and saves to Google Sheets
```

### Example 2: AI Customer Support
```
Build an AI agent using Claude 3.5 Sonnet that can:
- Answer questions from knowledge base
- Create support tickets
- Escalate to human if uncertain
```

### Example 3: Scheduled Data Sync
```
Create a workflow that runs daily, syncs Airtable to
PostgreSQL with error notifications to Slack
```

---

## Files Added

```
.claude/
├── skills/
│   ├── n8n-workflow-builder.md      # Claude Code skill
│   └── skill.json
├── README.md
└── QUICKSTART.md

langchain-agent/
├── workflow_builder_agent.py         # Main Python agent
├── requirements.txt
├── setup.sh                          # Automated setup
├── README.md                         # RTX 5090 guide
└── REPO-ORGANIZATION.md              # Org recommendations

workflows/
├── demo-hello-world.json
└── meta-workflow-generator.json      # Meta workflow

COMPARISON-CLAUDE-VS-LOCAL.md         # Detailed comparison
fix-repo-push.sh                      # Git remote fix script
```

---

## Usage

### With Claude Code (Development)
```
You: Create a webhook workflow that receives Stripe payments
     and sends thank you emails

Claude: [Creates complete workflow JSON ready to import]
```

### With Local Agent (Production)
```bash
python workflow_builder_agent.py \
    --model-name qwen2.5:72b \
    --query "Create GitHub issues to Slack workflow"
```

### With n8n Meta Workflow
1. Import `workflows/meta-workflow-generator.json`
2. Configure Ollama node
3. Chat to generate workflows!

---

## Next Steps

1. ✅ Try Claude Code skill for development
2. ⚙️ Set up local agent for production/scale
3. 🎯 Use hybrid approach for best results

---

## Hybrid Approach (Recommended)

```
Development → Claude Code Skill (best quality)
    ↓
Production → Local Agent (unlimited scale)
```

Both options complement each other perfectly!

---

**Implements both cloud (Claude API) and local (RTX 5090) approaches for maximum flexibility and cost optimization.**
