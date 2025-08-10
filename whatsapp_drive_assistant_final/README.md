# WhatsApp-Driven Google Drive Assistant (n8n Workflow)

## 🚀 Overview
This project automates Google Drive file operations via WhatsApp commands using Twilio, n8n, and OpenAI.

## 🛠 Requirements
- Docker & Docker Compose
- Twilio account (Sandbox mode)
- Google API credentials (OAuth2)
- OpenAI API key (for GPT-4o)

## 🧪 Supported Commands via WhatsApp
- `LIST /folder`
- `DELETE /folder/file.pdf`
- `MOVE /from/file.pdf /to`
- `SUMMARY /folder`

## 📝 Setup Instructions
1. Duplicate `.env.sample` to `.env` and fill in credentials.
2. Start n8n:
   ```bash
   docker-compose up -d
   ```
3. Import `workflow.json` into n8n UI.
4. Enable your workflow.
5. Test via Twilio Sandbox (WhatsApp).

## 📄 Notes
- All commands are logged for audit.
- SUMMARY uses OpenAI GPT-4o for bullet-style digest.
