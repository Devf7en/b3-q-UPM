# ADR-0001: Confirm UPM as Unified Platform Manifest

- **Status:** Accepted
- **Date:** 2026-11-01
- **Portfolio ID:** B3EQ-PORT-0014

## Context

The initial repository presentation incorrectly expanded UPM as Universal Project Manager. The authoritative pre-existing project charter in b3Ɛq Core at `docs/portfolio/initiatives/upm.md` defines UPM as **Unified Platform Manifest**, a portable machine-readable description of a platform and its architecture, contracts, dependencies, deployment, security and evidence.

## Decision

This repository implements **b3Ɛq UPM™ — Unified Platform Manifest**. It is the declarative platform-description input to UAPC. It is not a project/task management system.

If a Universal Project Manager product is still desired, it must be treated as a separate initiative with its own confirmed name, portfolio ID, charter and repository decision. It must not be conflated with this UPM.

## Relationship

EBMA defines normative architecture; UPM declares a platform against EBMA; UAPC consumes validated UPM manifests to compile scaffolds and plans; Build Orchesty executes governed delivery pipelines.

## Consequences

Documentation, repository metadata, portfolio registry and future integrations must use this expansion. Correct the earlier presentation in the governance conversation record. The schema is a draft and requires validation fixtures and review before stabilization.
