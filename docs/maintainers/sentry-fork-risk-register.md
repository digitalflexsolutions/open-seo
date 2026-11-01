# Sentry fork risk register

Accepted dependency advisories, ignored in `pnpm.auditConfig.ignoreGhsas`.
Approved by Jason Orrock, 1 Nov 2026 (HRM-00367).

## better-auth 1.6.22

- Advisories: GHSA-965c-763c-88jm (critical), GHSA-r4xp-prcw-77qf (high), GHSA-q84f-53jg-9ppm (high).
- Why accepted: upgrading to 1.7.x breaks type checks in `src/lib/auth.ts` and `scripts/cli-auth.ts`, which needs an upstream code change.
- Condition: valid only with `AUTH_MODE=cloudflare_access`. Cloudflare Access rejects unauthenticated requests before better-auth endpoints are reached. Not valid for `password`, `hosted` or `local_noauth`.
- Removal: when upstream moves to better-auth 1.7, flagged by the weekly upstream check.
