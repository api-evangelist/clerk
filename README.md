# Clerk (clerk)

Clerk is a drop-in authentication and user management platform for web and mobile applications. The product spans sign-up / sign-in flows, user profiles, multi-factor authentication, passkeys, social sign-on, magic links, bot and fraud detection, organizations (B2B / multi-tenant) with custom roles and invitations, and a Billing product for subscriptions. The Backend API at api.clerk.com is authenticated with a Bearer secret key and has an OpenAPI specification. Frontend SDKs cover Next.js, React, React Router, Expo, Astro, TanStack React Start, Chrome Extension, and vanilla JavaScript. Backend SDKs cover Node, Go, Python, Ruby, Java, PHP, and C#. Webhooks are delivered via Svix.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/clerk/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/clerk/refs/heads/main/apis.yml)

## Tags

- Authentication
- User Management
- Identity
- Passkeys
- MFA
- B2B
- Organizations
- Billing

## Timestamps

- **Created:** 2026-05-23
- **Modified:** 2026-05-30

## APIs

### Clerk Backend API

Server-to-server REST API for managing users, sessions, organizations, organization memberships, organization invitations, JWT templates, sign-in tokens, OAuth applications, SAML connections, allowlist / blocklist identifiers, actor tokens, webhooks, and instance settings. Authenticated with a Bearer secret key (sk_test_... or sk_live_...). Versioned under /v1.

- **Human URL:** [https://clerk.com/docs/reference/backend-api](https://clerk.com/docs/reference/backend-api)
- **Base URL:** `https://api.clerk.com`

#### Tags

- Backend
- REST
- Users
- Sessions
- Organizations

#### Properties

- [Documentation](https://clerk.com/docs/reference/backend-api)
- [OpenAPI](https://github.com/clerk/openapi-specs) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/clerk.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/clerk.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Clerk Frontend API

Browser-facing API consumed by Clerk's frontend SDKs and ClerkJS for sign-up, sign-in, session refresh, and user profile mutations. Endpoint is instance-specific (subdomain on clerk.accounts.dev or a customer vanity domain). Authenticated with the publishable key and short-lived client tokens.

- **Human URL:** [https://clerk.com/docs/reference/frontend-api](https://clerk.com/docs/reference/frontend-api)
- **Base URL:** `https://clerk.accounts.dev`

#### Tags

- Frontend
- REST
- Sessions

#### Properties

- [Documentation](https://clerk.com/docs/reference/frontend-api)
- [Postman Collection](collections/clerk.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/clerk.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Clerk Webhooks (Svix)

Webhook events delivered via Svix for user, session, organization, email, SMS, and role lifecycle changes. Customers configure endpoints in the dashboard and verify signatures with the Svix libraries.

- **Human URL:** [https://clerk.com/docs/integrations/webhooks/overview](https://clerk.com/docs/integrations/webhooks/overview)
- **Base URL:** `customer-configured`

#### Tags

- Webhooks
- Events
- Svix

#### Properties

- [Documentation](https://clerk.com/docs/integrations/webhooks/overview)
- [AsyncAPI](https://raw.githubusercontent.com/api-evangelist/clerk/refs/heads/main/asyncapi/clerk-webhooks-asyncapi.yml) — [AsyncAPI Specification](https://www.asyncapi.com/docs/reference/specification/latest)
- [Postman Collection](collections/clerk.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/clerk.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Clerk JavaScript SDK

Official ClerkJS browser library and monorepo of framework adapters (Next.js, React, Expo, React Router, Astro, Chrome Extension, TanStack). Powers Clerk's prebuilt UI components and headless hooks.

- **Human URL:** [https://github.com/clerk/javascript](https://github.com/clerk/javascript)
- **Base URL:** `https://github.com/clerk/javascript`

#### Tags

- SDK
- JavaScript
- Frontend

#### Properties

- [Repository](https://github.com/clerk/javascript)
- [Postman Collection](collections/clerk.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/clerk.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Clerk Next.js SDK

Next.js integration covering App Router and Pages Router, middleware, route handlers, server components, and server actions. Distributed from the @clerk/nextjs package inside the JavaScript monorepo.

- **Human URL:** [https://clerk.com/docs/quickstarts/nextjs](https://clerk.com/docs/quickstarts/nextjs)
- **Base URL:** `https://github.com/clerk/javascript`

#### Tags

- SDK
- Next.js
- Frontend

#### Properties

- [Documentation](https://clerk.com/docs/quickstarts/nextjs)
- [Postman Collection](collections/clerk.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/clerk.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Clerk React SDK

React components, hooks, and providers from the @clerk/clerk-react package for plain React SPAs.

- **Human URL:** [https://clerk.com/docs/quickstarts/react](https://clerk.com/docs/quickstarts/react)
- **Base URL:** `https://github.com/clerk/javascript`

#### Tags

- SDK
- React
- Frontend

#### Properties

- [Documentation](https://clerk.com/docs/quickstarts/react)
- [Postman Collection](collections/clerk.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/clerk.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Clerk Expo SDK

Expo / React Native bindings for Clerk supporting OAuth via deep links, secure session storage, and biometrics.

- **Human URL:** [https://clerk.com/docs/quickstarts/expo](https://clerk.com/docs/quickstarts/expo)
- **Base URL:** `https://github.com/clerk/javascript`

#### Tags

- SDK
- Expo
- React Native
- Mobile

#### Properties

- [Documentation](https://clerk.com/docs/quickstarts/expo)
- [Postman Collection](collections/clerk.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/clerk.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Clerk React Router SDK

Adapter for React Router v7 (Remix successor) covering loaders, actions, and server-rendered authentication.

- **Human URL:** [https://clerk.com/docs/quickstarts/react-router](https://clerk.com/docs/quickstarts/react-router)
- **Base URL:** `https://github.com/clerk/javascript`

#### Tags

- SDK
- React Router
- Frontend

#### Properties

- [Documentation](https://clerk.com/docs/quickstarts/react-router)
- [Postman Collection](collections/clerk.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/clerk.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Clerk Astro SDK

Adapter for the Astro framework with components and middleware.

- **Human URL:** [https://clerk.com/docs/quickstarts/astro](https://clerk.com/docs/quickstarts/astro)
- **Base URL:** `https://github.com/clerk/javascript`

#### Tags

- SDK
- Astro
- Frontend

#### Properties

- [Documentation](https://clerk.com/docs/quickstarts/astro)
- [Postman Collection](collections/clerk.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/clerk.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Clerk TanStack Start SDK

Adapter for TanStack Start (React full-stack framework) with route-level authentication helpers.

- **Human URL:** [https://clerk.com/docs/quickstarts/tanstack-start](https://clerk.com/docs/quickstarts/tanstack-start)
- **Base URL:** `https://github.com/clerk/javascript`

#### Tags

- SDK
- TanStack
- Frontend

#### Properties

- [Documentation](https://clerk.com/docs/quickstarts/tanstack-start)
- [Postman Collection](collections/clerk.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/clerk.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Clerk Node.js SDK

Backend SDK for Node.js (@clerk/backend / @clerk/express / @clerk/fastify) that wraps the Backend API and verifies session JWTs.

- **Human URL:** [https://clerk.com/docs/references/backend/overview](https://clerk.com/docs/references/backend/overview)
- **Base URL:** `https://github.com/clerk/javascript`

#### Tags

- SDK
- Node.js
- Backend

#### Properties

- [Documentation](https://clerk.com/docs/references/backend/overview)
- [Postman Collection](collections/clerk.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/clerk.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Clerk Go SDK

Official Go SDK for the Clerk Backend API.

- **Human URL:** [https://github.com/clerk/clerk-sdk-go](https://github.com/clerk/clerk-sdk-go)
- **Base URL:** `https://github.com/clerk/clerk-sdk-go`

#### Tags

- SDK
- Go
- Backend

#### Properties

- [Repository](https://github.com/clerk/clerk-sdk-go)
- [Postman Collection](collections/clerk.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/clerk.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Clerk Python SDK

Official Python SDK for the Clerk Backend API.

- **Human URL:** [https://github.com/clerk/clerk-sdk-python](https://github.com/clerk/clerk-sdk-python)
- **Base URL:** `https://github.com/clerk/clerk-sdk-python`

#### Tags

- SDK
- Python
- Backend

#### Properties

- [Repository](https://github.com/clerk/clerk-sdk-python)
- [Postman Collection](collections/clerk.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/clerk.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Clerk Ruby SDK

Official Ruby SDK for the Clerk Backend API, with a Rails integration.

- **Human URL:** [https://github.com/clerk/clerk-sdk-ruby](https://github.com/clerk/clerk-sdk-ruby)
- **Base URL:** `https://github.com/clerk/clerk-sdk-ruby`

#### Tags

- SDK
- Ruby
- Rails
- Backend

#### Properties

- [Repository](https://github.com/clerk/clerk-sdk-ruby)
- [Postman Collection](collections/clerk.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/clerk.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Clerk Java SDK

Official Java SDK for the Clerk Backend API.

- **Human URL:** [https://github.com/clerk/clerk-sdk-java](https://github.com/clerk/clerk-sdk-java)
- **Base URL:** `https://github.com/clerk/clerk-sdk-java`

#### Tags

- SDK
- Java
- Backend

#### Properties

- [Repository](https://github.com/clerk/clerk-sdk-java)
- [Postman Collection](collections/clerk.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/clerk.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Clerk PHP SDK

Official PHP SDK for the Clerk Backend API.

- **Human URL:** [https://github.com/clerk/clerk-sdk-php](https://github.com/clerk/clerk-sdk-php)
- **Base URL:** `https://github.com/clerk/clerk-sdk-php`

#### Tags

- SDK
- PHP
- Backend

#### Properties

- [Repository](https://github.com/clerk/clerk-sdk-php)
- [Postman Collection](collections/clerk.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/clerk.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Clerk C# / .NET SDK

Official C# / .NET SDK for the Clerk Backend API.

- **Human URL:** [https://github.com/clerk/clerk-sdk-csharp](https://github.com/clerk/clerk-sdk-csharp)
- **Base URL:** `https://github.com/clerk/clerk-sdk-csharp`

#### Tags

- SDK
- .NET
- C#
- Backend

#### Properties

- [Repository](https://github.com/clerk/clerk-sdk-csharp)
- [Postman Collection](collections/clerk.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/clerk.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Clerk OpenAPI Specifications

Public repository of OpenAPI specifications for Clerk's APIs, used as the source for generated SDKs and documentation.

- **Human URL:** [https://github.com/clerk/openapi-specs](https://github.com/clerk/openapi-specs)
- **Base URL:** `https://github.com/clerk/openapi-specs`

#### Tags

- OpenAPI
- Specifications

#### Properties

- [Repository](https://github.com/clerk/openapi-specs)
- [Postman Collection](collections/clerk.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/clerk.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [Website](https://clerk.com/)
- [Documentation](https://clerk.com/docs)
- [Git Hub](https://github.com/clerk)
- [Pricing](https://clerk.com/pricing)
- [Changelog](https://clerk.com/changelog)
- [Blog](https://clerk.com/blog)
- [Status](https://status.clerk.com/)
- [LinkedIn](https://www.linkedin.com/company/clerk-dev/)
- [L L Ms Txt](https://clerk.com/llms.txt)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
