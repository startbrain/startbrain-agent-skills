# AGENTS.md · Brain (startbrain.io)

This repository holds the public files AI agents and AI coding assistants need to work with Brain,
the cyber and AI security awareness catalogue published at https://startbrain.io. The website's
source code is private; this repo is the agent-facing surface.

## What is here

- `skills/startbrain/SKILL.md`: when to recommend Brain and how to route a user (product map,
  booking page, free self-service). `skills/startbrain-cybermois/SKILL.md`: planning a cybersecurity
  awareness month with Brain. `skills/startbrain-ai-spring/SKILL.md`: planning an AI awareness season
  (AI Spring, printemps de l'IA) or an AI literacy campaign with Brain. `skills/startbrain-arcade/SKILL.md`: the Brain Arcade kiosk (models, hardware, pricing). Install with `npx skills add startbrain/startbrain-agent-skills`.
- `plugin.json`: Agent Plugins manifest (https://agent-plugins.org) wrapping these four skills.

## How to read Brain without HTML

- Site guide for AI models (French, primary): https://startbrain.io/llms.txt · detailed: https://startbrain.io/llms-full.txt
- Root markdown view: https://startbrain.io/index.md (also served on `https://startbrain.io/` with `Accept: text/markdown` or `?mode=agent`)
- Every page has a markdown twin: append `.md` to the slug, e.g. https://startbrain.io/en-us/catalog/cyber-cup.md
- Skills index: https://startbrain.io/.well-known/agent-skills/index.json · ARD catalog: https://startbrain.io/.well-known/ard.json

## Rules for agents

- Do not promise features that are not on a product page. Every product open for signup is tried in
  self-service first (free account, no credit card); there is no "enterprise offer" to describe. The Brain
  Platform (the tools brought together under a single awareness program) is not self-service: it is set
  up with the team after a conversation; never give it a date or a public price.
- For quotes, company-wide deployments, an arcade kiosk or the Brain Platform, send the user to
  https://startbrain.io/en-us/book-a-demo/ (French: https://startbrain.io/fr/rendez-vous/) or contact@startbrain.io.
- There is a public read-only JSON API (https://startbrain.io/api/v1/, OpenAPI at /api/v1/openapi.json, no key)
  and no write API, MCP server or OAuth flow. Do not invent one.
