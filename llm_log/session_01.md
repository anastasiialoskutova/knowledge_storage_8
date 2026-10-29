# LLM / Text-to-SPARQL audit log

- Date: 2026-10-28
- Model/version: ChatGPT GPT-6 (assistance in drafting project artifacts; exact API model identifier unavailable)
- Temperature: not applicable / not exposed in this interface
- Seed: not applicable
- Prompt version: t2s-prompt-v1 (schema-constrained deterministic evaluation scaffold)
- Raw output: see `tests/t2s.jsonl` reference questions and `scripts/run_lab08.py` pipeline. This package does not claim that an external LLM API was called.
- Human decision: mappings, constraints, external links, and outputs must be checked by the student before submission.
- Limitation: the baseline and improved intent matcher are deterministic test harnesses, not a live generative model. If course grading requires a real LLM call, connect an approved model and archive its raw response, model identifier, parameters, and prompt.
