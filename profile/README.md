![SkyMetron](logo.svg)

# SkyMetron

AI Operating System — memória permanente, agentes especializados, autonomia controlada, LLM multi-provider **100% free** (R$ 0,00/mês).

**v0.1.0-beta** — [Release](https://github.com/SkyMetron/skymetron/releases/tag/v0.1.0-beta) · [Swagger UI](https://skymetron.dev/swagger-ui.html) · [CHANGELOG](https://github.com/SkyMetron/skymetron/blob/main/CHANGELOG.md)

---

## Ecossistema

| Repositório | Descrição |
|-------------|-----------|
| [skymetron](https://github.com/SkyMetron/skymetron) | Core Java (Spring Boot 3) + Desktop (Electron) + API REST |
| [sky-vault](https://github.com/SkyMetron/sky-vault) | Knowledge base Obsidian — 575+ markdowns, skills, sessões |
| [skymetron-docs](https://github.com/SkyMetron/skymetron-docs) | ADRs, documentação, arquitetura, roadmap |
| [skymetron-ai-services](https://github.com/SkyMetron/skymetron-ai-services) | Python/FastAPI — Ollama Bridge, embeddings, inferência |
| [skymetron-deployment](https://github.com/SkyMetron/skymetron-deployment) | Docker Compose, infraestrutura, scripts de deploy |
| [skymetron-monitoring](https://github.com/SkyMetron/skymetron-monitoring) | Grafana, Prometheus, Loki — observabilidade |
| [skymetron-vault](https://github.com/SkyMetron/skymetron-vault) | Configuração vault vetorial (pgvector, embeddings) |
| [skymetron-secrets](https://github.com/SkyMetron/skymetron-secrets) | Templates de secrets (nunca contém secrets reais) |

---

## Stack

**Java 21** · **Spring Boot 3.3.5** · **PostgreSQL 16 + pgvector** · **Redis 7** · **RabbitMQ 3.13** · **Electron 32** · **React 18** · **TypeScript** · **Vite 5** · **Docker**

---

## Arquitetura

```
┌──────────────┐    ┌────────────────┐    ┌───────────────┐
│  skymetron   │◄──►│ skymetron-ai   │◄──►│    Ollama     │
│  (Java Core) │    │ (Python/Fast)  │    │  (local LLM)  │
└──────┬───────┘    └────────────────┘    └───────────────┘
       │
┌──────▼───────┐    ┌────────────────┐    ┌───────────────┐
│  PostgreSQL  │    │     Redis      │    │   RabbitMQ    │
│  + pgvector  │    │   (cache)      │    │  (event bus)  │
└──────────────┘    └────────────────┘    └───────────────┘
       │
┌──────▼───────┐    ┌────────────────┐
│  skymetron-  │    │  skymetron-   │
│  monitoring  │    │  deployment   │
│ (Grafana +   │    │ (Docker +     │
│  Prometheus) │    │  infra)       │
└──────────────┘    └────────────────┘
```

---

## Roadmap

- **v0.1.0-beta** ✅ — Core, agentes, vault, observabilidade, desktop, deploy
- **v0.2.0** 🔄 — sky-vault API (busca semântica, RAG, embeddings)
- **v0.3.0** 📋 — Autonomia avançada, research swarm distribuído
- **v0.4.0** 📋 — Plugins / MCP, marketplace de skills

---

[sky-vault](https://github.com/SkyMetron/sky-vault) ·
[Documentação](https://github.com/SkyMetron/skymetron-docs) ·
[Deploy](https://github.com/SkyMetron/skymetron-deployment)

**In Veritas, Fundamentum.**
