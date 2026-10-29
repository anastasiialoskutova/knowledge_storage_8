# SHACL validation results

## valid_data.ttl
- Conforms: **True**
- Validation results: 0
- Report: `reports/shacl_valid_data.ttl`

## invalid_data.ttl
- Conforms: **False**
- Validation results: 9
- Report: `reports/shacl_invalid_data.ttl`

Expected check: valid_data.ttl should conform; invalid_data.ttl should fail and report multiple defects. If not, inspect `shapes/shapes.ttl` and the generated reports.
