<<<<<<< HEAD
# Restaurant Full System — n8n

An end-to-end restaurant automation workflow built with **n8n**, **Telegram**, **AI Agents**, **Google Sheets**, and **OpenRouter**.

## Overview

This workflow receives customer messages through Telegram, classifies the customer's intent, and routes the conversation to an AI restaurant assistant.

The system supports:

- Customer order conversations
- Restaurant/menu questions
- Customer feedback and sentiment
- Order creation
- Order cancellation
- Order status lookup
- Google Sheets data storage
- Conversation memory
- AI tool calling

## Workflow

```text
Telegram Trigger
      ↓
Intent Classification (AI Agent)
      ↓
Switch
 ┌────┼───────────────┐
 ↓    ↓               ↓
Order  Restaurant      Feedback
       Question
 └────┴───────────────┘
            ↓
     Restaurant AI Agent
            ↓
   Google Sheets Tools
```

## Main Components

### AI Intent Classification
The first AI Agent classifies messages into:

- `order`
- `restaurant_question`
- `feedback`

### Restaurant AI Agent
The main agent handles customer conversations and chooses the appropriate tool.

### Tools

- **Get Menu** — reads menu items and prices.
- **Create Order** — stores confirmed orders.
- **Cancel Order** — updates an existing order to `Canceled`.
- **Order Status** — checks order status.
- **Feedbacks** — stores feedback and sentiment.

### Memory

Conversation history is maintained per Telegram chat using the Telegram chat ID as the session key.

## Requirements

- n8n
- Telegram Bot
- Google Sheets
- OpenRouter API (or another compatible chat model)
- Google Sheets OAuth2 credentials

## Setup

1. Import `restaurant-full-system-public.json` into n8n.
2. Recreate the required credentials in your own n8n instance.
3. Replace the placeholder Google Sheet IDs with your own Sheets.
4. Connect the Telegram credential.
5. Connect the Google Sheets credential.
6. Configure the chat model credential.
7. Activate the workflow.

## Security

This repository contains a **sanitized public version** of the workflow.

Before publishing, make sure you never commit:

- API keys
- Bot tokens
- OAuth client secrets
- Passwords
- Private URLs
- Production credentials

All credential references and private Google Sheet identifiers in the public JSON have been replaced with placeholders.

## Portfolio

This project demonstrates practical experience with:

- n8n workflow automation
- AI Agents
- Intent classification
- Tool calling
- Memory
- Telegram integration
- Google Sheets integration
- Workflow routing
- Customer order automation

## License

This repository contains an original workflow created for portfolio and learning purposes.
=======
# n8n-restaurant-ai-ordering-system
AI-powered restaurant ordering automation built with n8n, Telegram, Google Sheets, and AI Agents.
>>>>>>> 375381b8addfe3c5a03c68f960f309f7ed19d29f
