# AGENTS.md

## Cursor Cloud specific instructions

This repository is the special GitHub **profile README** repo (`rachdelaguila/rachdelaguila`).
Its only tracked content is `README.md`, which renders on the owner's GitHub profile page.
There is **no application code, no build system, no test suite, and no lint config** — the
"product" is the rendered `README.md`.

### Previewing changes (the dev loop)

Use [`grip`](https://github.com/joeyespo/grip) to preview `README.md` exactly as GitHub
renders it. It is installed by the update script (`pip install --user grip`), so the `grip`
binary lives in `~/.local/bin` — invoke it as `~/.local/bin/grip` if `~/.local/bin` is not on
your `PATH`.

- Live preview server: `~/.local/bin/grip README.md 0.0.0.0:6419`, then open
  `http://localhost:6419`. `grip` reads the file on each request, so editing `README.md` and
  refreshing the browser shows the update (no separate live-reload).
- Export to standalone HTML: `~/.local/bin/grip README.md --export out.html`.

### Gotcha: GitHub API rate limits

`grip` renders through GitHub's Markdown API. Anonymous requests are rate-limited (~60/hour),
which is plenty for occasional previews. If you hit `403`/rate-limit errors, authenticate with
`~/.local/bin/grip README.md --user <github-user> --pass <token>` (or set a token) to raise the
limit. Local Markdown offline rendering is available via `grip --norender` but does not match
GitHub's styling as closely.
