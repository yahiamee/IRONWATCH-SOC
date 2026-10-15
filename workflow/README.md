# Workflow

This folder contains the exported n8n workflow used by the IRONWATCH SOC.

## File

- **IRONWATCH-SOC.json** – Complete n8n workflow export.

## Workflow Overview

The workflow performs the following steps:

1. Receives a security alert.
2. Structures the alert using the Edit Fields node.
3. Sends the alert to a Large Language Model (Google Gemini).
4. Applies evidence-based prompt engineering.
5. Produces a structured SOC incident analysis report.

## Notes

The workflow was designed to demonstrate:

- AI-assisted cybersecurity analysis
- Workflow automation
- Prompt engineering
- Evidence-based incident reporting
- Dynamic data handling using n8n expressions

Import the JSON file into n8n to explore or extend the workflow.
