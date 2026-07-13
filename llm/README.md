# LLM Prompts and Inference Configuration

This directory documents the proprietary LLM setup used for zero-shot violence
classification experiments.

## Files

- `violencia_global.txt`: zero-shot prompt for document-level binary violence
  classification.
- `violencia_sentencas.txt`: zero-shot prompt for sentence-level severity
  extraction and global severity aggregation.
- `inference_config.yaml`: model identifiers, provider endpoints, temperature,
  timeout/retry settings, prompt-file mapping, and API-key environment variables.

## Inference Parameters

The reported setup uses zero-shot prompting and deterministic decoding
(`temperature: 0.0`). Other decoding parameters, such as `top_p`, `top_k`,
maximum output tokens, and penalties, were not overwritten in the client code
and therefore used provider defaults. The active provider in the released
configuration is Maritaca AI with model identifier `sabia-4`,
`max_retries: 3`, and `timeout_seconds: 45.0`.

The configuration file also records the alternative proprietary model endpoints
supported by the code: OpenRouter with `anthropic/claude-sonnet-4.5` and Google
GenAI with `gemini-3-flash-preview`. API keys are referenced only through environment
variables and are not included in this repository.
