# UPM, EBMA™ and UAPC™ — Responsibility and Data Flow

## EBMA™ defines the standard

The b3Ɛq Enterprise Bio-Mimetic Architecture™ is the normative enterprise architecture. It defines what architectural principles, structures, systems and governance requirements apply.

## UPM describes a platform

The Unified Platform Manifest records how a particular platform declares its identity, capabilities, components, contracts, dependencies, deployment profiles, configuration, security controls, conformance gates and operational evidence against an EBMA profile.

UPM is descriptive and declarative. It cannot redefine the normative architecture or claim conformance without evidence.

## UAPC™ compiles a validated manifest

The Universal Application, Agent and Process Compiler consumes a structurally and semantically validated UPM manifest. It may compile:
- application and service scaffolds;
- integration and contract plans;
- environment and deployment artefacts;
- policy and conformance gates;
- test plans and evidence requirements.

UAPC must reject invalid or incompatible manifests and retain source, compiler, output and provenance references.

## Build Orchesty™ executes governed delivery

Build Orchesty coordinates the approved build, test, package and deployment pipeline. A manifest does not itself deploy software; compilation and execution remain separate, auditable stages.

## Conceptual flow

```text
EBMA™ normative requirements
              |
              v
UPM platform manifest
(identity • capabilities • components • contracts
 dependencies • deployment • security • evidence)
              |
       schema + semantic validation
              |
              v
UAPC™ compilation
(scaffolds • integration plans • deployment artefacts)
              |
              v
Build Orchesty™
(build • test • package • release • deploy)
              |
              v
Runtime systems + evidence + feedback
```

The diagram expresses intended architecture, not a claim that these integrations are implemented.
