# GroundSurf Evidence Manifest

**A public, country-neutral specification for portable evidence provenance in land-site reports.**

GroundSurf Evidence Manifest defines a machine-readable JSON snapshot of the evidence presented in a GroundSurf detailed report. It is intended to make source attribution and evidence context easier for other tools to preserve and consume, without requiring them to extract claims from report prose.

- **Current version:** 1.0.0
- **JSON Schema:** [schemas/groundsurf-evidence-manifest-v1.schema.json](schemas/groundsurf-evidence-manifest-v1.schema.json)
- **Specification notes:** [schemas/README-groundsurf-evidence-manifest-v1.md](schemas/README-groundsurf-evidence-manifest-v1.md)
- **GroundSurf:** https://groundsurf.net

## What the manifest preserves

Each evidence record can carry a stable identifier, claim text and language, source attribution, dataset date where available, spatial relationship, method, assessment status, confidence, limitations, and retrieval time when explicitly recorded. It also includes report-level location context and a source list.

## Important interpretation notes

- VERIFIED, MODELLED, and REQUIRES_VERIFICATION are GroundSurf's internal assessment labels. They are not third-party attestations or a guarantee that a source statement is correct.
- A nearby observation is not automatically a measurement from the selected plot. Spatial context and limitations must be retained.
- Missing values are not positive or negative findings.
- GroundSurf Evidence Manifest does not claim conformance with PDTF. Similar provenance concepts are used only where useful; a future adapter must preserve the separate meaning of GroundSurf statuses.

## Scope

This repository publishes the format specification and documentation only. It does not contain GroundSurf's application source code, report-generation logic, data integrations, or manifest-export implementation.

## License

The schema and documentation in this repository are available under the MIT License. See [LICENSE](LICENSE).
