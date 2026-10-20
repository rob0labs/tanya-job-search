# tanya-job-search

Weekly job board for Tanya. Served by Cloudflare Workers static assets at https://tanya-job-search.rob0labs.workers.dev

- `public/index.html` is the board shell. It is written once and never rewritten by weekly runs.
- Weekly runs add `public/data/scans/YYYY-MM-DD.json` and append the file name to `public/data/manifest.json`.
- Config is `wrangler.toml`. Do not switch to `wrangler.jsonc`: the wrangler-action default (3.90) does not read it and fails with "Missing entry-point".
