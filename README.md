# Restaurant Full System — n8n

An end-to-end restaurant automation workflow built with **n8n**, **Telegram**, **AI Agents**, **Google Sheets**, and **OpenRouter**.

## Overview

This workflow receives customer messages through Telegram, classifies the customer's intent, and routes the conversation to an AI restaurant assistant.

The system supports:

- Customer order conversations
- Restaurant and menu questions
- Customer feedback and sentiment analysis
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
 ┌────┼────────────────┐
 ↓    ↓                ↓
Order  Restaurant      Feedback
       Question
 └────┴────────────────┘
            ↓
     Restaurant AI Agent
            ↓
   Google Sheets Tools



   --Main Components--

## AI Intent Classification

The first AI Agent classifies customer messages into:
-order
-restaurant_question
-feedback


## Restaurant AI Agent

-The main AI Agent manages the conversation and chooses the appropriate tool based on the customer's request.


## Tools

-"Get Menu" — retrieves menu items, prices, and availability.
-"Create Order" — stores confirmed customer orders.
-"Cancel Order" — updates an existing order to Canceled.
-"Order Status" — retrieves the current status of an order.
-"Feedbacks" — stores customer feedback and sentiment.


## Memory

-Conversation history is maintained for each Telegram chat using the Telegram chat ID as the session key.


## Requirements

-n8n
-Telegram Bot
-Google Sheets
-OpenRouter API or another compatible chat model
-Google Sheets OAuth2 credentials


## Setup

-Import restaurant-full-system-public.json into your n8n instance.
-Recreate the required credentials in your own n8n instance.
-Replace the placeholder Google Sheet identifiers with your own Sheets.
-Connect your Telegram credential.
-Connect your Google Sheets credential.
-Configure the chat model credential.
-Activate the workflow.


## Security

-This repository contains a sanitized public version of the workflow.

## Never commit:

-API keys
-Bot tokens
-OAuth client secrets
-Passwords
-Private URLs
-Production credentials
-Portfolio


## This project demonstrates practical experience with:

-n8n workflow automation
-AI Agents
-Intent classification
-AI tool calling
-Conversation memory
-Telegram integration
-Google Sheets integration
-Workflow routing
-Restaurant order automation
-Customer feedback handling


## License 

This repository contains an original workflow created for portfolio and learning purposes.