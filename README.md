<picture>
  <source media="(prefers-color-scheme: dark)" srcset="./assets/header-dark.svg">
  <img alt="..." src="./assets/header-light.svg" width="100%">
</picture>

<p>
  <a href="https://nestjs.com"><img alt="NestJS" src="https://img.shields.io/badge/NestJS-E0234E?style=flat-square&logo=nestjs&logoColor=white"></a>
  <a href="https://www.typescriptlang.org"><img alt="TypeScript" src="https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white"></a>
  <a href="https://www.postgresql.org"><img alt="PostgreSQL" src="https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white"></a>
  <a href="https://graphql.org"><img alt="GraphQL" src="https://img.shields.io/badge/GraphQL-E10098?style=flat-square&logo=graphql&logoColor=white"></a>
  <a href="https://bullmq.io"><img alt="BullMQ" src="https://img.shields.io/badge/BullMQ-DC382D?style=flat-square&logo=redis&logoColor=white"></a>
  <a href="https://redis.io"><img alt="Redis" src="https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white"></a>
  <img alt="RAG" src="https://img.shields.io/badge/RAG-7C3AED?style=flat-square">
  <img alt="LLM" src="https://img.shields.io/badge/LLM-0A0A0A?style=flat-square">
</p>

8+ years on production backends. I own multi-tenant SaaS architecture from database schema to deployment, with a recent focus on production AI: a provider-agnostic LLM layer, RAG, and failure containment. Backend Lead Engineer at MicroAgility Services, Jan 2024 – Present. Based in Islamabad (UTC+5), with working hours aligned to EST/PST for US and Canada remote teams.

> [!IMPORTANT]
> **Case study · [Designing for AI Failure](https://juh-bukhari.vercel.app/case-study)**
> How the Talentnix AI gateway kept answering through live LLM outages: Retry across OpenAI, Gemini and Anthropic → RAG Fallback → Rule-Based Floor. Result: **zero AI failures during live LLM outages**.

### Impact, in numbers

| Result | System |
| --- | --- |
| Dashboard load **from 12s to under 2s (83%)** | PostgreSQL and MongoDB query tuning, new indexes, MeiliSearch rollout |
| **Cut AI integration complexity by 60%** | Talentnix AI gateway: OpenAI, Gemini and Anthropic behind one routing layer with automatic failover |
| **Zero AI failures during live LLM outages** | Retry → RAG Fallback → Rule-Based Floor |
| **No cross-tenant data exposure incidents to date** | Tenant isolation across REST and GraphQL APIs with OAuth 2.0/JWT |
| **APIs under a second while thousands of async jobs run concurrently** | Event-driven BullMQ and Redis job pipeline |
| Mentoring **three associate backend developers** | Learning & Development programme |

### Agentic loops I build

**One agent: plan, act, observe, reflect.** Each pass ends in Reflect: loop again with what was learned, or stop and respond. Illustrative run from the internal ATS (Claude Code + Gemini 2.5 Flash).

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="./assets/agent-loop-dark.svg">
  <img alt="Agent loop cycling through plan, act (tool call), observe and reflect" src="./assets/agent-loop-light.svg" width="100%">
</picture>

**A team of agents on one bus.** Planner, Retriever (RAG), Tool runner (MCP) and Critic exchange tasks through BullMQ and Redis until the Critic approves.

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="./assets/agent-swarm-dark.svg">
  <img alt="Planner, Retriever, Tool runner and Critic agents exchanging messages over a BullMQ and Redis bus" src="./assets/agent-swarm-light.svg" width="100%">
</picture>

**The fallback chain behind every agent call.** Two retries per provider, a circuit breaker opens, the call moves on. With every LLM provider down, the RAG Fallback answers; the Rule-Based Floor answers last.

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="./assets/fallback-chain-dark.svg">
  <img alt="Fallback chain: OpenAI, Gemini and Anthropic fail in turn, then the RAG Fallback answers" src="./assets/fallback-chain-light.svg" width="100%">
</picture>

### Public projects

Personal builds, public and verifiable. Client systems are under NDA, so they appear only as architecture.

| Project | What it does | Link |
| --- | --- | --- |
| Omni.io | Multi-tenant RAG support engine with a three-tier resilience ladder, Postgres row-level-security isolation, an embeddable widget and an MCP server. | Private repo |
| TalntFlow AI | Lightweight ATS with a Kanban pipeline, STAR scorecards, hiring analytics and an approval-based recruiting agent on Claude with a rules fallback. | [Live ↗](https://talntflow-ai.vercel.app) · [Source](https://github.com/JawadulHadi/talnt-flow-ai) |
| Scanwise | Turns scans, PDFs and Office files into one cited summary and a source-grounded chat, with on-device OCR. | [Live ↗](https://scanwise-io.vercel.app) · [Source](https://github.com/JawadulHadi/scanwise) |
| Catchbox | Human-in-the-loop safety net for web scrapers: failed scrapes land in an inbox, a person fixes them, and only approved records count as data. | [Live ↗](https://catch-box.vercel.app) · [Source](https://github.com/JawadulHadi/catch-box) |
| Scrapefix | The first build of the scraper-triage dashboard: fix queue, record review and a personal ingest key for any scraper. | [Source](https://github.com/JawadulHadi/scrapio) |
| Taskmaster Agent | Hackathon entry: an event-driven HR operations agent on Genkit and Gemini over Pub/Sub, with a manager-approval pause when it finds a policy violation. | [Source](https://github.com/JawadulHadi/taskmaster-agent) |
| GitHub Glow-Up | Workspace for repository documentation: README drafts, code reports that separate verified facts from AI interpretation, and publishing to GitHub. | [Live ↗](https://repo-glow-io.lovable.app) · [Source](https://github.com/JawadulHadi/git-glow) |
| Verdict | Tamper-evident decision engine that issues hash-chained, signed reasoning receipts for EU AI Act record-keeping. | [Live ↗](https://qeloma-verdict.vercel.app/) · [Source](https://github.com/Qeloma/qeloma-verdict) |
| Lens Studio | Summarise, extract and compare across PDFs, DOCX and images on Gemini, with deterministic fallbacks. | [Live ↗](https://qelomalens.vercel.app/) · [Source](https://github.com/Qeloma/qeloma_lens_studio) |
| Voice Studio | Real-time voice analyst on the Gemini Live API that answers from your own documents. | [Live ↗](https://qeloma-voice.vercel.app/) · [Source](https://github.com/Qeloma/qeloma_voice_studio) |
| Shift | Semantic diffing for contracts and configs that ranks changes by materiality and explains business impact. | [Live ↗](https://qeloma-shift.vercel.app/) · [Source](https://github.com/Qeloma/qeloma_shift) |
| Cover Studio | Browser-based LinkedIn banner designer with an AI copywriting assistant, safe-zone guides and high-resolution export. | [Live ↗](https://cover-studiio.vercel.app/) · [Source](https://github.com/Qeloma/qeloma-cover-studio) |
| Qeloma Studio | In-browser photo and video editor on WebGPU, WebGL2 and WebAssembly, with local ONNX background removal. | [Source](https://github.com/Qeloma/Qeloma-Studio) |
| Qeloma Recruit | Angular ATS sandbox on Gemini: JD generator, STAR interview guides, scorecards and a five-stage pipeline. | [Source](https://github.com/Qeloma/qeloma-recruitment-sandbox) |
| Extension suite | Ten single-purpose Manifest V3 browser extensions built with WXT, local-first. | [Source](https://github.com/Qeloma/qeloma-extension-suite) |

### Stack

**Backend** -
<a href="https://nestjs.com"><img alt="NestJS" src="https://img.shields.io/badge/NestJS-E0234E?style=flat-square&logo=nestjs&logoColor=white"></a>
<a href="https://nodejs.org"><img alt="Node.js" src="https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=nodedotjs&logoColor=white"></a>
<a href="https://www.typescriptlang.org"><img alt="TypeScript" src="https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white"></a>
<a href="https://expressjs.com"><img alt="Express.js" src="https://img.shields.io/badge/Express.js-000000?style=flat-square&logo=express&logoColor=white"></a>
<a href="https://www.python.org"><img alt="Python" src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white"></a>
<a href="https://fastapi.tiangolo.com"><img alt="FastAPI" src="https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white"></a>
<a href="https://www.django-rest-framework.org"><img alt="Django REST" src="https://img.shields.io/badge/Django%20REST-092E20?style=flat-square&logo=django&logoColor=white"></a>

**Data** -
<a href="https://www.postgresql.org"><img alt="PostgreSQL" src="https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white"></a>
<a href="https://www.mysql.com"><img alt="MySQL" src="https://img.shields.io/badge/MySQL-4479A1?style=flat-square&logo=mysql&logoColor=white"></a>
<a href="https://www.mongodb.com"><img alt="MongoDB" src="https://img.shields.io/badge/MongoDB-47A248?style=flat-square&logo=mongodb&logoColor=white"></a>
<a href="https://redis.io"><img alt="Redis" src="https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white"></a>
<a href="https://bullmq.io"><img alt="BullMQ" src="https://img.shields.io/badge/BullMQ-DC382D?style=flat-square&logo=redis&logoColor=white"></a>
<a href="https://www.meilisearch.com"><img alt="MeiliSearch" src="https://img.shields.io/badge/MeiliSearch-FF5CAA?style=flat-square&logo=meilisearch&logoColor=white"></a>

**AI** -
<a href="https://openai.com"><img alt="OpenAI" src="https://img.shields.io/badge/OpenAI-412991?style=flat-square&logo=openai&logoColor=white"></a>
<a href="https://deepmind.google/technologies/gemini/"><img alt="Gemini" src="https://img.shields.io/badge/Gemini-8E75B2?style=flat-square&logo=googlegemini&logoColor=white"></a>
<a href="https://www.anthropic.com"><img alt="Anthropic" src="https://img.shields.io/badge/Anthropic-191919?style=flat-square&logo=anthropic&logoColor=white"></a>
<a href="https://www.anthropic.com/claude-code"><img alt="Claude Code" src="https://img.shields.io/badge/Claude%20Code-D97757?style=flat-square&logo=claude&logoColor=white"></a>
<a href="https://github.com/features/copilot"><img alt="GitHub Copilot" src="https://img.shields.io/badge/GitHub%20Copilot-000000?style=flat-square&logo=githubcopilot&logoColor=white"></a>

**Architecture** -
<img alt="Multi-tenant SaaS" src="https://img.shields.io/badge/Multi--tenant%20SaaS-0A0A0A?style=flat-square">
<img alt="Microservices" src="https://img.shields.io/badge/Microservices-0A0A0A?style=flat-square">
<img alt="Event-Driven" src="https://img.shields.io/badge/Event--Driven-0A0A0A?style=flat-square">
<img alt="REST API" src="https://img.shields.io/badge/REST%20API-0A0A0A?style=flat-square">
<a href="https://graphql.org"><img alt="GraphQL" src="https://img.shields.io/badge/GraphQL-E10098?style=flat-square&logo=graphql&logoColor=white"></a>

**Cloud & Delivery** -
<a href="https://aws.amazon.com"><img alt="AWS" src="https://img.shields.io/badge/AWS-232F3E?style=flat-square&logo=amazonwebservices&logoColor=white"></a>
<a href="https://cloud.google.com"><img alt="GCP" src="https://img.shields.io/badge/GCP-4285F4?style=flat-square&logo=googlecloud&logoColor=white"></a>
<a href="https://www.openstack.org"><img alt="OpenStack" src="https://img.shields.io/badge/OpenStack-ED1944?style=flat-square&logo=openstack&logoColor=white"></a>
<a href="https://www.docker.com"><img alt="Docker" src="https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white"></a>
<a href="https://kubernetes.io"><img alt="Kubernetes" src="https://img.shields.io/badge/Kubernetes-326CE5?style=flat-square&logo=kubernetes&logoColor=white"></a>
<a href="https://github.com/features/actions"><img alt="GitHub Actions" src="https://img.shields.io/badge/GitHub%20Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white"></a>
<a href="https://jestjs.io"><img alt="Jest" src="https://img.shields.io/badge/Jest-C21325?style=flat-square&logo=jest&logoColor=white"></a>
<a href="https://oauth.net/2/"><img alt="OAuth 2.0 / JWT" src="https://img.shields.io/badge/OAuth%202.0%20%2F%20JWT-3C3C3D?style=flat-square&logo=jsonwebtokens&logoColor=white"></a>

### Experience

- **Backend Lead Engineer**, MicroAgility Services (Pvt) Ltd. · Jan 2024 – Present · Talentnix (multi-tenant SaaS), APAC Management System (HRMS)
- **Backend Software Engineer**, MicroAgility Services (Pvt) Ltd. · Mar 2022 – Jan 2024 · iAgility and AgileBrains; 99.9% uptime with zero-downtime schema migrations on live multi-tenant databases
- **Software Engineer**, Market Icon · Aug 2018 – Mar 2022 · Distributed MEAN system on OpenStack, serverless AWS Lambda services

### Credentials

**74 Verified Credentials** · LinkedIn Learning 23 · Google Cloud Skills Boost 20 · IBM 14 · Anthropic 7 · Microsoft Learning 6 · 5 others → [full list](https://juh-bukhari.vercel.app/credentials) · [in this repo](./CERTIFICATIONS.md)

| Credential | Issuer | Completed |
| --- | --- | --- |
| [Claude Code in Action](https://academy.claude.com/verify/ff1b2c578e9794408a0ba9c5beedc928) | Anthropic | Aug 2026 |
| [Containers & Kubernetes Essentials](https://www.credly.com/badges/13300660-220e-4a01-ad7e-c4be671babf4) | IBM | Sep 2026 |
| [Gen AI: Beyond the Chatbot](https://www.skills.google/public_profiles/e7e2ac08-758d-47f5-af65-589153c6b873/badges/26965991) | Google | Aug 2026 |
| [Introduction to generative AI and agents](https://learn.microsoft.com/api/achievements/share/en-us/JawadUlHadi-0198/FEGYP6TX?sharingId=AFF773B6C8D61F92) | Microsoft Learning | Sep 2026 |

### GitHub activity

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="./profile-3d-contrib/profile-night-rainbow.svg">
  <img alt="3D contribution calendar with yearly contribution, star and fork counts" src="./profile-3d-contrib/profile-season-animate.svg" width="100%">
</picture>

### Find me

<p>
  <a href="https://juh-bukhari.vercel.app"><img alt="Portfolio" src="https://img.shields.io/badge/Portfolio-0A0A0A?style=flat-square&logo=vercel&logoColor=white" /></a>
  <a href="https://juh-bukhari.vercel.app/resume.pdf"><img alt="Résumé" src="https://img.shields.io/badge/R%C3%A9sum%C3%A9-4B5563?style=flat-square&logo=adobeacrobatreader&logoColor=white" /></a>
  <a href="https://juh-bukhari.vercel.app/case-study"><img alt="Case Study" src="https://img.shields.io/badge/Case%20Study-7C3AED?style=flat-square&logo=readthedocs&logoColor=white" /></a>
  <a href="https://linkedin.com/in/jawad-ul-hadi"><img alt="LinkedIn" src="https://img.shields.io/badge/LinkedIn-0A66C2?style=flat-square&logo=linkedin&logoColor=white" /></a>
  <a href="https://gitlab.com/JawadulHadi"><img alt="GitLab" src="https://img.shields.io/badge/GitLab-FC6D26?style=flat-square&logo=gitlab&logoColor=white" /></a>
  <a href="https://stackoverflow.com/users/19086162/jawad-ul-hadi"><img alt="Stack Overflow" src="https://img.shields.io/badge/Stack%20Overflow-F58025?style=flat-square&logo=stackoverflow&logoColor=white" /></a>
  <a href="https://orcid.org/0009-0007-1317-4615"><img alt="ORCID" src="https://img.shields.io/badge/ORCID-A6CE39?style=flat-square&logo=orcid&logoColor=white" /></a>
  <a href="https://calendly.com/jawadulhadicc"><img alt="Book a call" src="https://img.shields.io/badge/Book%20a%20call-006BFF?style=flat-square&logo=calendly&logoColor=white" /></a>
  <a href="https://mail.google.com/mail/?view=cm&fs=1&to=jawadulhadicc@gmail.com&su=Hello%20Jawad&body=Hi%20Jawad%2C%0A%0AI%20came%20across%20your%20profile." target="_blank">
  <img alt="Email" src="https://img.shields.io/badge/Email-EA4335?style=flat-square&logo=gmail&logoColor=white" />
</a>
</p>

<sub><i>Animations are plain SVG (CSS + SMIL), follow your GitHub light/dark theme, and stop when your system asks for reduced motion.</i></sub>
