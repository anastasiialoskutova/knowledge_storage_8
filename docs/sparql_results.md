# SPARQL query results

Run `python scripts/run_lab08.py --queries` to execute the local-compatible queries against `data/kb.ttl`; results and interpretation notes are written to `reports/sparql_results.md`. The federated query is retained as a separate query file but requires an endpoint that supports `SERVICE` and a network connection. The `cq09_federated_wikidata.rq` is a template: local demo products are not asserted to have Wikidata identities, so zero results is an acceptable result rather than a fabricated match.

The script measures execution time for two equivalent local queries and records timings from the current run. Timing depends on hardware and environment. At least three result samples should be manually checked against the triples in `data/kb.ttl` before submission.
