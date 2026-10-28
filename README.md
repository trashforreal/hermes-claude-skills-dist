# hermes-claude-skills-dist

Payload for a claude.ai/code environment setup script. `hermes-plugins.tar.gz` contains nine Claude Code plugins
under `plugins/<name>/`, each with its own licence file; `SHA256SUMS` holds the tarball's sha256. The setup script
fetches the tarball by commit SHA from raw.githubusercontent.com and checks the sha256 before installing.

| Plugin | Upstream (pinned) | Licence |
|---|---|---|
| pstack 0.15.32 | https://github.com/cursor/plugins @ 99b609a, harness/pstack/claude-code (make-bot-ui removed) | MIT |
| ponytail 5.3.2 | https://github.com/DietrichGebert/ponytail @ 09c434ab (Claude Code files only) | MIT |
| agentic-actions-auditor, differential-review, insecure-defaults, sharp-edges, static-analysis, supply-chain-risk-auditor | https://github.com/trailofbits/skills @ 196a907, © Trail of Bits | CC BY-SA 4.0, https://creativecommons.org/licenses/by-sa/4.0/ |
| sentry-picks | https://github.com/getsentry/skills @ d12f250 (selected skills) | Apache-2.0 |

Licence texts: `plugins/<name>/LICENSE` inside the tarball. The tarball is a deterministic `tar | gzip -n` of the
`plugins/` folder of a private repo; nothing else is added. It contains no Anthropic-proprietary material.
