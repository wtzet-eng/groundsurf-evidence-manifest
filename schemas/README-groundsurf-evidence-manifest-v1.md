# GroundSurf Evidence Manifest v1

GroundSurf Evidence Manifest v1 is an optional, machine-readable snapshot of the evidence already presented in a GroundSurf detailed report. It preserves source attribution and context in a form that other tools can consume without extracting evidence from report prose.

## Files

- JSON Schema: [groundsurf-evidence-manifest-v1.schema.json](./groundsurf-evidence-manifest-v1.schema.json)
- Schema version: `1.0.0`

## Core fields

Each evidence item contains a stable GroundSurf evidence identifier, claim text and language, source attribution, dataset date where available, spatial relationship, calculation or ingestion method, GroundSurf's own assessment status, confidence and limitations. A source record reference is supplied only when the evidence record includes an explicit source-specific identifier.

The report-level metadata records the report generation timestamp and the location context. A source retrieval timestamp is exported only when it was explicitly captured on the evidence item. GroundSurf does not substitute the report generation timestamp for source retrieval time.

## Status semantics

- `VERIFIED`, `MODELLED` and `REQUIRES_VERIFICATION` are GroundSurf's internal assessment statuses.
- These labels are not a third-party attestation, a formal PDTF verification claim or a guarantee that a source statement is correct.
- A nearby source observation is not automatically a measurement from the selected plot. The spatial relationship and limitation fields must be retained when interpreting the finding.

## Data minimisation

The export keeps useful scalar values and bounded summaries of returned attributes. Large geometries, feature collections, raw response payloads and map-image URLs are omitted to keep the manifest portable. The regular detailed report and its linked original sources remain the place to inspect full source material.

## Compatibility approach

This is a GroundSurf format designed to be stable and country-neutral. It borrows common provenance concepts—claim, source, reference, method, time and limitations—without claiming conformance with PDTF. A future PDTF adapter should map fields only where the meaning is equivalent and preserve GroundSurf's status semantics separately.
