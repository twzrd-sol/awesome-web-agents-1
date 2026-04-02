# Awesome Web Agents [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> A curated list of web agent frameworks, tools, benchmarks, and research papers.

Web agents are AI systems that can browse, interact with, and automate tasks on websites. This list covers the full spectrum — from research prototypes to production platforms.

**Maintained by [Pantheon AI](https://pantheonai.co.uk)** — we build deterministic web agents that run on small, locally-hosted models.

## Contents

- [Frameworks & Platforms](#frameworks--platforms)
  - [Production Platforms](#production-platforms)
  - [Open-Source Frameworks](#open-source-frameworks)
  - [Scraping & Data Extraction](#scraping--data-extraction)
- [Benchmarks](#benchmarks)
- [Anti-Bot & Evasion](#anti-bot--evasion)
- [Research Papers](#research-papers)
- [LLM Integration](#llm-integration)
- [Cost & Architecture Comparison](#cost--architecture-comparison)
- [Contributing](#contributing)

## Frameworks & Platforms

### Production Platforms

- [Pantheon AI](https://pantheonai.co.uk) — Deterministic web automation via network-level API interception. Record once with a frontier model, replay with small local models. On-prem deployable. 81% WebArena.
- [BrowserBase](https://browserbase.com) — Cloud browser infrastructure for AI agents. Managed headless browsers with session management.
- [Induced AI](https://induced.ai) — AI-powered platform combining browser automation with human-in-the-loop workflows.
- [MultiOn](https://theagi.company) — AI agent platform for autonomous web task completion. Formerly multion.ai.
- [Convergence AI](https://convergence.ai) — Autonomous web agents for enterprise automation.

### Open-Source Frameworks

- [Browser Use](https://github.com/browser-use/browser-use) — Open-source web agent framework with multi-LLM support. 85k+ stars.
- [Crawlee](https://crawlee.dev) — Web scraping and browser automation library by Apify. Built-in anti-blocking.
- [LaVague](https://github.com/lavague-ai/LaVague) — Large Action Model framework for building web agents with LLMs. Supports Selenium and Playwright.
- [Playwright](https://playwright.dev) — Cross-browser automation library by Microsoft. The industry standard for programmatic browser control.
- [Puppeteer](https://pptr.dev) — Chrome/Chromium automation by Google. Tight Chrome DevTools Protocol integration.
- [Selenium](https://selenium.dev) — The original browser automation framework. Massive ecosystem, broad language support.
- [Skyvern](https://github.com/skyvern-ai/skyvern) — AI agent for browser automation using LLMs and computer vision. 21k+ stars.
- [Agent-Q](https://github.com/sentient-engineering/agent-q) — Research agent using Monte Carlo tree search and DPO fine-tuning for web tasks.

### Scraping & Data Extraction

- [Apify](https://apify.com) — Web scraping and automation platform with actor model.
- [Bright Data](https://brightdata.com) — Proxy network and web scraping infrastructure.
- [Crawl4AI](https://github.com/unclecode/crawl4ai) — Open-source LLM-friendly web crawler. Converts pages to clean markdown. 63k+ stars.
- [Firecrawl](https://firecrawl.dev) — Turn websites into LLM-ready data. Handles JS rendering and anti-bot.
- [ScrapingBee](https://scrapingbee.com) — Web scraping API with headless browser and proxy rotation.

## Benchmarks

- [WebArena](https://webarena.dev) — Realistic web environment benchmark for autonomous agents. 812 tasks across real websites. NeurIPS 2024.
- [pantheon-webarena](https://github.com/pantheon-auto/pantheon-webarena) — Vendor-neutral benchmark harness. Run any agent against WebArena tasks with standardized metrics.
- [VisualWebArena](https://jykoh.com/vwa) — Extension of WebArena focusing on visually grounded tasks. 910 tasks. ACL 2024.
- [Mind2Web](https://osu-nlp-group.github.io/Mind2Web/) — Large-scale dataset for web agents with 2,000+ tasks across 137 websites.
- [WebVoyager](https://github.com/MinorJerry/WebVoyager) — End-to-end web agent benchmark using real-world websites. 643 tasks across 15 sites.
- [WorkArena](https://github.com/ServiceNow/WorkArena) — Benchmark for web agents on enterprise applications (ServiceNow). ICML 2024.

## Anti-Bot & Evasion

Understanding bot detection is essential for building robust web agents.

- [Botright](https://github.com/Vinyzu/Botright) — Playwright-based stealth browsing with built-in CAPTCHA solving.
- [Camoufox](https://github.com/daijro/camoufox) — Anti-fingerprinting Firefox build for web scraping. C++-level fingerprint spoofing.
- [undetected-chromedriver](https://github.com/ultrafunkamsterdam/undetected-chromedriver) — Selenium-based approach to avoiding bot detection.
- [Cloudflare Turnstile](https://www.cloudflare.com/products/turnstile/) — CAPTCHA alternative. A common challenge for web agents to handle.
- [HUMAN (PerimeterX)](https://www.humansecurity.com/) — Bot detection platform. Widely deployed across enterprise sites.
- [Akamai Bot Manager](https://www.akamai.com/products/bot-manager) — Enterprise bot detection and management.

## Research Papers

- [WebArena: A Realistic Web Environment for Building Autonomous Agents](https://arxiv.org/abs/2307.13854) (2023) — The foundational benchmark paper for web agent evaluation.
- [Mind2Web: Towards a Generalist Agent for the Web](https://arxiv.org/abs/2306.06070) (2023) — Large-scale web agent dataset and model.
- [A Real-World WebAgent with Planning, Long Context Understanding, and Program Synthesis](https://arxiv.org/abs/2307.12856) (2023) — Google DeepMind's WebAgent.
- [SeeAct: GPT-4V(ision) is a Generalist Web Agent, if Grounded](https://arxiv.org/abs/2401.01614) (2024) — Vision-based web agent grounding approach.
- [Agent-E: From Autonomous Web Agent to Your Conversational Assistant](https://arxiv.org/abs/2407.13032) (2024) — Convergence AI's research on conversational web agents.
- [Tree Search for Language Model Agents](https://arxiv.org/abs/2407.01476) (2024) — Search-based planning for web agents.
- [Agent Q: Advanced Reasoning and Learning for Autonomous AI Agents](https://arxiv.org/abs/2408.07199) (2024) — Monte Carlo tree search with DPO for web agent training.

## LLM Integration

- [Claude Computer Use](https://docs.anthropic.com/en/docs/build-with-claude/computer-use) — Anthropic's API for controlling desktop and browser via screenshots and actions.
- [LangChain](https://langchain.com) — Framework for building LLM applications. Includes web browsing tools and agent primitives.
- [OpenAI Assistants](https://platform.openai.com/docs/assistants) — OpenAI's agent framework with tool use capabilities.
- [Semantic Kernel](https://github.com/microsoft/semantic-kernel) — Microsoft's AI orchestration framework for building agents.

## Cost & Architecture Comparison

| Approach | Latency | Cost/Task | Determinism | Anti-Bot | On-Prem |
|----------|---------|-----------|-------------|----------|---------|
| Screenshot + GPT-4V | High | $0.10–0.50 | Low | Low | No |
| Screenshot + Claude | High | $0.05–0.30 | Low | Low | No |
| DOM parsing + LLM | Medium | $0.02–0.10 | Medium | Low | Partial |
| Network interception + small model | Low | $0.001–0.01 | High | High | Yes |
| Traditional automation (Selenium) | Low | ~$0 | High | Low | Yes |

## Contributing

Contributions welcome! Please read the [contribution guidelines](CONTRIBUTING.md) first.

## License

[![CC0](https://licensebuttons.net/p/zero/1.0/88x31.png)](https://creativecommons.org/publicdomain/zero/1.0/)

To the extent possible under law, [Pantheon AI](https://pantheonai.co.uk) has waived all copyright and related or neighboring rights to this work.
