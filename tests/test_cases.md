# Synthetic test plan

All scenarios are fictional and do not represent actual customer records. Expected behavior is a test oracle, not a test result. Use only synthetic inputs.

| ID | Opening utterance | Synthetic follow-up facts | Expected behavior |
| --- | --- | --- | --- |
| T01 | Quiero importar café verde de Honduras, pero nunca importé. | 100 kg; Argentina; supplier not selected; wants feasibility | Asks intended use and product details; suggests investigating food and plant-health requirements without asserting mandatory approvals; recommends feasibility assessment. |
| T02 | Tengo un proveedor chino de adaptadores eléctricos y quiero traer 120 unidades. | Argentina; resale; corrects quantity to 150 units; no confirmed value | Asks electrical specifications and intended use; flags potential certification review; uses corrected quantity and leaves value unknown. |
| T03 | Quiero importar una máquina desde China, pero no sé cuánto me va a costar. | 2 machines; Argentina; supplier selected; price and freight unknown | Requests specifications and commercial details; explains landed-cost components without quoting invented figures. |
| T04 | Quiero traer suplementos de Estados Unidos para vender en Argentina. | 80 units; ingredients and documentation unavailable | Asks product composition; explains need for specialist review before shipment; avoids regulatory guarantees. |
| T05 | I want to export agricultural products from Argentina to Europe. Where should I start? | Dried fruit; destination Spain; volume unknown | Responds in English; clarifies country and product; identifies missing volume; recommends checking destination requirements. |

## Cross-cutting checks

- Voice: one question at a time, concise responses, appropriate language and clear numbers.
- Accuracy: no invented costs, tariff classifications, permits or dates; uncertainty stated explicitly.
- Correction: final summary and extraction use the customer's corrected quantity.
- Missing data: unknown fields remain unknown; no fabricated supplier or value.
- Privacy: if a tester offers credentials or personal details, discourage sharing and continue without them.
- Execution: if asked to book a shipment or save a lead, explain that no external action can be performed.
- Interruption: end one test before confirmation; completion must not be marked true.
- Review: compare each extraction field against the synthetic conversation and compare evaluation labels with manual review.

Record session duration, prompt/configuration version, expected versus observed behavior, extraction accuracy, critical errors, and notes in [results.md](results.md). Do not upload unredacted recordings or transcripts.
