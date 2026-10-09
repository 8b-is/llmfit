# Upstream provenance

This repository is the **8b-is fork** of
<https://github.com/AlexsJones/llmfit> — a WebAssembly-free, pure-Rust tool
that matches open-source LLMs to local hardware. The fork keeps upstream's
history; it is not a history-free snapshot.

- Upstream: <https://github.com/AlexsJones/llmfit>
- Fork: <https://github.com/8b-is/llmfit>
- Fork point (and current upstream HEAD at fork time): `781e76a`
- Upstream version at fork point: `1.1.17`
- License: MIT (see `LICENSE`); the fork does not relicense the work.

## Keeping in sync

`upstream` is wired as a remote so the fork can track the project it came
from:

```bash
git remote add upstream https://github.com/AlexsJones/llmfit.git   # once
git fetch upstream
git merge upstream/main        # or: git rebase upstream/main
git push origin main
```

## What the fork is for

Same engine, the 8b-is constellation's point of view on it: the
hardware↔model fit decision is the local-first, "what actually runs here"
question the constellation cares about (see `docs/constellation.md` when it
lands). Divergence from upstream should stay small and landed as reviews
that can flow back — the goal is contribution, not a private island.
