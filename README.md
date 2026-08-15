# AI Chatbot Backend

Custom AI-powered chatbot backend that handles customer inquiries 24/7
for businesses. Built with Flask, integrated with AI
providers (Claude/ Gemini/ DeepSeek), deployed on Render.

## What It Does

- Handles common customer questions automatically (hours, services,
  pricing, booking, eligibility)
- Works 24/7 — captures leads and answers questions outside business hours
- Supports Claude, Gemini, and DeepSeek — provider selected during
  setup based on your budget and needs
- Session-based conversation memory so customers can have natural
  back-and-forth conversations
- Custom system prompts tailored to each client's business
- Admin panel where you can review real customer conversations and
  see exactly what your clients are asking about

## Tech Stack

- **Backend:** Python (Flask)
- **Database:** PostgreSQL
- **AI Providers:** Anthropic Claude / Google Gemini / DeepSeek
- **Deployment:** Render
- **Frontend Widget:** Vanilla JavaScript (embeddable via CDN)

## Safety Features

- **Trigger-word filtering:** high-risk topics are detected before
  reaching the AI model, returning a pre-written safety response
  that directs the user to contact the business directly
- **System prompt hardening:** narrow scope defined per client so
  the chatbot stays on-topic and refuses out-of-scope requests
- **Rate limiting** on all API endpoints to prevent spam and abuse
- **Request logging** for monitoring and manual review
- **Visible disclaimers** on the chat widget

## Integration

The chatbot is delivered as an embeddable JavaScript widget. Adding it
to a client site is a single `<script>` tag:

```html
<script src="https://cdn.jsdelivr.net/gh/tnoshin/chatbot-widget@v1.0.0/widget.js"
    data-backend="https://your-backend.onrender.com"
    data-title="Your Business Assistant"
    data-welcome="Hi! How can I help you today?"
    data-color="#0891b2"
></script>
```

Works on WordPress (via WPCode plugin), custom HTML/CSS/JS sites,
React, Vue, and other JavaScript frameworks.

## Customization

Every aspect of the widget is configurable via `data-` attributes —
no code editing required. Customizeable according to client's website theme.

## Live Demo

- Dental clinic demo: [BrightSmile Dental](https://brightsmile-dental-demo.onrender.com/)

## Why Add a Chatbot?

- Answers repetitive questions instantly so your team
  can focus on real client work
- Guides visitors to the right service, form, or
  booking page
- Available 24/7 — captures leads outside business
  hours when competitors' phones go to voicemail
- Gives you data on what customers actually ask about,
  straight from the admin panel


**Important:** AI chatbots can occasionally generate inaccurate
information. This is a known limitation of all AI language models,
not specific to this product. To minimize risk, every deployment
includes system prompt constraints that keep responses within
your business's scope, trigger-word filtering for sensitive
topics, and visible disclaimers on the chat widget advising
users to verify critical information directly with your business.
This chatbot is designed to assist with common inquiries, not
to replace professional advice.

*This is a demonstration version. Production deployments are 
customized per client with business-specific system prompts, 
trigger words, safety layers, and integration.*
