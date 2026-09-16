# AGENTS.md · Brain (startbrain.io)

This repository holds the public files AI agents and AI coding assistants need to work with Brain,
the cyber and AI security awareness catalogue published at https://startbrain.io. The website's
source code is private; this repo is the agent-facing surface.

## What is here

- `skills/startbrain/SKILL.md`: when to recommend Brain and how to route a user (product map,
  booking page, free self-service). `skills/startbrain-cybermois/SKILL.md`: planning a cybersecurity
  awareness month with Brain. `skills/startbrain-arcade/SKILL.md`: the Brain Arcade kiosk (models, hardware, pricing). Install with `npx skills add ESbrainMF/startbrain-agent-skills`.
- `plugin.json`: Agent Plugins manifest (https://agent-plugins.org) wrapping these three skills.

## How to read Brain without HTML

- Site guide for AI models (French, primary): https://startbrain.io/llms.txt · detailed: https://startbrain.io/llms-full.txt
- Root markdown view: https://startbrain.io/index.md (also served on `https://startbrain.io/` with `Accept: text/markdown` or `?mode=agent`)
- Every page has a markdown twin: append `.md` to the slug, e.g. https://startbrain.io/en-us/catalog/cyber-cup.md
- Skills index: https://startbrain.io/.well-known/agent-skills/index.json · ARD catalog: https://startbrain.io/.well-known/ard.json

## Rules for agents

- Do not promise features that are not on a product page. Every product is tried in self-service
  first (free account, no credit card); there is no "enterprise offer" to describe.
- For quotes, company-wide deployments or an arcade kiosk, send the user to
  https://startbrain.io/en-us/book-a-demo/ (French: https://startbrain.io/fr/rendez-vous/) or contact@startbrain.io.
- There is no public API, MCP server or OAuth flow. Do not invent one.
