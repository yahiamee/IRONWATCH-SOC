# Troubleshooting

## Google Gemini Quota Error (429)

### Problem

The workflow returns:

```
429 Too Many Requests
Quota exceeded
```

### Cause

The selected Gemini model may not have available quota.

### Solution

Check the selected model and account quota in your provider console. Select an available model or retry after the applicable quota window. Automated retries are not implemented.

---

## Missing Output

Check that:

- All required fields are populated.
- The Basic LLM Chain is correctly configured.
- The Google Gemini credential is valid.

---

## Incorrect Analysis

Review the prompt in:

```
prompts/soc-analyst-prompt.md
```

Prompt quality directly affects AI output quality.
