# Text-to-SPARQL prompt versions

## v1 — baseline
"Translate the question to SPARQL. Return only the query."

This intentionally underspecified baseline is represented in the local test harness by supporting only the four simplest intents. It is a deterministic proxy, not a raw LLM generation.

## v2 — schema-constrained improvement
"You are generating SPARQL for the e-commerce recommendation RDF graph. Use only the declared classes and properties in `data/kb.ttl`. Prefix: `PREFIX : <http://example.org/ecommerce-recommendations#>`. Return exactly one SELECT, ASK, or CONSTRUCT query. Use OPTIONAL only when a value may be absent. Use FILTER for numeric conditions. Do not invent predicates or classes. Add LIMIT 100 to row-returning queries. If the question cannot be represented with the supplied schema, return `UNSUPPORTED` and explain the missing schema term. Before execution, parse the query, check class/property names against the schema, and execute with the row limit. Preserve the raw prompt and raw model output for each test."

## Evaluation note
The included evaluation measures a deterministic baseline and improved intent mapper so it runs without an API key. It does not substitute for a real LLM call if the instructor explicitly requires one. When connected to a real model, replace the proxy candidates with archived raw model outputs and rerun the same validation/evaluation.
