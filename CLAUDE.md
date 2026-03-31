# Research Agent — Project CLAUDE.md

## Overview

Sales prospecting research agent built as a Claude Code slash command (`/research-agent`). No code — pure agentic orchestration using Exa MCP and Claude Code's agent capabilities.

## How It Works

When invoked as `/research-agent <company name>`, it:
1. Searches for company intel and recent signals (funding, launches, hires, partnerships)
2. Identifies VP Sales / CRO / Head of Revenue
3. Finds public quotes, LinkedIn posts, or podcast appearances from that person
4. Generates a structured research brief with a suggested outreach angle

## Key Files

| File | Purpose |
|------|---------|
| `.claude/commands/research-agent.md` | The slash command prompt |
| `research-agents/` | Output folder for generated briefs |
| `README.md` | Public repo description |

## Tech Stack

- **Search:** Exa MCP (`web_search_exa`, `crawling_exa`, `web_search_advanced_exa`)
- **Orchestration:** Claude Code agents (parallel + sequential)
- **Output:** Markdown briefs

## Output Format

Each brief saved to `research-agents/{company-name}.md` contains:
- Company overview (2-3 sentences)
- Recent signals (with dates)
- Target contact name + title
- Key quote or insight from that person
- Suggested outreach angle

## Deployment

- **Repo:** https://github.com/QuanNguyen-Alex/research-agent
- **GitHub Account:** QuanNguyen-Alex
