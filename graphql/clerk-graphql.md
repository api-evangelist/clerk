# Clerk GraphQL

## Overview

Clerk's public API surface is REST-based. The Backend API lives at `https://api.clerk.com/v1` and is documented at [https://clerk.com/docs/reference/backend-api](https://clerk.com/docs/reference/backend-api). An OpenAPI specification is maintained at [https://github.com/clerk/openapi-specs](https://github.com/clerk/openapi-specs).

As of June 2026, Clerk does **not** publish a native GraphQL endpoint. A POST to `https://api.clerk.dev/v1/graphql` with an introspection query returns an authentication error rather than a schema, indicating no public GraphQL surface is exposed.

The schema in `clerk-schema.graphql` is a **conceptual GraphQL data model** derived from the REST API's resource types and documented object shapes. It is suitable for:

- Tooling and code generation
- Federated API design (e.g., wrapping Clerk behind a GraphQL gateway)
- Documentation of the Clerk data model in SDL form

## Schema Source

**Type:** Conceptual (REST-derived)
**Source:** [Clerk Backend API Reference](https://clerk.com/docs/reference/backend-api)
**OpenAPI Spec:** [https://github.com/clerk/openapi-specs](https://github.com/clerk/openapi-specs)

## Types Modeled

The schema covers the following Clerk resource types:

| Type | Description |
|---|---|
| `User` | Core user account with identifiers, metadata, and MFA state |
| `Session` | Active or historical user session |
| `Client` | Browser/device context containing sessions |
| `SignIn` | In-progress sign-in flow |
| `SignUp` | In-progress sign-up flow |
| `Organization` | B2B / multi-tenant organization |
| `OrganizationMembership` | A user's role within an organization |
| `OrganizationInvitation` | Pending invitation to join an organization |
| `OrganizationDomain` | Verified domain linked to an organization |
| `EmailAddress` | Verified or unverified email attached to a user |
| `PhoneNumber` | Verified or unverified phone number attached to a user |
| `ExternalAccount` | OAuth account linked to a user |
| `Web3Wallet` | Web3 wallet address |
| `Passkey` | WebAuthn passkey credential |
| `IdentificationLink` | Link between an identifier and an external account |
| `SamlAccount` | SAML account linked to a user |
| `SamlConnection` | Enterprise SSO SAML connection |
| `OAuthToken` | OAuth access token for an external account |
| `SignInToken` | Short-lived ticket / magic-link token |
| `ActorToken` | Token for user impersonation flows |
| `Token` | Signed JWT for a session |
| `JWTTemplate` | Custom JWT claims template |
| `AllowlistIdentifier` | Email/domain on the signup allowlist |
| `BlocklistIdentifier` | Email/domain on the signup blocklist |
| `Permission` | Granular permission key |
| `Role` | Named role composed of permissions |
| `ApplicationConfig` | Instance-level auth configuration |
| `Domain` | Custom domain for a Clerk instance |
| `ProxyConfig` | Proxy routing configuration |
| `Redirect` | Registered redirect URL |
| `PublishableKey` | Frontend publishable key |
| `WebhookEndpoint` | Svix webhook endpoint registration |
| `Verification` | Verification state for any identifier |

## Enums

`UserStatus`, `SessionStatus`, `OrganizationMembershipRole`, `InvitationStatus`, `IdentifierType`, `OAuthProvider`, `SignInStrategy`, `SignInStatus`, `SignUpStatus`, `TokenAlgorithm`, `PermissionType`

## Notes on Clerk's API Architecture

- **Authentication:** The Backend API uses Bearer secret keys (`sk_test_...` / `sk_live_...`). The Frontend API uses publishable keys and short-lived client tokens.
- **Pagination:** REST endpoints accept `limit` and `offset`; the GraphQL schema mirrors this pattern.
- **Metadata:** Clerk supports three metadata buckets per user: `publicMetadata` (readable by client), `privateMetadata` (server-only), and `unsafeMetadata` (user-writable, not trusted).
- **Webhooks:** Lifecycle events are delivered via Svix. See `asyncapi/clerk-webhooks-asyncapi.yml` for the event schema.
- **Organizations:** Role keys and permission keys are strings; the system roles `org:admin` and `org:member` are always present. Custom roles are defined per instance.

## References

- Backend API Docs: [https://clerk.com/docs/reference/backend-api](https://clerk.com/docs/reference/backend-api)
- Frontend API Docs: [https://clerk.com/docs/reference/frontend-api](https://clerk.com/docs/reference/frontend-api)
- OpenAPI Specs: [https://github.com/clerk/openapi-specs](https://github.com/clerk/openapi-specs)
- JavaScript SDK: [https://github.com/clerk/javascript](https://github.com/clerk/javascript)
- Webhooks: [https://clerk.com/docs/integrations/webhooks/overview](https://clerk.com/docs/integrations/webhooks/overview)
