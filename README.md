# openapi-sdk

Fork of [`digitalocean/openapi`](https://github.com/digitalocean/openapi)
used as the controlled spec source for the SDK generation POC.

For the POC we do **not** auto-sync from upstream — pull updates manually
when needed (`git pull upstream main`). Once the pipeline is proven we'll
move this onto the main `openapi` repo and retire the fork.

## What lives here

- The full OpenAPI spec (mirrored from upstream).
- `.github/workflows/dispatch.yml` — fires on every push to `main` and
  fans out a `repository_dispatch` to each SDK output repo
  (`godo-next`, `pydo-next`, `dots-next`).

## Triggering manually

GitHub UI → Actions → "dispatch sdk regen" → Run workflow → pick a SHA
(or leave blank to use `main`).
