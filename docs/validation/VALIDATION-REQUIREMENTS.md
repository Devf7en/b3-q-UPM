# UPM Validation Requirements

## Validation layers

1. **Parsing:** input is valid JSON (and later any explicitly supported authoring format).
2. **Schema validation:** structure conforms to the selected JSON Schema version.
3. **Semantic validation:** identifiers resolve; owners exist; component references are valid; dependencies are satisfiable; contracts have compatible versions; no forbidden cycles exist.
4. **Policy validation:** security, privacy, secrets, data classification, allowed deployment targets and governance policies are satisfied.
5. **EBMA mapping review:** applicable requirements are mapped and evidence is inspectable; a declaration alone is not verification.
6. **Provenance validation:** source revision, artefact digests, attestations and signatures are verifiable where required.
7. **Compiler readiness:** all UAPC-required fields and constraints are satisfied for the requested compilation target.

## Required negative fixtures

- Missing required top-level field.
- Invalid platform slug or semantic version.
- Duplicate component/capability identifiers.
- Dangling component or contract reference.
- Circular dependency where prohibited.
- Secret literal or credential embedded in a manifest.
- Unsupported schema version.
- Incompatible deployment profile.
- Invalid or untrusted evidence reference.
- Manifest claims verified conformance without required evidence.

## Result model

A validator should return machine-readable findings with rule identifier, severity, JSON Pointer, message, remediation hint and validator version. Distinguish errors, warnings and informational findings. Validation must be deterministic for the same input, schema, policy and validator version.
