# Data Notice

## Purpose

This repository documents `xrechnung-to-json-parser` with three paired input and
output examples plus a standalone Dataset JSON Schema. It is an independent,
unofficial technical sample and is not endorsed by a standards body, tax
authority, validator vendor, Peppol authority, Access Point, or invoice
recipient.

## Snapshot and evidence class

| Field | Verified value |
|---|---|
| Snapshot date | `2026-07-30` |
| Actor ID | `QR4q0jicBJaU7yhI1` |
| Actor status | `PUBLIC STORE LISTING` |
| Successful build | `0.0.3` |
| Event contract | `document-processed` at `$0.005` |
| Evidence class | hosted Apify run evidence |

Hosted build 0.0.3: accepted run vDoLHAXakiHa2XevL, source failure run iVTmKY39aMbv6zsKk, and budget run W1EFkJfrdcmgZugxr.

The Actor is now available through its [public Store listing](https://apify.com/kamerozkan/xrechnung-to-json-parser). Local contract results with `billable: false` were produced outside an Apify PPE run. They prove the pinned processing contract exercised locally, not a hosted charge or public lifecycle.

## Input provenance

| # | Stem | Fixture | SHA-256 observed in result |
|---:|---|---|---|
| 01 | `01_accepted_ubl` | Accepted official XRechnung UBL | `3558d8eee6499350f69c150b54b4019556458667cfc972beaa9bb7bf1e11303f` |
| 02 | `02_source_failure` | Blocked loopback source | `not available before evaluation` |
| 03 | `03_budget_guard` | Pre-engine charge budget stop | `not available before evaluation` |

The input JSON files link to public fixtures at immutable commits or version
tags where available. The fixture bytes are not copied into this repository.
Each linked document remains governed by its upstream license and terms.

## Output provenance

Each output is an exact field subset from a hosted Dataset row or an exact
projection from a real local engine result. Projection removes bulky trace,
finding, and raw-report material; it does not invent replacement values.
`producedAt`, source digests, engine digests, target digests, status values,
and error codes are retained when present.

Hosted owner-side provenance:

- ZUGFeRD PDF parser build `0.0.6`: runs `eH5xbA5flKNgEoO0q`,
  `q2vDgyT5AM9mGXGoe`, and `GqxUtLATVjLlKuiaI`.
- XRechnung parser build `0.0.3`: runs `vDoLHAXakiHa2XevL`,
  `iVTmKY39aMbv6zsKk`, and `W1EFkJfrdcmgZugxr`.

The run and Dataset records are not made public by this repository. IDs are
included for owner-side audit provenance only.

## Privacy and security

No access token, cookie, signed URL, webhook secret, customer account ID, or
private KVS URL belongs in this repository. Public fixtures may contain
synthetic invoice parties, addresses, tax identifiers, bank data, amounts, and
line items under upstream terms.

Customer runs can contain personal data and confidential accounting data.
Validation reports, generated XML, extracted XML, and source PDFs can reproduce
the full invoice. Users are responsible for lawful processing, authorization,
access control, retention, deletion, and contractual obligations.

## Interpretation limits

- Technical conformance is not legal or tax validity.
- A parser does not prove authenticity, delivery, payment, or recipient acceptance.
- Peppol document validation is not AS4 transport or network delivery.
- A ZUGFeRD 1.0 upgrade does not prove legacy source-to-upgrade semantic identity.
- `CONVERTED` does not mean `LOSSLESS`.
- `LOSSLESS` is used only when the recorded canonical comparisons are complete and equivalent.
- Local evidence is not a hosted availability or billing claim.

## License boundary

MIT covers this repository's original text, result projections, and schema
adaptation. It does not relicense EN 16931, XRechnung, ZUGFeRD, Factur-X,
Peppol BIS, UBL, CII, KoSIT, Mustangproject, phax, public fixtures, third-party
software, specifications, trademarks, or report formats.
