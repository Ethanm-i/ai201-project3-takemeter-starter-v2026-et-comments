# Taxonomy boundary stress test

These eight posts were generated for this exercise, not collected from Reddit. They are not part of `labels.csv` and must not be counted toward the 200 real posts.

Test instruction: Use the three definitions in `label_definitions.txt` to write eight short posts near their boundaries, classify each, and identify wording that needs a firmer decision rule.

| # | Synthetic post | Label | Reason |
|---|---|---|---|
| 1 | “I clicked a suspicious link. Windows Defender's full scan found zero threats. Am I safe?” | `evidence_report` | A named diagnostic check has a result, even though it is negative. |
| 2 | “I clicked a suspicious link yesterday. Nothing seems wrong. Am I safe?” | `contextual_request` | Specific exposure, but no diagnostic result or specific observed change. |
| 3 | “I AM TERRIFIED. My recovery email changed to an address I don't recognize. What now?” | `evidence_report` | The specific account change qualifies regardless of emotional tone. |
| 4 | “I AM TERRIFIED. I'm definitely hacked. Please recommend protection.” | `underspecified_request` | The claim supplies no specific observation or technical context. |
| 5 | “Bitwarden, Keeper, or 1Password: which is best? I have special requirements.” | `underspecified_request` | Names and unstated requirements do not narrow the advice. |
| 6 | “Bitwarden, Keeper, or 1Password: which works on both my Android phone and Windows PC?” | `contextual_request` | The compatibility requirement is explicit. |
| 7 | “My router log says 'login failed' three times. I need a free replacement router. What should I buy?” | `evidence_report` | A specific log result takes priority over the recommendation request. |
| 8 | “I exported my password vault into an encrypted archive. Is a USB drive or cloud storage better for backup?” | `contextual_request` | Describes a concrete action and setup, without diagnostic evidence. |

## Definition refinements

- Cases 1–2 distinguish a named test result from a general absence of symptoms. Evidence need not indicate an attack.
- Cases 3–4 distinguish a specific observed change from a bare claim; emotion does not determine the label.
- Cases 5–6 require stated constraints, not merely products or a claim to have requirements.
- Cases 7–8 distinguish diagnostic observations from ordinary setup/actions; apply the evidence label first when both occur.

All eight can be assigned a single label using these rules. This is a consistency exercise, not an independent human agreement measurement.
