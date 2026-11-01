# UPM Manifest Model — Specification Draft

**Specification:** b3Ɛq Unified Platform Manifest  
**Draft version:** 0.1.0  
**Normative architecture:** b3Ɛq EBMA™

## 1. Design goals

A UPM manifest must be portable, machine-readable, deterministic to validate, traceable to a source revision, explicit about ownership and dependencies, safe to publish without exposing secrets, and suitable for downstream compilation by UAPC.

## 2. Top-level structure

- `apiVersion`: manifest schema family and version.
- `kind`: fixed discriminator `PlatformManifest`.
- `metadata`: platform identity, version, owner, lifecycle and source revision.
- `architecture`: EBMA profile, components, boundaries and deployment units.
- `capabilities`: named capabilities with ownership and maturity.
- `contracts`: APIs, events, schemas and compatibility declarations.
- `dependencies`: internal and external dependencies with version constraints.
- `deploymentProfiles`: environments, regions, topology and resource requirements.
- `configuration`: non-secret configuration and references to secret identifiers.
- `security`: identity, authorization, data classification, privacy and policy requirements.
- `conformance`: gates, test suites, requirement mappings and evidence references.
- `release`: build artefacts, provenance, digests and signature references.
- `operations`: health, scaling, backup, recovery, SLO and observability requirements.
- `extensions`: namespaced vendor or product extensions with explicit schemas.

## 3. Identity and versioning

A manifest is identified by platform slug, platform version, manifest schema version and source revision. These identifiers are distinct. Updating a manifest must not mutate an already published immutable version.

## 4. Ownership and boundaries

Each component and capability must declare an owner. Each contract must identify producer, consumers, version and compatibility policy. Each data entity should identify its authoritative source system where relevant. Circular dependencies should be rejected or explicitly reviewed.

## 5. Secrets

Manifests may declare secret references (for example, a provider-specific secret identifier or external secret URI) and required access policy. They must never contain secret values, credentials, private keys, tokens or unredacted connection strings.

## 6. Evidence and trust

Evidence entries reference immutable artefacts or reports and record subject, producer, timestamp, scope and digest where available. A reference to evidence is not proof that the evidence is valid; consumers must verify authenticity, integrity and applicability.

## 7. Compatibility

Schema compatibility and platform dependency compatibility are separate concerns. A schema-valid manifest can still be semantically incompatible with a target runtime. UAPC must check both structural validation and declared compatibility constraints.

## 8. Extension policy

Extensions use namespaced keys and must not redefine core fields. Unknown extensions may be rejected or ignored only according to the declared compatibility profile; silent semantic reinterpretation is prohibited.

## 9. Lifecycle

Draft → Review → Approved → Published → Deprecated → Withdrawn. Published versions are immutable. Withdrawal must preserve audit history and define downstream impact.
