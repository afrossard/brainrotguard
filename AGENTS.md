# Agent instructions

## Fork

This repo is a fork of `GHJJ123/brainrotguard`, and all work stays in the fork, `afrossard/brainrotguard`.
Open pull requests and issues against `afrossard/brainrotguard`, passing `--repo afrossard/brainrotguard` to `gh` so it never resolves to the upstream parent.
The `upstream` remote points at `GHJJ123/brainrotguard`.
Port upstream changes only when asked, as a reviewed merge of `main..upstream/main` (see `docs/adr/0001-fork-maintenance.md`).
Cut branches meant for an upstream PR from `upstream/main`, so they carry none of the fork's own changes.

## Agent skills

### Issue tracker

Issues live in GitHub Issues on the fork, `afrossard/brainrotguard`. See `docs/agents/issue-tracker.md`.

### Triage labels

The five default triage labels, each named after its role. See `docs/agents/triage-labels.md`.

### Domain docs

Single-context: one `GLOSSARY.md` and `docs/adr/` at the repo root. See `docs/agents/domain.md`.
