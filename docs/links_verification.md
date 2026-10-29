# External graph links: verification register

The source ontology already has a limited conceptual mapping to Schema.org. This register avoids asserting unverified identity links. Links below are candidate mappings grounded in the source ontology's own class names and Schema.org vocabulary; they should be checked against the current external definitions before final submission.

| Local concept | Candidate external URI | Predicate | Confidence | Rationale / status |
|---|---|---|---|---|
| Product | `https://schema.org/Product` | `skos:exactMatch` | 0.98 | Same broad product concept; verify definition and scope. Candidate. |
| Brand | `https://schema.org/Brand` | `skos:exactMatch` | 0.98 | Same brand concept. Candidate. |
| Offer | `https://schema.org/Offer` | `skos:exactMatch` | 0.98 | Commercial offer concept. Candidate. |
| Order | `https://schema.org/Order` | `skos:exactMatch` | 0.95 | Order concept; check differences in transaction semantics. Candidate. |
| ProductReview | `https://schema.org/Review` | `skos:closeMatch` | 0.90 | Review concept; local name is product-specific. Candidate. |
| Recommendation | `https://schema.org/Recommendation` | none | 0.00 | Rejected: no verified matching standard concept established by this exercise; do not use `owl:sameAs` based on name similarity alone. |

Each accepted mapping needs a human verification date and source URL before it is considered final. The local ontology currently contains `skos:closeMatch schema:ViewAction` for ProductView; this is a pre-existing conceptual mapping, not proof that all candidate mappings have been externally verified.
