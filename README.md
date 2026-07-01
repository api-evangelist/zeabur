# Zeabur (zeabur)

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
