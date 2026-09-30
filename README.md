> **Live Actor:** [Run XRechnung to JSON Parser on Apify](https://apify.com/kamerozkan/xrechnung-to-json-parser).

# XRechnung to JSON Parser: Samples

Parse XRechnung UBL or CII XML into a stable EN 16931-oriented JSON contract with pinned technical conformance findings.

[Run XRechnung to JSON Parser on Apify](https://apify.com/kamerozkan/xrechnung-to-json-parser)

[![Apify Actor](https://img.shields.io/badge/Apify-Run%20Actor-00c7b7?logo=apify)](https://apify.com/kamerozkan/xrechnung-to-json-parser)
![Build](https://img.shields.io/badge/build-0.0.3%20SUCCEEDED-2f855a)
![PPE](https://img.shields.io/badge/document--processed-%240.005-4c1)
![Samples](https://img.shields.io/badge/examples-3%20paired%20JSON-2f855a)
![License](https://img.shields.io/badge/license-MIT-blue)

Parse XRechnung UBL or CII XML into a shared EN 16931-oriented JSON model with pinned KoSIT technical validation evidence.

This repository is a flat, GitHub-friendly sample pack with three paired Actor
inputs, three Dataset result rows, and a standalone JSON Schema. It is useful
for ERP integration design, AP automation, e-invoice testing, and search-driven
technical discovery.

## Verified snapshot

| Field | Value |
|---|---|
| Actor | `xrechnung-to-json-parser` |
| Actor ID | `QR4q0jicBJaU7yhI1` |
| Status | `PUBLIC STORE LISTING` |
| Successful build | `0.0.3` |
| Custom event | `document-processed` |
| Exact event price | `$0.005` |

The live pay-per-event price is $0.005 per evaluated document. An Actor-start charge can also apply; check the Store page for the current maximum charge before a production run.

Hosted build 0.0.3: accepted run vDoLHAXakiHa2XevL, source failure run iVTmKY39aMbv6zsKk, and budget run W1EFkJfrdcmgZugxr.

## What the Actor does

- UBL Invoice, UBL CreditNote, and CII syntax detection
- XRechnung 3.0.2 technical validation and structured findings
- optional XML and XHTML report artifacts stored outside Dataset rows

## Example matrix

| # | Scenario and input | Output | Result |
|---:|---|---|---|
| 01 | [Accepted official XRechnung UBL](01_accepted_ubl_input.json) | [Dataset row](01_accepted_ubl_output.json) | `SUCCEEDED` / `ACCEPTED` |
| 02 | [Blocked loopback source](02_source_failure_input.json) | [Dataset row](02_source_failure_output.json) | `FAILED` / `NOT_EVALUATED` |
| 03 | [Pre-engine charge budget stop](03_budget_guard_input.json) | [Dataset row](03_budget_guard_output.json) | `FAILED` / `NOT_EVALUATED` |

Example outputs are exact hosted field subsets or projections from real local
engine results. No omitted value was reconstructed. See
[`DATA_NOTICE.md`](DATA_NOTICE.md) for run IDs, fixture hashes, status, and the
hosted-versus-local evidence boundary.


The third XRechnung budget example is a request recipe: `actorInput` is the
Actor input and `runOptions.maxTotalChargeUsd` is a run API option. It must not
be inserted into the Actor input itself.


## Dataset contract

[`dataset_record.schema.json`](dataset_record.schema.json) is adapted directly
from the production Dataset contract and narrowed to this Actor name. Money and
quantity values remain decimal strings. Raw XML, PDFs, and generated artifacts
belong in the run key-value store, not in Dataset rows.

Validate an output with any JSON Schema Draft 7 implementation:

```bash
python -m jsonschema -i 01_accepted_ubl_output.json dataset_record.schema.json
```

## Interpretation boundary

ACCEPTED means the pinned technical checks accepted the bytes. It is not legal validity, tax recognition, authenticity, transmission, or recipient acceptance.

`ACCEPTED`, `CONFORMANT`, or `CONVERTED` describes only the evidence explicitly
recorded by the pinned processing pipeline. It does not prove legal validity,
tax treatment, authenticity, signature validity, transmission, payment,
archival compliance, or recipient or network acceptance.

## Privacy

Do not publish customer invoices, raw reports, extracted XML, bank details,
tax identifiers, personal data, access tokens, cookies, or private KVS links.
The examples reference public upstream fixtures. You remain responsible for
lawful processing, access control, retention, and deletion.

## Related e-invoice Actor samples

- [ZUGFeRD and Factur-X PDF to JSON](https://github.com/kamerozkan/zugferd-facturx-pdf-to-json-sample)
- [XRechnung XML to JSON](https://github.com/kamerozkan/xrechnung-to-json-parser-sample) (this repository)
- [Peppol BIS UBL to JSON](https://github.com/kamerozkan/peppol-ubl-to-json-parser-sample)
- [ZUGFeRD to XRechnung](https://github.com/kamerozkan/zugferd-to-xrechnung-converter-sample)
- [UBL and CII conversion](https://github.com/kamerozkan/ubl-cii-format-converter-sample)

## License

MIT applies to this repository's original documentation, JSON projections, and
schema adaptation. It does not relicense standards, validator engines, public
fixtures, upstream repositories, third-party marks, or source documents.
