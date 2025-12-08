# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a **KDP Publishing Pipeline** for creating Amazon KDP (Kindle Direct Publishing) coloring books and activity books. The system uses a multi-agent workflow to take a niche idea from market research through production to ready-to-publish assets.

## Agent Pipeline Architecture

The pipeline consists of three specialized agents that run sequentially:

### 1. Market Intelligence Architect (Phase 1)
**Agent file:** `.claude/agents/market-intelligence-architect.md`
- Validates niches using BSR (Best Seller Rank) data on Amazon.com (US) and Amazon.it (IT)
- Performs competitor analysis with ASINs and pricing
- Calculates revenue projections and royalties
- Makes Go/No-Go decisions with strict criteria checklist
- Generates SEO keyword strategy for both markets
- **Output:** `NICHE_REPORT_[BookName].md`

### 2. Product Design Director (Phase 2)
**Agent file:** `.claude/agents/product-design-director.md`
- Creates technical specifications (trim size, page count, spine width)
- Generates AI image prompts (Midjourney/Leonardo) for interior pages
- Designs complexity distribution (30% Beginner, 50% Intermediate, 20% Advanced)
- Creates cover design briefs with color palettes and typography
- Maps Universal vs Localized content for dual-market publishing
- **Output:** `CONTENT_BLUEPRINT_[BookName].md`

### 3. Publishing Optimization Specialist (Phase 3)
**Agent file:** `.claude/agents/publishing-optimization-specialist.md`
- Writes HTML product descriptions (max 4000 chars) for US and IT
- Identifies Amazon Browse Node IDs for both markets
- Validates backend keywords (7 slots, <50 bytes each, no title word overlap)
- Performs bilingual pre-flight compliance check
- Creates A+ Content briefs
- **Output:** `PUBLISHING_PACKAGE_[BookName].md`

## Key Business Rules

### Dual Market Strategy
- All products target both Amazon.com (US) and Amazon.it (IT) simultaneously
- Italian text must be native quality, not Google Translate
- Price points: typically $9.99 USD / €9.99 EUR
- Metric conversions required for IT market (e.g., 8.5" x 8.5" → 21.6 x 21.6 cm)

### BSR Sweet Spots
- US Market: 20,000 - 80,000 BSR
- IT Market: 5,000 - 30,000 BSR

### KDP Technical Specs (Coloring Books)
- Standard trim: 8.5" x 8.5" (square format)
- Page count: 104 pages (52 designs, single-sided)
- Spine width formula: Pages × 0.002252" (white paper)
- Interior: Black & white, 300 DPI
- Cover: CMYK, full bleed (0.125" all sides)

### Backend Keywords Rules
- 7 keyword slots maximum
- Each slot: <50 bytes
- NO words already in title/subtitle
- Different keywords for US vs IT

## File Naming Conventions

- Phase 1: `NICHE_REPORT_[BookName].md` or `phase1_*.md`
- Phase 2: `CONTENT_BLUEPRINT_[BookName].md` or `phase2_*.md`
- Phase 3: `PUBLISHING_PACKAGE_[BookName].md` or `phase3_*.md`

## Invoking Agents

Use the Task tool with the appropriate `subagent_type`:
- `market-intelligence-architect` - For niche research and validation
- `product-design-director` - For production blueprints
- `publishing-optimization-specialist` - For final publishing assets

Each agent saves its complete output as a markdown file before handover to the next phase.
