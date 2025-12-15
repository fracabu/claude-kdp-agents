<h1 align="center">Claude KDP Agents</h1>
<h3 align="center">Multi-agent pipeline for Amazon KDP book creation</h3>

<p align="center">
  <em>Powered by Claude Code - From niche validation to ready-to-publish assets</em>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Claude_Code-8B5CF6?style=flat-square&logo=anthropic&logoColor=white" alt="Claude Code" />
  <img src="https://img.shields.io/badge/Amazon_KDP-FF9900?style=flat-square&logo=amazon&logoColor=white" alt="Amazon KDP" />
  <img src="https://img.shields.io/badge/Dual_Market-US_&_IT-blue?style=flat-square" alt="Dual Market" />
</p>

<p align="center">
  :gb: <a href="#english">English</a> | :it: <a href="#italiano">Italiano</a>
</p>

---

<a name="english"></a>
## :gb: English

### Overview

A multi-agent pipeline for Amazon Kindle Direct Publishing (KDP) book creation. Three specialized Claude agents work sequentially to take a book idea from market research to ready-to-publish assets, targeting both **Amazon.com (US)** and **Amazon.it (IT)** markets simultaneously.

```
┌─────────────────────────┐     ┌─────────────────────────┐     ┌─────────────────────────┐
│   Market Intelligence   │     │    Product Design       │     │     Publishing          │
│      Architect          │────▶│       Director          │────▶│   Optimization          │
│      (Phase 1)          │     │      (Phase 2)          │     │    Specialist           │
└─────────────────────────┘     └─────────────────────────┘     └─────────────────────────┘
         │                               │                               │
         ▼                               ▼                               ▼
   NICHE_REPORT_*.md            CONTENT_BLUEPRINT_*.md         PUBLISHING_PACKAGE_*.md
```

### Features

- **Dual Market Strategy** - Simultaneous optimization for US and IT with native Italian copywriting
- **Market Intelligence Agent** - Competitor analysis, BSR rankings, Google Trends, Go/No-Go decision
- **Product Design Agent** - Technical specs, AI image prompts, cover briefs, Canva workflow
- **Publishing Agent** - HTML descriptions, backend keywords, A+ Content briefs
- **KDP Compliance** - Accurate spine calculations, bleed specs, PDF requirements
- **SEO Optimization** - Backend keyword validation with byte-count verification

### Agents

| Agent | Phase | Output |
|-------|-------|--------|
| Market Intelligence Architect | 1 | `NICHE_REPORT_*.md` |
| Product Design Director | 2 | `CONTENT_BLUEPRINT_*.md` |
| Publishing Optimization Specialist | 3 | `PUBLISHING_PACKAGE_*.md` |

### Quick Start

```bash
# Prerequisites: Claude Code CLI installed

# Phase 1: Market Research
# Use market-intelligence-architect agent

# Phase 2: Product Design (after GO decision)
# Use product-design-director agent

# Phase 3: Publishing Package
# Use publishing-optimization-specialist agent
```

**Example Prompt:**
```
Analyze the "Mandala Flowers" niche for an adult coloring book,
8.5x8.5 inches, 104 pages, targeting US and IT markets at $9.99/€9.99
```

### Business Rules

| Spec | Value |
|------|-------|
| Trim Size | 8.5" x 8.5" |
| Pages | 104 |
| Bleed | 0.125" |
| Resolution | 300 DPI |
| US Price | $9.99 (60% royalty) |
| IT Price | €9.99 (60% royalty) |

---

<a name="italiano"></a>
## :it: Italiano

### Panoramica

Una pipeline multi-agente per la creazione di libri su Amazon Kindle Direct Publishing (KDP). Tre agenti Claude specializzati lavorano in sequenza per portare un'idea di libro dalla ricerca di mercato agli asset pronti per la pubblicazione, targetizzando simultaneamente **Amazon.com (US)** e **Amazon.it (IT)**.

### Funzionalita

- **Strategia Dual Market** - Ottimizzazione simultanea US e IT con copywriting italiano nativo
- **Agente Market Intelligence** - Analisi competitor, ranking BSR, Google Trends, decisione Go/No-Go
- **Agente Product Design** - Specifiche tecniche, prompt AI, brief copertine, workflow Canva
- **Agente Publishing** - Descrizioni HTML, keyword backend, brief A+ Content
- **Conformita KDP** - Calcolo dorso, specifiche abbondanza, requisiti PDF
- **Ottimizzazione SEO** - Validazione keyword con verifica byte-count

### Agenti

| Agente | Fase | Output |
|--------|------|--------|
| Market Intelligence Architect | 1 | `NICHE_REPORT_*.md` |
| Product Design Director | 2 | `CONTENT_BLUEPRINT_*.md` |
| Publishing Optimization Specialist | 3 | `PUBLISHING_PACKAGE_*.md` |

### Avvio Rapido

```bash
# Prerequisiti: Claude Code CLI installato

# Fase 1: Ricerca di Mercato
# Usa agente market-intelligence-architect

# Fase 2: Design Prodotto (dopo decisione GO)
# Usa agente product-design-director

# Fase 3: Pacchetto Publishing
# Usa agente publishing-optimization-specialist
```

---

## License

MIT

---

<p align="center">
  <a href="https://github.com/fracabu">
    <img src="https://img.shields.io/badge/Made_by-fracabu-8B5CF6?style=flat-square" alt="Made by fracabu" />
  </a>
</p>
