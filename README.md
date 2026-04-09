# 🤖 AI Lead Response & Qualification System

> ✅ **STATUS: REAL WORKFLOW - Ready for Import**
> 
> This repository contains a fully functional n8n workflow that can be imported and used immediately.

Automated lead capture, qualification, and intelligent routing system for Velox AI Agency.

## ✨ What's Included

| Component | Status | Description |
|-----------|--------|-------------|
| **n8n Workflow** | ✅ **REAL** | 9-node workflow, import-ready |
| **Setup Guide** | ✅ Complete | Step-by-step instructions |
| **AI Prompt** | ✅ Complete | Claude qualification prompt |
| **Google Form** | ✅ Template | Ready to deploy |

## ⚡ Quick Overview

```
Lead lands on Form → AI analyzes → Qualification Score → Smart Action
```

**Timeline**: Response < 60 seconds | Qualification instant | Routing automatic

## 🏗️ System Architecture

```
Google Form → Webhook → Claude AI → Router → Email Action
                                        ↓
                    ┌──────────────────┼──────────────────┐
                    ▼                  ▼                  ▼
                 🔥 HOT             🌡️ WARM            ❄️ COLD
              (Calendar)         (Discovery)         (Nurture)
```

## 📦 Repository Structure

```
├── 📁 n8n-workflows/
│   └── lead-qualification-workflow.json    ✅ REAL WORKFLOW (import ready)
├── 📁 docs/
│   ├── google-form-setup.md               ✅ Form configuration
│   └── setup-checklist.md                 ✅ Setup tracking
├── 📁 prompts/
│   └── lead-qualification-prompt.md       ✅ Claude prompt
└── README.md                             ✅ This file
```

## 🚀 Quick Start

### 1. Import to n8n
```bash
1. Go to n8n.veloxai.work
2. Add workflow → Import from file
3. Select: lead-qualification-workflow.json
```

### 2. Configure Credentials
- **Claude API**: Get from https://console.anthropic.com
- **SMTP**: Your email provider settings

### 3. Test
```bash
curl -X POST "YOUR_WEBHOOK_URL"   -H "Content-Type: application/json"   -d '{"name":"Test","email":"test@test.com","budget":"$5000+","timeline":"ASAP","project":"AI automation"}'
```

### 4. Connect Form
See `docs/google-form-setup.md` for complete form setup.

## 🎯 Qualification Criteria

| Score | Category | Response | Action |
|-------|----------|----------|--------|
| 80-100 | 🔥 HOT | < 60 sec | Direct booking |
| 50-79 | 🌡️ WARM | < 2 hours | Case studies + follow-up |
| 0-49 | ❄️ COLD | < 24 hours | Nurture sequence |

## 📊 Workflow Nodes (9 Total)

1. **Lead Webhook** - POST endpoint for form data
2. **Prepare Data** - Extract and clean fields
3. **AI Qualification** - Claude API scoring
4. **Parse Response** - Extract JSON from AI output
5. **Router** - HOT/WARM/COLD switch
6. **HOT Email** - Priority response
7. **WARM Email** - Education + discovery
8. **COLD Email** - Nurture intro
9. **Response** - Success JSON to caller

## 🔧 Requirements

- n8n server (self-hosted or cloud)
- Anthropic Claude API key
- SMTP email credentials
- Cal.com/Calendly for HOT leads

## 📚 Documentation

- [Setup Guide](docs/setup-checklist.md)
- [Google Form Setup](docs/google-form-setup.md)
- [AI Prompt](prompts/lead-qualification-prompt.md)

---
**Built with ❤️ by Velox AI Agency**

Last updated: 2026-04-09
