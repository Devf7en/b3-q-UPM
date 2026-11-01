# b3Ɛq UPM™ Roadmap

## P0 — Schema and terminology
- [x] Recover the original UPM charter and confirm expansion: Unified Platform Manifest.
- [x] Define scope and clarify it is not Universal Project Manager.
- [x] Create initial manifest vocabulary and schema draft.
- [ ] Review schema against JSON Schema 2020-12 and establish schema linting.
- [ ] Define required/optional fields, extension policy and canonical identifiers.
- [ ] Create positive and negative validation fixtures.

## P1 — Validation and compatibility
- [ ] Implement reference validator.
- [ ] Define semantic validation beyond JSON Schema.
- [ ] Define schema compatibility and migration rules.
- [ ] Define dependency constraint and conflict resolution rules.
- [ ] Define environment profile inheritance and override precedence.
- [ ] Validate signatures, provenance references and artefact digests.

## P2 — Reference manifests
- [ ] Create reviewed manifests for b3Ɛq Core, ComOS, Finverse and Nigeria DataOS.
- [ ] Add manifests for EBMA profiles and shared infrastructure where appropriate.
- [ ] Validate manifests against actual repository content and contracts.
- [ ] Record ownership, update cadence and source revision for each manifest.

## P3 — Signed manifest registry
- [ ] Define registry API and lifecycle.
- [ ] Define publication, review, deprecation and revocation.
- [ ] Implement artifact storage and immutable version references.
- [ ] Add cryptographic signing and verification.
- [ ] Integrate provenance and software supply-chain attestations.

## P4 — UAPC compiler integration
- [ ] Define UPM-to-UAPC input contract.
- [ ] Compile scaffolds, integration plans and deployment artefacts from validated manifests.
- [ ] Add deterministic compilation and reproducibility tests.
- [ ] Record compiler version, inputs, outputs and provenance.

## P5 — Conformance and supply-chain security
- [ ] Define EBMA requirement-to-manifest mappings.
- [ ] Add conformance gate references and evidence collection.
- [ ] Add policy checks, dependency risk and SBOM references.
- [ ] Establish release signing, verification and revocation workflow.
- [ ] Review governance, threat model and production readiness.

A roadmap item is complete only when the artefact and verification evidence exist.
