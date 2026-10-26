# identity-service

Accounts and sign-in. This service is our own OAuth 2.0 / OpenID Connect provider: people sign in with a passkey, and the app gets a token that every other service and the API gateway can verify against our JWKS.

It also keeps track of organizations, roles and each user's devices, and it signs the credential that ties a device's encryption key to its owner, so the other members of a conversation know who they are talking to.

Built with .NET 10, ASP.NET Core Identity and OpenIddict, backed by PostgreSQL. A small read-only GraphQL endpoint serves the organization admin page.

Owner: Tibor Koderman. Status: planned, work starts in early November.

## Where this fits

This is one of the repositories of [Pretty Good Pigeon](https://github.com/rso-ekipa13), an end-to-end encrypted messenger built by ekipa 13 for the Cloud Computing course at UL FRI (2026/27). The architecture, plan and decisions live in [docs](https://github.com/rso-ekipa13/docs).

`main` only changes through pull requests; day-to-day work goes to `dev`.
