# cog-hubspot-rest

HubSpot developer-platform project (marketplace OAuth, account-level) plus the future `stackmoxie/hubspot-rest` cog.

This is **not** a replacement for [`cog-hubspot`](https://github.com/Stack-Moxie/cog-hubspot) (`stackmoxie/hubspot`). It is not a `mcp.hubspot.com` client.

## HubSpot CLI

Requires Node 20+ and `@hubspot/cli`. Authenticate with `hs account auth`, then:

```bash
hs project upload
hs project dev
```

Do not change `distribution` (`marketplace`) or switch to user-level access after first upload.

OAuth callback paths (must match App routes when those land):

- `https://app.stackmoxie.com/oauth/callback/hubspot-rest`
- `https://staging-app.stackmoxie.com/oauth/callback/hubspot-rest`
- `https://dev-app.stackmoxie.com/oauth/callback/hubspot-rest`
- `http://localhost:1337/oauth/callback/hubspot-rest`

First-slice scopes are contacts + `oauth`. Expand `requiredScopes` before claiming 42-step parity.
