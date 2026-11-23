# CLAUDE.md: unset-sh/pds

## Where this repository fits

This is `unset-sh/pds`: unset.sh's PDS image and everything that customises the PDS. It is empty for now; until
the image moves here, it is built in `Undefined6799/unset` (`deployment/pds/`).

- **Belongs here:** the first-party PDS image, built on the official `bluesky-social/pds` image with its upstream
  source and package versions pinned; the theme for its sign-in and account pages and any other change to the
  stock PDS; the image build and its release.
- **Does not belong here:** running and deploying the PDS, its environment and the process that holds its admin
  password (that is `unset-sh/deployment`); Unset's product integration with the PDS (that is `unset-sh/backend`);
  colours, fonts and the mark the theme uses (that is `unset-sh/brand`).
- **Uses:** `unset-sh/brand` at an exact version for the theme (after the move); `unset-sh/tooling` for the
  branch policy check at a full commit; `unset-sh/agent-kit` as the copy under `.claude/`. **Used by:**
  `unset-sh/deployment`, which selects released images.
- **Licence:** first-party work follows the organisation rule. The upstream PDS keeps its own licence.

The map of every unset.sh repository is <https://github.com/unset-sh/.github/blob/main/MAP.md>. Read it before
moving work between repositories or starting work that might belong elsewhere.

**Keep the map current.** When a change here adds, removes or moves a responsibility, changes what this
repository uses or ships, or renames or archives it, open a pull request on `unset-sh/.github` that updates
`repos.json` (run `npm run map` there) and update this section to match.

## Rules

- Build on the official image by digest, never a mutable tag, and record the upstream versions it pins.
- The image never contains a secret, a key or an admin password. Deployment supplies them at run time.
- Do not copy the image build from `Undefined6799/unset` without its provenance; that repository stays read-only.

## Commands

```sh
bun .claude/agent-kit/sync.mjs --check
```
