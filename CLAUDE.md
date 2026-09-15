# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Commands

Run the test suite:

```bash
PYTHONPATH=. python -m unittest tests.test_greet -v
```

`unittest discover` does not work here because `tests/` has no `__init__.py`; invoke the test module directly as shown above, with the repo root on `PYTHONPATH` so `greet` is importable.

## Architecture

This is a minimal practice repository: a single top-level module, `greet.py`, exposing one function (`greet`), with its test in `tests/test_greet.py`. There is no build step, package structure, or dependency beyond the standard library.

## Agent skills

### Issue tracker

Issues live in GitHub Issues for `suhrobbek0628-jpg/first-pr-practice`, managed with the `gh` CLI. See `docs/agents/issue-tracker.md`.

### Triage labels

Default five-role vocabulary: `needs-triage`, `needs-info`, `ready-for-agent`, `ready-for-human`, `wontfix`. See `docs/agents/triage-labels.md`.

### Domain docs

Single-context: one `CONTEXT.md` plus `docs/adr/` at the repo root (created lazily). See `docs/agents/domain.md`.
