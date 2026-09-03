# AI Property Inspection Pipeline

An end-to-end property inspection automation built with **n8n** and **Google Gemini**, designed to receive inspection videos, analyze property conditions with multimodal AI, generate structured inspection reports, and compare entry/exit inspections.

## Architecture

1. **Sequential video upload** — receives inspection videos and stores them by session.
2. **AI inspection processing** — uploads media to Gemini, analyzes each environment, refines the structured result, and generates HTML/PDF output.
3. **Entry/exit comparison** — compares two inspection reports with Gemini and produces a structured comparison report.

## Tech stack

- n8n
- Google Gemini Files API / Gemini multimodal models
- JavaScript Code nodes
- Gotenberg for HTML-to-PDF conversion
- Webhooks and binary file processing
- Optional Bitrix24 file delivery

## Repository structure

```text
workflows/
  01-video-upload.json
  02-ai-inspection-processing.json
  03-inspection-comparison.json
docs/
  architecture.md
  security.md
examples/
.env.example
.gitignore
```

## Security

The workflows in this repository are **sanitized portfolio versions**. Production API keys, credential IDs, webhook identifiers, infrastructure URLs, instance metadata, and company-specific internal values have been removed or replaced with placeholders.

Never commit your real `.env`, API keys, webhook tokens, or n8n credential exports.

## Importing into n8n

Import the JSON files from `workflows/` and configure your own credentials and deployment paths. Review the placeholders before activation. The public workflows are intentionally exported as inactive.

## Disclaimer

This repository demonstrates the technical architecture of an AI-assisted inspection pipeline. AI-generated inspection results should be reviewed by a qualified professional before being used for legal, contractual, or property-condition decisions.
