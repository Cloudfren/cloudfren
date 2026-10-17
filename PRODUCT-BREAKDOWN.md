# Cloudfren Product Breakdown — Scratch s

> Working planning note. This is not an implementation spec or a commitment that existing code is production-ready. Decisions below are based on the founder's agreement in the planning conversation; unresolved topics remain open.

## Destination

Produce a shared product vision and an actionable MVP specification for Cloudfren: an open-source, self-hostable Kubernetes PaaS for independent developers and small teams, with a credible business model and useful built-in observability.

## Decisions so far

- **Planning outcome:** both a product vision and an MVP specification.
- **Initial audience:** independent developers and small teams who want to deploy and operate applications without building a platform themselves.
- **Business direction:** open-source core that can be self-hosted, with a commercial offering such as managed hosting and/or clearly differentiated paid value. Exact licensing and feature boundaries are undecided.
- **Observability in MVP:** include basic application health/status, logs, and metrics; advanced capabilities can follow.
- **MVP platform:** Kubernetes only.
- **Cluster ownership:** users bring their own Kubernetes cluster for MVP; Cloudfren-managed infrastructure is a possible later offering.
- **MVP deployment sources:** GitHub and container image registries.

## Current repository context

The workspace contains separate `paas/cloudfren-core`, `paas/cloudfren-web`, `paas/cloudfren-cli`, and `paas/cloudfren-worker` directories. A preliminary source-structure review suggests a Kubernetes-oriented control plane, web console, CLI, and worker-based build flow. The core appears to have deployment lifecycle, projects/teams, GitHub integration, billing, marketplace, and metrics-related areas. These are clues, not verified product commitments: implementation completeness and end-to-end behavior still need validation.

## Open decisions — next discussion round

1. **MVP deployment workflow:** Which path is the required golden path: connect GitHub and build from source, deploy an existing image, or both? What build strategy should be supported first?
2. **Application/runtime scope:** What should count as an MVP workload (stateless web service, worker, scheduled job, database/add-on)? Which workload types are explicitly deferred?
3. **Cluster onboarding and support boundary:** Which Kubernetes distributions/versions are supported, and what permissions and installation experience are acceptable for a user-provided cluster?
4. **Open-source and commercial boundary:** Which capabilities must remain in the open-source self-hosted edition, and what is the first paid offer (managed Cloudfren, support, enterprise controls, or another option)?
5. **Observability ownership and retention:** Which metrics/logging components are included or integrated, where is telemetry stored, and what default retention/resource-cost limits apply?
6. **Initial product success:** What is the single user outcome that defines MVP success (for example, first successful deploy, reliable rollback, or operating multiple apps), and how will it be measured?

## Not yet specified

- Detailed user personas, onboarding journey, and differentiation from Coolify/Kubero.
- Build pipeline, deployment lifecycle, rollback semantics, and supported source/registry integrations beyond the agreed initial categories.
- Multi-tenancy, team roles, secrets, networking/ingress, domains/TLS, persistent storage, backups, and security boundaries.
- Observability architecture, dashboards, alerting scope, data retention, and cost controls.
- Licensing, contribution governance, trademark/branding, hosted-service packaging, pricing, and feature entitlements.
- Release/support policy, upgrade path, installation/backup/restore experience, and operational SLOs.
- Validation of current repository behavior against intended user journeys, including worker job execution and frontend-to-core integration.

## Out of scope for this planning pass

- Implementing features or refactoring the existing repositories.
- Committing to detailed architecture, vendors, pricing, or launch dates before the product decisions above are settled.
