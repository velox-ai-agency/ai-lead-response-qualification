# 🤖 AI Lead Response & Qualification System

> ⚠️ **STATUS: CONCEPT/TEMPLATE ONLY - NOT TESTED**
> 
> This repository contains concept documentation and templates only. 
> The n8n workflow JSON is NOT ready for import - it needs to be built manually on n8n.

Automated lead capture, qualification, and intelligent routing system for Velox AI Agency.

## ⚡ Quick Overview

```
Lead lands on Form → AI analyzes → Qualification Score → Smart Action
```

## 🏗️ System Architecture

```
Google Form → Google Sheets → n8n Webhook → Claude AI → Router → Email Action
                                                    ↓
                               ┌────────────────────┼────────────────────┐
                               ▼                    ▼                    ▼
                            🔥 HOT              🌡️ WARM              ❄️ COLD
                          (Calendar)          (Discovery)          (Nurture)
```

## 📦 Repository Contents

| File | Status | Description |
|------|--------|-------------|
| `docs/google-form-setup.md` | ✅ Ready | Google Form configuration |
| `docs/setup-checklist.md` | ✅ Ready | Step-by-step setup guide |
| `prompts/lead-qualification-prompt.md` | ✅ Ready | Claude AI prompt template |
| `n8n-workflows/lead-qualification-workflow.json` | ❌ **CONCEPT** | Template - needs manual build |

## ⚠️ What's Missing (To Build)

### 1. Real n8n Workflow
The JSON file is a **concept/template**. To make it work:
- [ ] Go to n8n.veloxai.work
- [ ] Create workflow manually
- [ ] Add Webhook node
- [ ] Add Claude/OpenAI node with prompt
- [ ] Add Switch/Router node
- [ ] Add Email nodes (3 branches)
- [ ] Configure credentials
- [ ] Test end-to-end

### 2. Credentials Setup
- [ ] Claude/OpenAI API key
- [ ] SMTP email credentials
- [ ] Google Sheets connection

### 3. Google Form
- [ ] Create the actual form
- [ ] Connect to Google Sheets
- [ ] Add n8n webhook trigger

## 📋 Next Steps

1. **Review** `docs/setup-checklist.md`
2. **Build** the workflow on n8n manually
3. **Test** with sample leads
4. **Export** working JSON from n8n
5. **Replace** the concept file with real one

---
**Built with ❤️ by Velox AI Agency**
