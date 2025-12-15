# Claude KDP Agents

**Multi-agent pipeline for Amazon KDP book creation powered by Claude Code**

[English](#english) | [Italiano](#italiano)

---

## English

### Overview

A multi-agent pipeline for Amazon Kindle Direct Publishing (KDP) book creation, powered by Claude Code. This system automates the process of validating niches, designing products, and preparing publishing assets for coloring books and activity books, targeting both **Amazon.com (US)** and **Amazon.it (IT)** markets simultaneously.

```
┌─────────────────────────┐     ┌─────────────────────────┐     ┌─────────────────────────┐
│   Market Intelligence   │     │    Product Design       │     │     Publishing          │
│      Architect          │────▶│       Director          │────▶│   Optimization          │
│      (Phase 1)          │     │      (Phase 2)          │     │    Specialist           │
│                         │     │                         │     │      (Phase 3)          │
└─────────────────────────┘     └─────────────────────────┘     └─────────────────────────┘
         │                               │                               │
         ▼                               ▼                               ▼
   NICHE_REPORT_*.md            CONTENT_BLUEPRINT_*.md         PUBLISHING_PACKAGE_*.md
```

### Key Features

- **Dual Market Strategy** - Simultaneous optimization for Amazon.com and Amazon.it with native Italian copywriting
- **Market Intelligence Agent** - Competitor analysis with ASINs, BSR rankings, reviews, and pricing
- **Product Design Agent** - Technical specs, AI image generation prompts, cover design briefs
- **Publishing Agent** - HTML descriptions, backend keywords, A+ Content briefs
- **KDP Technical Compliance** - Accurate spine width calculations, bleed specs, PDF requirements
- **SEO Optimization** - Backend keyword validation with byte-count verification

### Agents

| Agent | Phase | Output | Responsibilities |
|-------|-------|--------|------------------|
| Market Intelligence Architect | 1 | `NICHE_REPORT_*.md` | Competitor analysis, Google Trends, Go/No-Go decision |
| Product Design Director | 2 | `CONTENT_BLUEPRINT_*.md` | Tech specs, AI prompts, Canva workflow |
| Publishing Optimization Specialist | 3 | `PUBLISHING_PACKAGE_*.md` | HTML descriptions, Browse Nodes, keywords |

### Tech Stack

- **Claude Code** - AI agent orchestration
- **Web Search** - Market research capabilities
- **Midjourney/Leonardo** - AI image generation (prompts provided)
- **Canva** - Cover and interior assembly

### Quick Start

```bash
# Prerequisites: Claude Code CLI installed

# Phase 1: Market Research
# Ask Claude to analyze a niche using the market-intelligence-architect agent

# Phase 2: Product Design (after GO decision)
# Proceed with product-design-director agent

# Phase 3: Publishing Package
# Complete with publishing-optimization-specialist agent
```

**Example Prompt:**
```
Analyze the "Mandala Flowers" niche for an adult coloring book,
8.5x8.5 inches, 104 pages, targeting US and IT markets at $9.99/€9.99
```

### Business Rules

| Specification | Value |
|---------------|-------|
| Trim Size | 8.5" x 8.5" |
| Page Count | 104 pages |
| Interior | Black & White |
| Bleed | 0.125" all sides |
| Resolution | 300 DPI |
| US Price | $9.99 (60% royalty) |
| IT Price | €9.99 (60% royalty) |
| US BSR Target | 20,000 - 80,000 |
| IT BSR Target | 5,000 - 30,000 |

### Project Structure

```
claude-kdp-agents/
├── .claude/agents/
│   ├── market-intelligence-architect.md
│   ├── product-design-director.md
│   └── publishing-optimization-specialist.md
├── CLAUDE.md
├── NICHE_REPORT_*.md
├── CONTENT_BLUEPRINT_*.md
└── PUBLISHING_PACKAGE_*.md
```

### License

MIT License

---

## Italiano

### Panoramica

Una pipeline multi-agente per la creazione di libri su Amazon Kindle Direct Publishing (KDP), alimentata da Claude Code. Il sistema automatizza la validazione delle nicchie, la progettazione dei prodotti e la preparazione degli asset per libri da colorare e activity book, targetizzando simultaneamente i mercati **Amazon.com (US)** e **Amazon.it (IT)**.

```
┌─────────────────────────┐     ┌─────────────────────────┐     ┌─────────────────────────┐
│   Market Intelligence   │     │    Product Design       │     │     Publishing          │
│      Architect          │────▶│       Director          │────▶│   Optimization          │
│      (Fase 1)           │     │      (Fase 2)           │     │    Specialist           │
│                         │     │                         │     │      (Fase 3)           │
└─────────────────────────┘     └─────────────────────────┘     └─────────────────────────┘
         │                               │                               │
         ▼                               ▼                               ▼
   NICHE_REPORT_*.md            CONTENT_BLUEPRINT_*.md         PUBLISHING_PACKAGE_*.md
```

### Funzionalita Principali

- **Strategia Dual Market** - Ottimizzazione simultanea per Amazon.com e Amazon.it con copywriting italiano nativo
- **Agente Market Intelligence** - Analisi competitor con ASIN, ranking BSR, recensioni e prezzi
- **Agente Product Design** - Specifiche tecniche, prompt per generazione immagini AI, brief per copertine
- **Agente Publishing** - Descrizioni HTML, keyword backend, brief A+ Content
- **Conformita Tecnica KDP** - Calcolo preciso dorso, specifiche abbondanza, requisiti PDF
- **Ottimizzazione SEO** - Validazione keyword backend con verifica byte-count

### Agenti

| Agente | Fase | Output | Responsabilita |
|--------|------|--------|----------------|
| Market Intelligence Architect | 1 | `NICHE_REPORT_*.md` | Analisi competitor, Google Trends, decisione Go/No-Go |
| Product Design Director | 2 | `CONTENT_BLUEPRINT_*.md` | Specifiche tecniche, prompt AI, workflow Canva |
| Publishing Optimization Specialist | 3 | `PUBLISHING_PACKAGE_*.md` | Descrizioni HTML, Browse Node, keyword |

### Stack Tecnologico

- **Claude Code** - Orchestrazione agenti AI
- **Web Search** - Capacita di ricerca di mercato
- **Midjourney/Leonardo** - Generazione immagini AI (prompt forniti)
- **Canva** - Assemblaggio copertine e interni

### Avvio Rapido

```bash
# Prerequisiti: Claude Code CLI installato

# Fase 1: Ricerca di Mercato
# Chiedi a Claude di analizzare una nicchia usando l'agente market-intelligence-architect

# Fase 2: Design Prodotto (dopo decisione GO)
# Procedi con l'agente product-design-director

# Fase 3: Pacchetto Publishing
# Completa con l'agente publishing-optimization-specialist
```

**Esempio di Prompt:**
```
Analizza la nicchia "Mandala Fiori" per un libro da colorare per adulti,
8.5x8.5 pollici, 104 pagine, targeting mercati US e IT a $9.99/€9.99
```

### Regole di Business

| Specifica | Valore |
|-----------|--------|
| Formato | 8.5" x 8.5" |
| Pagine | 104 pagine |
| Interno | Bianco e Nero |
| Abbondanza | 0.125" tutti i lati |
| Risoluzione | 300 DPI |
| Prezzo US | $9.99 (60% royalty) |
| Prezzo IT | €9.99 (60% royalty) |
| BSR Target US | 20,000 - 80,000 |
| BSR Target IT | 5,000 - 30,000 |

### Struttura Progetto

```
claude-kdp-agents/
├── .claude/agents/
│   ├── market-intelligence-architect.md
│   ├── product-design-director.md
│   └── publishing-optimization-specialist.md
├── CLAUDE.md
├── NICHE_REPORT_*.md
├── CONTENT_BLUEPRINT_*.md
└── PUBLISHING_PACKAGE_*.md
```

### Licenza

MIT License
