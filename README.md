# Claude KDP Agents

A multi-agent pipeline for Amazon KDP (Kindle Direct Publishing) book creation, powered by Claude Code. This system automates the process of validating niches, designing products, and preparing publishing assets for coloring books and activity books.

## Overview

This pipeline uses three specialized Claude agents that work sequentially to take a book idea from market research to ready-to-publish assets, targeting both **Amazon.com (US)** and **Amazon.it (IT)** markets simultaneously.

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

## Agents

### 1. Market Intelligence Architect

The strategic lead that validates niches using real market data.

**Responsibilities:**
- Competitor analysis with ASINs, BSR rankings, reviews, and pricing
- Google Trends analysis for seasonality and growth
- Revenue projections and royalty calculations
- Go/No-Go decision with strict criteria checklist
- SEO keyword strategy for US and IT markets

**Output:** `NICHE_REPORT_[BookName].md`

### 2. Product Design Director

The creative and technical architect that creates production blueprints.

**Responsibilities:**
- Technical specifications (trim size, page count, spine width)
- AI image generation prompts (Midjourney/Leonardo)
- Complexity distribution for designs
- Cover design briefs with color palettes
- Universal vs Localized content mapping
- Canva assembly workflow

**Output:** `CONTENT_BLUEPRINT_[BookName].md`

### 3. Publishing Optimization Specialist

The final quality gatekeeper that prepares ready-to-upload assets.

**Responsibilities:**
- HTML product descriptions (max 4000 chars)
- Amazon Browse Node ID identification
- Backend keyword optimization (7 slots, <50 bytes each)
- Bilingual pre-flight compliance check
- A+ Content briefs

**Output:** `PUBLISHING_PACKAGE_[BookName].md`

## Usage

### Prerequisites

- [Claude Code](https://claude.ai/code) CLI installed
- Access to web search for market research

### Running the Pipeline

1. **Start with Phase 1 - Market Research:**
   ```
   Ask Claude to analyze a niche using the market-intelligence-architect agent
   ```

2. **Continue to Phase 2 - Production Blueprint:**
   ```
   After GO decision, proceed with product-design-director agent
   ```

3. **Finish with Phase 3 - Publishing Package:**
   ```
   Complete with publishing-optimization-specialist agent
   ```

### Example Prompt

```
Analyze the "Mandala Flowers" niche for an adult coloring book,
8.5x8.5 inches, 104 pages, targeting US and IT markets at $9.99/€9.99
```

## Key Features

### Dual Market Strategy
- Simultaneous optimization for Amazon.com and Amazon.it
- Native Italian copywriting (not machine translated)
- Market-specific Browse Node recommendations
- Currency and metric conversions

### KDP Technical Compliance
- Accurate spine width calculations
- Bleed and margin specifications
- PDF export requirements
- Cover dimension formulas

### SEO Optimization
- Backend keyword validation
- Title/subtitle character limits (200 chars)
- No keyword overlap with title
- Byte-count verification (<50 bytes per slot)

## Project Structure

```
claude-kdp-agents/
├── .claude/
│   └── agents/
│       ├── market-intelligence-architect.md
│       ├── product-design-director.md
│       └── publishing-optimization-specialist.md
├── CLAUDE.md                    # Claude Code guidance
├── README.md                    # This file
├── NICHE_REPORT_*.md           # Phase 1 outputs
├── CONTENT_BLUEPRINT_*.md      # Phase 2 outputs (or phase2_*.md)
└── PUBLISHING_PACKAGE_*.md     # Phase 3 outputs (or phase3_*.md)
```

## Business Rules

### BSR Sweet Spots
| Market | Target BSR Range |
|--------|------------------|
| US     | 20,000 - 80,000  |
| IT     | 5,000 - 30,000   |

### Standard Coloring Book Specs
| Specification | Value |
|---------------|-------|
| Trim Size     | 8.5" x 8.5" |
| Page Count    | 104 pages |
| Interior      | Black & White |
| Paper         | White |
| Bleed         | 0.125" all sides |
| Resolution    | 300 DPI |

### Pricing Strategy
- US: $9.99 (60% royalty)
- IT: €9.99 (60% royalty)

## License

MIT License

## Author

Created with Claude Code by Anthropic
