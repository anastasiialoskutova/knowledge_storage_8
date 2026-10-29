# Lab 8 report — RDF store and SPARQL

## 1. Objective
Prepare an RDF dataset from the Lab 7 ontology, query it with SPARQL, validate it with SHACL, evaluate natural-language-to-SPARQL mappings, and document external concept links.

## 2. Environment
- OS: macOS (record exact version)
- Python: record `python --version`
- rdflib: record `python -c "import rdflib; print(rdflib.__version__)"`
- pySHACL: record `python -c "import pyshacl; print(pyshacl.__version__)"`
- Triple store: GraphDB or Apache Jena Fuseki (record exact version and dataset name)

## 3. RDF dataset
Insert the actual output from `reports/data_check.md`. Record the triple-store COUNT result and load evidence.

## 4. SPARQL queries
Summarize at least eight CQ queries, paste actual outputs from `reports/sparql_results.md`, explain each result, and manually verify at least three answers against the dataset.

## 5. SHACL validation
Paste actual results from `reports/shacl_run.md`. Explain at least three detected defects and compare SHACL validation with OWL inference.

## 6. Text-to-SPARQL evaluation
Paste actual metrics from `reports/t2s_run.md`. Clearly distinguish deterministic harness results from actual LLM results. Include five error analyses and before/after evaluation if a live model is used.

## 7. External links
Document five or more verified links, confidence and sources, and explain why at least one candidate was rejected. Run the federated query in a connected endpoint if required.

## 8. Conclusions
State which criteria are verified by execution and which remain manual/external steps.

## 9. AI use declaration
Describe the assistance used and which outputs were independently checked.
