# n8n Starter Pack — 3 production-ready workflow templates

[![validate-workflows](https://github.com/jian1929/n8n-starter-pack/actions/workflows/validate.yml/badge.svg)](https://github.com/jian1929/n8n-starter-pack/actions/workflows/validate.yml)

> **Import. Click Execute. It runs with zero credentials.** Replace the clearly-marked steps with your own tools to go live.
> 导入即用：三个模板都不依赖任何外部凭证即可运行；生产化替换点已在节点注释中标注。

**Tested:** imported + executed successfully on n8n 2.40.7 (2026-10-12). 已在 n8n 2.40.7 实测导入与执行成功。

## What's inside | 包含什么

| # | Workflow | Trigger | What it does |
|---|---|---|---|
| 01 | Lead Instant Response | Webhook `POST /lead-instant-response` | normalize + score leads → route high/low priority actions |
| 02 | Daily Digest | Schedule (daily) | pull sample metrics → compile a Markdown digest |
| 03 | KB FAQ Chatbot | Webhook `POST /kb-chat` | keyword retrieval over a mini knowledge base → auto-answer or escalate |

## Quick start | 快速开始

1. n8n → Workflows → ⋯ → **Import from File** → pick a JSON（或直接复制 JSON 粘贴新建）
2. Open it → click **Execute workflow**（01/03 可在 Webhook 面板发一条样例请求）
3. Swap the marked steps (comments say exactly what to replace).

## Production notes | 生产化提示

- **01** — replace the scoring rules with your own AI endpoint; wire the two action branches to your CRM / Slack / SMS.
- **02** — replace the sample data-fetch with your real source (DB / sheet / API); send the digest via Email / Slack / ntfy.
- **03** — replace the mini KB with a vector store or your FAQ table; connect an LLM (HTTP Request node) for generation.

## License | 许可证

MIT — use them, fork them, ship them. See [LICENSE](LICENSE).

## Need one built and hardened for you? | 需要定制？

I run a one-person AI studio: fixed price, 5-day delivery, walkthrough video + docs included.
https://jian1929.github.io/ai-studio-site/

---
*Maintained by [@jian1929](https://github.com/jian1929) · templates extracted from real client-pattern builds.*