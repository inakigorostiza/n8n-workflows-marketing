# n8n Workflows for Marketing

A growing library of production-ready n8n workflows, written as guided case studies for the **AI Marketing Lab** at **IE Business School**.

Each workflow ships with:

- The **raw JSON** you can import into n8n.
- A plain-language **anatomy** of every node.
- A **step-by-step build from scratch** so students can rebuild it and understand the craft.

| | |
|---|---|
| 🌐 **Live site** | [inakigorostiza.github.io/n8n-workflows-marketing](https://inakigorostiza.github.io/n8n-workflows-marketing/) |
| 📖 **Companion project** | [RC Celta Seat Availability Alert Platform](https://github.com/inakigorostiza/rc-celta-seat-availability-alert-platform) |

## Catalogue

| # | Workflow | What it does | Nodes |
|---|----------|--------------|-------|
| 01 | [Trending topics → Blog + X post](workflows/youtube-trends-blog-x.html) | Pulls YouTube + Google Trends, drafts copy with GPT-4.1-mini, publishes via Blogger + Buffer. | 14 |
| 02 | [AI Viral Video — NanoBanana × Veo 3.1 × Buffer](workflows/ai-viral-video.html) | Telegram-triggered: reference image + caption → Gemini NanoBanana still → Google Veo 3.1 video (9:16 / 8s) → published to X via Buffer. | 29 |

## Credentials

Every external service used by the library is documented in **[credentials.html](credentials.html)** — step-by-step setup for OpenAI, Google Cloud (YouTube + Sheets + Blogger), Buffer, and how to link each one in n8n's credentials panel. A quick-glance checklist at the bottom summarises which tokens, IDs and placeholders a given workflow needs.

## How to use a workflow

1. Open the guide page (linked above).
2. Download the `.json` file linked at the top.
3. In n8n → **Workflows → Import from File** → pick the JSON.
4. Replace every `REPLACE_WITH_*` placeholder with your own IDs and tokens.
5. Link the credentials the workflow asks for (each one is explained in the guide's §02 Prerequisites section).
6. Execute.

## Repository layout

```
n8n-workflows-marketing/
├── index.html                        # Catalogue landing page
├── workflows/
│   ├── youtube-trends-blog-x.html    # Guide for workflow 01
│   └── youtube-trends-blog-x.json    # Importable workflow file
├── assets/
│   ├── styles.css                    # Shared IE design system
│   ├── ie-logo.svg
│   └── claude-logo.svg
└── README.md
```

## License

Reference material for educational purposes. Each external service (YouTube, Google Sheets, OpenAI, Blogger, Buffer) has its own terms — check them before running the workflow on production data.
