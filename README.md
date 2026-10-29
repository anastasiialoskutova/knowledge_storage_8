# Lab 8 — RDF store and SPARQL queries

## About
This project reuses the Lab 7 e-commerce recommendation ontology and adds clearly synthetic example customers, products, offers, prices, inventory, and recommendations. No real customer data is included.

## Run on macOS

```bash
cd lab08_ecommerce
python3 -m venv .venv
source .venv/bin/activate
python -m pip install --upgrade pip
python -m pip install -r requirements.txt
python scripts/run_lab08.py --all
```

If the default Python is not Python 3, install Python 3.11+ first. Outputs are written to `reports/`.

## Artifacts
- `data/kb.ttl`: merged Turtle dataset (source ontology + synthetic demo records).
- `data/kb.jsonld`: JSON-LD export.
- `data/links.ttl`: candidate external concept links and a documented rejected link.
- `queries/`: SELECT, ASK, CONSTRUCT, aggregation, OPTIONAL, FILTER, property path, and federated query examples.
- `shapes/shapes.ttl`: five SHACL node shapes and varied constraints.
- `tests/valid_data.ttl`, `tests/invalid_data.ttl`: validation fixtures.
- `tests/t2s.jsonl`: 15 natural-language questions with reference SPARQL.
- `claims/claims.csv`, `llm_log/`: expert verification/audit artifacts.

## Triple-store import (manual required step)
The package includes Turtle for import into GraphDB or Apache Jena Fuseki. Create a repository/dataset in the selected store, import both `data/kb.ttl` and `data/links.ttl` into the same dataset/default graph, then run:

```sparql
SELECT (COUNT(*) AS ?count) WHERE { ?s ?p ?o }
```

Record the actual endpoint, date, version and returned count in `docs/load_log.md`. The package does not falsely claim that an external store was already loaded.

## Important limits to disclose
- The federated Wikidata query needs network access and endpoint support; local execution skips it.
- The Text-to-SPARQL harness is deterministic and does not call a live LLM. If the instructor requires actual LLM generation, connect an approved model and archive the real raw prompts/outputs and parameters.
- Check all candidate Schema.org mappings in `docs/links_verification.md` against current definitions and record verification URLs/dates before final submission.
- The supplied `claims.csv` is a starter audit register; the student must review claims and fill any required evidence from actual execution.

## AI assistance declaration
AI assistance was used to draft and structure code, query examples, test data, and documentation. Dataset checks, validation results, external mappings, and all claims should be verified by the student and reported truthfully.
# knowledge_storage_8
