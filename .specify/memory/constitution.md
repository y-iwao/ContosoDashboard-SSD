<!--
Sync Impact Report
Version change: none → 1.0.0
Modified principles: initial constitution created
Added sections: Scope and Constraints, Development Workflow
Removed sections: none
Templates requiring updates:
- `.specify/templates/plan-template.md` ✅ no change required
- `.specify/templates/spec-template.md` ✅ no change required
- `.specify/templates/tasks-template.md` ✅ no change required
Follow-up TODOs: none
-->

# ContosoDashboard Constitution

## Core Principles

### I. Training Safety and Transparency
All repository design and documentation MUST be explicit that ContosoDashboard is a training-only application. Training-specific implementations MUST not be treated as production-ready behavior, and any production migration path MUST be documented clearly.

### II. Spec-Driven Development
All feature work MUST begin with a specification and planning artifacts in `.specify`. Changes MUST be traceable to a spec, and every PR MUST reference the applicable spec or task set.

### III. Security Boundary Discipline
Authorization, access control, and IDOR protections MUST be enforced at page, service, and data-query boundaries. Mock authentication and training-only controls MUST remain isolated from any production-security claims.

### IV. Simplicity, Abstraction, and Separation
Code changes MUST preserve clear separation between UI, service, and data layers and avoid premature production complexity. Training implementations MUST favor readability and maintainability over optimization.

### V. Continuous Quality and Review
All feature or architecture changes MUST include documentation, rationale, and review. Tests and documentation updates MUST accompany changes that affect behavior, security, or user experience.

## Scope and Constraints
The repository MUST remain offline-friendly and self-contained. External service integration is prohibited unless a training stub, placeholder, or migration note is explicitly documented. This constitution applies to code, documentation, and architecture decisions.

## Development Workflow
Feature work MUST follow the Speckit workflow: specification first, plan second, task breakdown third, then implementation. Pull requests MUST verify constitution compliance, include design rationale, and update end-user or architecture documentation when scope changes.

## Governance
This constitution supersedes informal conventions and is the reference for repository governance.

- Amendments to this constitution MUST be documented in `.specify/memory/constitution.md` and reviewed by repository maintainers.
- All PRs MUST confirm whether proposed changes preserve training-only assumptions and security boundaries.
- Compliance checks for the constitution SHOULD be included in PR descriptions and review checklists.
- Any change that expands repository scope beyond training or adds external dependencies MUST include an explicit migration plan and approval note.

**Version**: 1.0.0 | **Ratified**: 2026-04-26 | **Last Amended**: 2026-04-26
