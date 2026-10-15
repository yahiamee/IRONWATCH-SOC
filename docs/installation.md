# IRONWATCH SOC Installation

Maintainer: **yahia hayder**.

1. Use n8n with the Manual Trigger, Edit Fields, Basic LLM Chain, and Google Gemini Chat Model nodes available. A tested n8n release has not yet been recorded.
2. Import `workflow/IRONWATCH-SOC.json` from the repository root.
3. In Google Gemini Chat Model, create/select your own Gemini credential and select an available model. No credentials or model selection are bundled.
4. Confirm Manual Trigger → Edit Fields → Basic LLM Chain, with Gemini connected to the chain's language-model input.
5. Edit the six sample fields in Edit Fields; `examples/sample-alert.json` contains the same synthetic data.
6. Execute manually and inspect the chain output for the ten requested report sections. The output is text and is not schema validated.

Alert data is transmitted to the configured provider. Use approved sanitized data. Review the output before taking any response action.

A successful live run and exact n8n/model versions still need to be recorded. See `docs/project-review.md`.
