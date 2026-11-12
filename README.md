# Hi 👋 — I keep pipelines honest

Most of my code runs where nobody watches: cron jobs, LLM pipelines, and message-delivery gates that have to behave at 3 a.m. Everything public here is **distilled from that practice** — generalized, stripped of anything traceable, and rebuilt as single-file tools you can drop into your own stack.

> **Mechanisms are real. Numbers are illustrative.**

## The tools

| Tool | The incident it prevents |
| --- | --- |
| 🛡️ [dupguard](https://github.com/ryousukefj1005-sys/dupguard) | the same notification sent twice by a retrying cron job |
| 🧩 [chartid](https://github.com/ryousukefj1005-sys/chartid) | two agents rebuilding the same chart, neither knowing the other exists |
| 🚦 [msglint](https://github.com/ryousukefj1005-sys/msglint) | a bot shipping Markdown that renders as a wall of garbage |

All three: **one file, zero dependencies, Python 3.8+**, MIT.

## Build rules I trust

- **One file, zero deps.** Anything that needs a package resolver at 3 a.m. is already broken.
- **Exit codes are the API.** `0` / `1` / `2` — shells and CI branch without parsing a thing.
- **Append-only JSONL ledgers.** Grep-able beats queryable-when-the-db-is-down.
- **Gate at the send port.** One blocked bad message beats ten dashboards after the fact.
- **Every verdict leaves a trail.** Suppressions, allocations, failures — all auditable.

## Say hi

Issues and PRs welcome on any repo. If a tool caught something your pipeline was about to ship, I want the incident story.
