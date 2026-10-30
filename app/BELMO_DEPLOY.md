# Private Belmo deployment

Use a Web Service on the Starter plan with repository root `app` and framework Go.

- Build: `go build -trimpath -o inceptionlabs2api . && go version`
- Start: `./inceptionlabs2api`
- Health check: `/healthz`
- Port: `3000`

Configure `IL2API_ADDR=:3000`, `PORT=3000`, `IL2API_MODEL=mercury-3`, and a private `IL2API_API_KEY` in the Belmo dashboard. Store the key as a secret; never commit its value to this repository. Configure the key before starting the API. Disable auto-deploy when manually validating a release.

This file documents this fork's deployment configuration. The upstream source code and license remain unchanged.
