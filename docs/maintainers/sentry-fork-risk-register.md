# Sentry fork risk register

Accepted dependency advisories, ignored in `pnpm.auditConfig.ignoreGhsas`.
Approved by Jason Orrock, 1 Nov 2026 (HRM-00367).

| Advisory | Package | Why accepted | Condition | Removal |
|---|---|---|---|---|
| GHSA-965c-763c-88jm (critical) | better-auth 1.6.22 | Upgrade to 1.7.x breaks type checks in `src/lib/auth.ts` and `scripts/cli-auth.ts`; needs an upstream code change. | Valid only with `AUTH_MODE=cloudflare_access`: Cloudflare Access rejects unauthenticated requests before better-auth endpoints are reached. Not valid for `password`, `hosted` or `local_noauth`. | Remove when upstream moves to better-auth 1.7 (flagged by the weekly upstream check). |
| GHSA-r4xp-prcw-77qf (high) | better-auth 1.6.22 | As above. | As above. | As above. |
| GHSA-q84f-53jg-9ppm (high) | better-auth 1.6.22 | As above. | As above. | As above. |
