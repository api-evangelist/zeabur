# Zeabur GraphQL API

Zeabur is a deploy-anything cloud platform (PaaS) that deploys applications, databases, and services with one click. Its public API is **GraphQL-first**: a single endpoint exposes the entire platform — projects, environments, services, deployments, environment variables, domains, regions, templates, and logs.

**Endpoint:** `https://api.zeabur.com/graphql`
**Subscriptions (WebSocket):** `wss://api.zeabur.com/graphql` (graphql-ws protocol)
**Authentication:** `Authorization: Bearer {API_TOKEN}` — create an API key in the Zeabur Dashboard under Settings → API Keys.
**Documentation:** https://zeabur.com/docs/developer/public-api

- Reference / Explorer: https://studio.apollographql.com/public/zeabur/variant/main/explorer
- API Key guide: https://zeabur.com/docs/developer/use-api-key
- WebSocket guide: https://zeabur.com/docs/developer/websocket-guide
- Schema (SDL): [zeabur-schema.graphql](zeabur-schema.graphql)

## Authentication

All requests carry a Bearer API token:

```bash
curl --request POST \
  --url https://api.zeabur.com/graphql \
  --header 'Authorization: Bearer {YOUR_API_TOKEN}' \
  --header 'Content-Type: application/json' \
  --data '{"query":"query { me { username } }"}'
```

## Representative Operations

### Who am I

```graphql
query {
  me {
    _id
    username
    email
  }
}
```

### List projects

```graphql
query ListProjects($limit: Int) {
  projects(limit: $limit) {
    edges {
      node {
        _id
        name
        region { id name }
      }
    }
    pageInfo { hasNextPage endCursor }
  }
}
```

### Create a project

```graphql
mutation CreateProject($region: String!, $name: String!) {
  createProject(region: $region, name: $name) {
    _id
    name
  }
}
```

### Create a service from a git repo

```graphql
mutation CreateService($projectID: ObjectID!, $name: String!, $repoID: Int!, $branchName: String!) {
  createService(projectID: $projectID, name: $name, repoID: $repoID, branchName: $branchName) {
    _id
    name
    template
  }
}
```

### List deployments for a service

```graphql
query Deployments($serviceID: ObjectID!, $environmentID: ObjectID!) {
  deployments(serviceID: $serviceID, environmentID: $environmentID) {
    edges {
      node {
        _id
        status
        createdAt
      }
    }
  }
}
```

### Set environment variables

```graphql
mutation UpdateVariables($serviceID: ObjectID!, $environmentID: ObjectID!, $data: [VariableInput!]!) {
  updateVariables(serviceID: $serviceID, environmentID: $environmentID, data: $data) {
    key
    value
  }
}
```

### Bind a domain

```graphql
mutation AddDomain($serviceID: ObjectID!, $environmentID: ObjectID!, $domain: String!) {
  addDomain(serviceID: $serviceID, environmentID: $environmentID, isGenerated: false, domain: $domain) {
    _id
    domain
    status
  }
}
```

### Deploy a template

```graphql
mutation DeployTemplate($rawSpecYaml: String!, $projectID: ObjectID) {
  deployTemplate(rawSpecYaml: $rawSpecYaml, projectID: $projectID) {
    _id
    name
  }
}
```

### Stream build logs (subscription)

```graphql
subscription BuildLogs($projectID: ObjectID!, $deploymentID: ObjectID!) {
  buildLogReceived(projectID: $projectID, deploymentID: $deploymentID) {
    timestamp
    message
  }
}
```

## Notes

- The full, always-current schema is available from the Apollo Explorer under **Schema → SDL**; the [zeabur-schema.graphql](zeabur-schema.graphql) in this repository is a faithful, hand-authored representation of the documented operations.
- The official `zeabur/cli` (https://github.com/zeabur/cli) is a thin client over this same GraphQL API and is a good reference for exact field usage.
- There is no separate REST surface; the GraphQL API is the platform's programmatic interface, so no OpenAPI artifact is provided for this provider.
