# Zeabur (zeabur)

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

Zeabur is a deploy-anything cloud platform (PaaS) that ships applications, databases, and services with one click. Its public API is GraphQL-first, exposing projects, environments, services, deployments, environment variables, domains, regions, and templates through a single endpoint at `https://api.zeabur.com/graphql`.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/zeabur/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/zeabur/refs/heads/main/apis.yml)

## Tags

- PaaS
- Deployment
- Cloud
- DevOps
- GraphQL

## Timestamps

- **Created:** 2026-07-01
- **Modified:** 2026-07-01

## APIs

### Zeabur Projects API

Create, list, clone, export, and delete projects, and manage the environments (production, staging, etc.) within each project, via GraphQL queries and mutations.

- **Human URL:** [https://zeabur.com/docs/developer/public-api](https://zeabur.com/docs/developer/public-api)
- **Base URL:** `https://api.zeabur.com/graphql`

#### Tags

- Projects
- Environments
- GraphQL

#### Properties

- [Documentation](https://zeabur.com/docs/developer/public-api)
- [GraphQL](graphql/zeabur-graphql.md)
- [GraphQL Schema](graphql/zeabur-schema.graphql)
- [Postman Collection](collections/zeabur.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/zeabur.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Zeabur Services API

Create services from git repositories, uploaded zips, Dockerfiles, or prebuilt marketplace codes; restart, suspend, redeploy, update image tags, read metrics/ports, and run commands inside running services.

- **Human URL:** [https://zeabur.com/docs/developer/public-api](https://zeabur.com/docs/developer/public-api)
- **Base URL:** `https://api.zeabur.com/graphql`

#### Tags

- Services
- Git
- Docker
- Marketplace

#### Properties

- [Documentation](https://zeabur.com/docs/developer/public-api)
- [GraphQL](graphql/zeabur-graphql.md)
- [GraphQL Schema](graphql/zeabur-schema.graphql)
- [Postman Collection](collections/zeabur.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/zeabur.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Zeabur Deployments API

List and inspect deployments for a service and environment, fetch the latest deployment, read build and runtime logs, and stream logs in real time via graphql-ws subscriptions.

- **Human URL:** [https://zeabur.com/docs/developer/public-api](https://zeabur.com/docs/developer/public-api)
- **Base URL:** `https://api.zeabur.com/graphql`

#### Tags

- Deployments
- Builds
- Logs

#### Properties

- [Documentation](https://zeabur.com/docs/developer/public-api)
- [Documentation](https://zeabur.com/docs/developer/websocket-guide)
- [GraphQL](graphql/zeabur-graphql.md)
- [GraphQL Schema](graphql/zeabur-schema.graphql)
- [Postman Collection](collections/zeabur.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/zeabur.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Zeabur Environment Variables API

List and update environment variables scoped to a service within an environment, for injecting configuration and secrets into deployed workloads.

- **Human URL:** [https://zeabur.com/docs/developer/public-api](https://zeabur.com/docs/developer/public-api)
- **Base URL:** `https://api.zeabur.com/graphql`

#### Tags

- Environment Variables
- Configuration
- Secrets

#### Properties

- [Documentation](https://zeabur.com/docs/developer/public-api)
- [GraphQL](graphql/zeabur-graphql.md)
- [GraphQL Schema](graphql/zeabur-schema.graphql)
- [Postman Collection](collections/zeabur.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/zeabur.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Zeabur Domains API

Bind generated (*.zeabur.app) or custom domains to a service, list bound domains, check domain availability, and remove domain bindings.

- **Human URL:** [https://zeabur.com/docs/developer/public-api](https://zeabur.com/docs/developer/public-api)
- **Base URL:** `https://api.zeabur.com/graphql`

#### Tags

- Domains
- DNS
- Networking

#### Properties

- [Documentation](https://zeabur.com/docs/developer/public-api)
- [GraphQL](graphql/zeabur-graphql.md)
- [GraphQL Schema](graphql/zeabur-schema.graphql)
- [Postman Collection](collections/zeabur.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/zeabur.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Zeabur Templates & Regions API

List and retrieve deploy templates, deploy a template spec into a project, create and update custom templates from spec YAML, and enumerate available deploy regions (including generic bring-your-own-server regions).

- **Human URL:** [https://zeabur.com/docs/developer/public-api](https://zeabur.com/docs/developer/public-api)
- **Base URL:** `https://api.zeabur.com/graphql`

#### Tags

- Templates
- Marketplace
- Regions

#### Properties

- [Documentation](https://zeabur.com/docs/developer/public-api)
- [GraphQL](graphql/zeabur-graphql.md)
- [GraphQL Schema](graphql/zeabur-schema.graphql)
- [Postman Collection](collections/zeabur.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/zeabur.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [GitHub Organization](https://github.com/zeabur)
- [LinkedIn](https://www.linkedin.com/company/zeabur)
- [Website](https://zeabur.com/)
- [Documentation](https://zeabur.com/docs)
- [Plans](plans/zeabur-plans-pricing.yml)
- [Rate Limits](rate-limits/zeabur-rate-limits.yml)
- [Fin Ops](finops/zeabur-finops.yml)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
