# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## What this is

Workshop materials for the **GDG x Bulacan State University (BulSU) AI Workshop**, "What Can Agentic CLI Do?", held 20 February 2026. Audience: university students new to agentic command-line coding tools. Presented by Real Minds AI. The repo is published as a static site to GitHub Pages at `realmindsai.github.io/bulsu_tutorial_2026/`; students browse the HTML pages and download exercise files during the session.

## Commands

There is no build step — this is a plain static site. Editing workflow:

```bash
# Slides/handouts are authored in Markdown (Marp) and rendered to HTML.
# The .md files (workshop_prompts.md, facilitator_briefing.md) carry `marp: true`
# frontmatter; render with Marp CLI, e.g.:
npx @marp-team/marp-cli workshop_prompts.md -o workshop_prompts.html

# Preview locally — just open the HTML, or serve the folder:
python3 -m http.server   # then visit http://localhost:8000

# Deploy: push to main. .github/workflows/pages.yml uploads the whole
# repo root as the Pages artifact (no Jekyll build).
```

## Contents

- `index.html` — landing page linking the other pages (entry point of the Pages site).
- `ai_toolkit.html` — "Your AI Coding Toolkit": what ~$20 of AI credits buys, the 10 models, and OpenCode + Aider setup. The recommended starting page.
- `student_handout.html` — combined setup guide + all exercises + hackathon prompts on one page.
- `setup_guide.html` — standalone tool-install guide (Gemini CLI, Claude Code, etc.).
- `workshop_prompts.{md,html}` — Marp presentation slides (concepts + the five exercises). `.md` is the source, `.html` is the rendered deck.
- `facilitator_briefing.{md,html}` — Marp deck for facilitators/mentors: schedule, per-exercise notes, troubleshooting. `.md` is the source.
- `ai-toolkit/` — config templates students copy: `opencode.json` and `aider.conf.yml`, both pointing at the RMAI LiteLLM proxy.

### Exercise files (students download these live)

- `broken_app.py` — Flask department dashboard with a closure bug; the debugging exercise (Ex. 3 in README, but slides group exercises 1–5).
- `sari_sari_sales.csv` / `bulacan_sari_sari_sales_6months.csv` — sari-sari store sales data for the data-to-dashboard exercise.
- `heartrate.zip` — dataset for the "read a real GitHub project" exercise.
- `qr_*.png` — QR codes pointing students to the handout / prompts pages.

The five exercises (per `facilitator_briefing.md`): App From a Sentence, Data to Dashboard, Read a Real GitHub Project, Build Your Own Specialist, Research and Report. Exercises 1, 3, 4 run offline once the CLI tool is installed; Ex. 2 needs the CSV (USB backup), Ex. 5 needs web access.

## Architecture notes

- **AI access is via the RMAI LiteLLM proxy**, not direct vendor keys. Both `ai-toolkit/opencode.json` and `ai-toolkit/aider.conf.yml` set `baseURL`/`openai-api-base` to `https://llm-proxy.realmindsai.com.au/v1` and read the key from `LITELLM_API_KEY` (placeholder `sk-YOUR-KEY-HERE` in the aider template). Models are namespaced `openrouter/<vendor>/<model>` (DeepSeek, Qwen3, GPT-4o, Gemini, Claude). Keep these endpoints/model names in sync with the toolkit HTML when editing either.
- **Branding/theme is consistent across pages:** dark background `#0F1229`, text `#E8E8EC`, orange accent `#E8873A`, Georgia headings. The Marp decks embed the same palette in their `style:` frontmatter. Preserve it when adding pages.
- **Do not edit the rendered `.html` for slide decks directly** — change the `.md` source and re-render, or the next render overwrites your edits.
