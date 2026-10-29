# Text-to-SPARQL evaluation

- Test questions: 15

| Metric | Baseline | Improved |
|---|---:|---:|
| Syntax-valid fraction | 26.7% | 100.0% |
| Schema-valid fraction | 26.7% | 100.0% |
| Correct supported intent/result fraction | 26.7% | 100.0% |

## Failure review (based on actual harness output)

- **T2S-04 / high_stock**: intent not mapped by baseline. Category: unsupported intent / coverage gap. Improvement: extend schema-grounded intent mapping and add a regression test.
- **T2S-05 / recommendations**: intent not mapped by baseline. Category: unsupported intent / coverage gap. Improvement: extend schema-grounded intent mapping and add a regression test.
- **T2S-06 / average_price**: intent not mapped by baseline. Category: unsupported intent / coverage gap. Improvement: extend schema-grounded intent mapping and add a regression test.
- **T2S-07 / high_score_exists**: intent not mapped by baseline. Category: unsupported intent / coverage gap. Improvement: extend schema-grounded intent mapping and add a regression test.
- **T2S-08 / customer_emails_optional**: intent not mapped by baseline. Category: unsupported intent / coverage gap. Improvement: extend schema-grounded intent mapping and add a regression test.

## Limitation

This is a deterministic intent-mapping evaluation harness, not a live LLM call. `correct` measures mapped intent coverage plus successful execution, not semantic equivalence against all gold result bindings. To satisfy a requirement for real LLM evaluation, integrate the course-approved model, preserve raw output, and compare result sets with the reference queries.
