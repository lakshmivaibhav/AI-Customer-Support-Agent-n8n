#  AI Customer Support Agent

An AI-powered Customer Support Agent built using **n8n**, **Ollama**, and **Notion**.

This workflow provides intelligent customer support by answering FAQs from a Notion Knowledge Base, maintaining conversation state, collecting customer information, and automatically creating support tickets when an answer cannot be found.

---

# Features

- ✅ Stateful conversations using Notion
- ✅ AI-powered FAQ retrieval
- ✅ Category-based knowledge search
- ✅ Automatic support ticket creation
- ✅ Customer email collection
- ✅ Conversation state management
- ✅ Notion Knowledge Base integration
- ✅ Support Ticket database
- ✅ Session tracking
- ✅ Multi-step workflow automation

---

# Technologies Used

- n8n
- Ollama
- Notion
- JavaScript
- AI Agents
- Workflow Automation

---

#  Screenshots

## Workflow

![Workflow](images/workflow.png)

---

## Knowledge Base

![Knowledge Base](images/knowledge-base.png)

---

## Support Tickets

![Support Tickets](images/support-tickets.png)

---

## Chat Demo

![Chat Demo](images/chat-demo.png)

---

## Architecture

```text
User
  │
  ▼
n8n Chat Trigger
  │
  ▼
Conversation State (Notion)
  │
  ▼
Knowledge Base Search
  │
  ▼
AI Agent
  │
  ▼
Answer Found?
   ├── Yes ──► Reply to User
   │
   └── No
        │
        ▼
Category Selection
        │
        ▼
Category Search
        │
        ▼
AI Agent
        │
        ▼
Answer Found?
   ├── Yes ──► Reply to User
   │
   └── No
        │
        ▼
Create Support Ticket
        │
        ▼
Collect Customer Email
        │
        ▼
Store Ticket in Notion
        │
        ▼
Reset Conversation State
```
#  Workflow Overview

1. User asks a question.
2. AI searches the Knowledge Base.
3. If an answer exists:
   - Responds immediately.
4. If no answer exists:
   - Requests a category.
5. Searches again using the selected category.
6. If still no answer:
   - Offers support ticket creation.
7. If accepted:
   - Collects customer email.
   - Creates a support ticket.
   - Resets the conversation.

---

## Demo Conversation

```text
User:
Where is your office?

↓

AI:
I couldn't find an exact answer.

Which category best matches your issue?

Account
Billing
Subscription
Technical
General

Please type the category name.

↓

User:
General

↓

AI:
I still couldn't find an answer to your question.

Would you like me to create a support ticket?

Please type:

Yes

or

No

↓

User:
Yes

↓

AI:
Your support ticket has been created successfully.

Status: Open

Our support team will review your request and get back to you as soon as possible.

Please provide your email address so that we can contact you.

↓

User:
vaibhav@gmail.com

↓

AI:
Thank you.

Your email has been recorded successfully.

Our support team will contact you regarding your ticket.

If you have another question, type Hello to start a new conversation.
```

#  Repository Structure

```
AI-Customer-Support-Agent-n8n
│
├── images/
├── workflow/
│   └── Customer_Support_Agent.json
├── README.md
└── LICENSE
```

---

#  Import Workflow

1. Download the workflow JSON.
2. Open n8n.
3. Click **Import Workflow**.
4. Configure your Notion credentials.
5. Configure your Ollama connection.
6. Start chatting.

---

#  Future Improvements

- Human agent dashboard
- Email notifications
- Slack integration
- Admin panel
- Analytics dashboard
- Semantic vector search

---

#  Author

**Vaibhav**

Built using n8n + Ollama + Notion.
