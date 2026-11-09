# Builder stack handbook

{{badges}}

{{header_line}}

One founder's handbook for building websites, apps, dashboards, visuals and outbound with AI agents: where I get design references, the component libraries and prompt packs I start from, how I ship and check what the agent built, the image and video stack, which scraper for which data, and the skills I hand Claude Code. It merges my private Notion notes with the public link directory at [agentmatik.ai/links](https://agentmatik.ai/links). It is not a directory of everything that exists - if something is here, it earned its place in real work. The longer notes live in [FIELD-NOTES.md](FIELD-NOTES.md). Suggest a link by opening an issue (see [CONTRIBUTING.md](CONTRIBUTING.md)).

Descriptions are my own notes where I wrote one. Where I only saved a link, the description is the repository's, the page's or the post's own summary. A suffix like `(free, no account)`, `(free account)` or `(paid)` is the access label from the agentmatik.ai directory, and a `Why:` that says "we" or "our" is that directory's reason, written for Agentmatik's clients. Ratings like `(Matt: 8/10)` are my personal scores.

## Contents

{{toc}}

{{start_here}}

{{sections}}

## How this list is built

The sources are four private Notion pages where I keep notes while I work (websites and apps, photos and video, scraping, GTM) and the public link directory at agentmatik.ai/links. A sync script in my workspace (`awesome-sync.py`, not in this repo) reads the pages through the Notion API and keeps only the sections that are explicitly mapped as public - everything else stays private by default. It canonicalizes every URL (https only, tracking parameters dropped, `youtu.be` and `twitter.com` rewritten), drops links to private places (Notion, Google Drive, course platforms, local addresses), scans every string for secrets and private names, merges the directory by canonical URL (my notes win on names and descriptions; the directory fills in a missing "why" and its access label), and writes three files: `data/links.csv` (one row per link), `data/notes.json` (the field notes) and `data/_report.md` (what was excluded and why).

From there everything is automated and reproducible from this repo alone:

- `tools/enrich.py` checks every link and writes `data/enrichment.json`: stars, license, last push and archive state from the GitHub API (renamed repositories are followed), titles from YouTube and X oEmbed, and a plain HTTP check with a browser user agent for everything else.
- `tools/build.py` renders this README and `FIELD-NOTES.md` from `data/` + `config/sections.json` + `templates/`. Links stay here, every note goes to the notes file, grouped by the same sections. Entries are sorted by name inside each section; the build is deterministic, so running it twice produces the same files.
- `tools/lint.py` fails on dead links, descriptions under 30 characters, duplicate names or URLs, non-https links, tracking parameters, links to private hosts, long dashes, placeholders, thin sections and broken table-of-contents anchors - in both files. Whatever it cannot fix on its own is listed under "Open decisions" in `data/_report.md`.
- A weekly GitHub Action (`.github/workflows/links.yml`) re-runs the checks and opens a pull request when either file changes. `data/_dead.md` lists what needs a human look.

Nothing in this README or in `FIELD-NOTES.md` is edited by hand. Fixes go to `data/overrides.json` (keyed by the entry id in `data/links.csv`, or by block id under `_notes` for a note) and the next build picks them up.

{{stats}}

## License

The content of this list (README, FIELD-NOTES and the files in `data/`) is licensed under [CC BY 4.0](LICENSE) - share and adapt it with attribution. The scripts in `tools/` are MIT licensed ([LICENSE-CODE](LICENSE-CODE)).
