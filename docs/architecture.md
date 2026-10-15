# System Architecture

## Overview

The IRONWATCH SOC is built using n8n as the workflow orchestration platform and Google Gemini as the Large Language Model (LLM).

The workflow accepts a structured security alert, enriches it through prompt engineering, and produces a professional SOC incident analysis report.

---

## Architecture Diagram

```text
Manual Trigger -> Edit Fields -> Basic LLM Chain -> Text report
                                      ^
                                      | language-model connection
                             Google Gemini Chat Model
```

---

## Workflow Components

### 1. Manual Trigger

Starts the workflow during testing and development.

---

### 2. Edit Fields

Creates a structured JSON object containing the security alert information, including:

- Alert Name
- Source IP
- Destination Host
- Username
- Severity
- Description

---

### 3. Basic LLM Chain

Constructs a structured prompt using dynamic n8n expressions.

The prompt instructs the AI to:

- Analyse the alert
- Assess risk
- Map to MITRE ATT&CK
- Recommend containment actions
- Recommend investigation steps
- Separate facts from assumptions

---

### 4. Google Gemini

Processes the prompt using Google's Gemini model and returns a text incident analysis; no output schema is enforced.

---

## Data Flow

Input Alert

â†“

Structured JSON

â†“

Prompt Engineering

â†“

AI Analysis

â†“

SOC Incident Report

---

## Design Principles

The workflow was designed around the following principles:

- Simplicity
- Readability
- Modularity
- Reusability
- Evidence-based AI analysis
- Hallucination reduction
- Professional cybersecurity reporting
