# SHACL validation report

Run `python scripts/run_lab08.py --shacl` after installing dependencies. The script validates the dataset in `tests/valid_data.ttl` and the intentionally defective dataset in `tests/invalid_data.ttl`, saves machine-readable Turtle reports in `reports/`, and writes this report's generated result summary.

The invalid fixture intentionally contains more than three defect types: malformed customer ID, missing required customer email/profile shape compliance, wrong profile class, missing product name, negative price, unsupported currency, negative stock, and recommendation score above 1. The exact number of SHACL validation results must be taken from the actual run output, not inferred from the number of planted defects.

SHACL vs OWL: OWL describes the meaning of classes and properties and supports logical inference under an open-world assumption. SHACL validates a data graph against explicit shapes and constraints, so it can report missing required values, datatype mismatches, patterns, and numeric bounds. A missing property is not automatically inconsistent in OWL, but it can violate a SHACL `sh:minCount` constraint.
