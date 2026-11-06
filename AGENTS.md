# AGENTS.md — flatcap-userstyles

Flatcap 2.0 UserCSS (LESS) styles for Gemini, Gmail, Instagram and Reddit.

## Guide

- Design guide: `../00-Flatcap/SKILL.md` (public: https://github.com/cheycron/flatcap-theme). Read it before changing any color, font or focus treatment.
- `src/theme.json` is the **only** token source. Never edit the generated block between `flatcap:tokens:begin` and `flatcap:tokens:end` in `styles/*.user.less`.

## Rules

- No hex outside the generated block (except attribute selectors matching colors the sites write themselves).
- Selectors are written by hand per site; colors come from generated tokens, assigned by role.
- `@author Cheycron Blaine` in every style header; keep NOTICE.md credits for upstream authors and do not claim licenses upstream did not grant.
- Screenshots in `images/` must have personal data blurred; never commit raw captures (`.review/` is ignored).

## Before finishing

Run `python3 scripts/build.py --check` (stale blocks, stray hex, metadata drift, contrast). Use `python3 scripts/build.py` to regenerate tokens and `--sync` to refresh `src/theme.json` from `../00-Flatcap`.
