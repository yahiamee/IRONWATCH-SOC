# Prompt Engineering

This folder contains the prompt used by the IRONWATCH SOC.

Rather than simply asking an AI model to summarize a security alert, the prompt was carefully engineered to produce structured, evidence-based incident reports suitable for a Security Operations Center (SOC) environment.

## Design Objectives

The prompt was designed to:

- Encourage evidence-based reasoning.
- Reduce AI hallucinations.
- Clearly distinguish confirmed facts from assumptions.
- Generate consistent and structured incident reports.
- Use professional cybersecurity terminology.
- Map observations to the MITRE ATT&CK framework where appropriate.
- Provide actionable containment and investigation recommendations.

## Prompt Engineering Techniques

The workflow demonstrates several prompt engineering best practices:

- Role-based prompting
- Structured output formatting
- Dynamic variable injection using n8n expressions
- Explicit reasoning constraints
- Confidence level reporting
- Hallucination mitigation
- Professional report generation

## Dynamic Expressions

The prompt dynamically inserts data from previous workflow nodes using n8n expressions such as:

```text
{{ $json.alertName }}
{{ $json.sourceIP }}
{{ $json.destinationHost }}
{{ $json.username }}
{{ $json.severity }}
{{ $json.description }}
```

This allows the same prompt to analyze different security alerts without modification.

## Prompt File

The complete prompt is available in:

- **soc-analyst-prompt.md**
