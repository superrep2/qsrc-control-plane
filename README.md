# QSRC — control plane (private, invite-only)

Owner: Justin Tyler Peña (`superrep2` / @DimensionsAlgo)
Visibility: **private**. Not public. Invite reviewers under Settings → Collaborators.

This is a virtual multi-agent security control plane for Grok Build apps,
connectors, and related data structures. It is not a physical quantum computer
and it does not hold live passwords.

## Open the computer

Open `console.html` in a browser (local file is enough). Mode is HOLD.
High-risk execute buttons stay dead on purpose.

## Tree

| Path | Role |
|---|---|
| `console.html` | Operator console |
| `PLAYBOOK.md` | Who may observe vs mutate |
| `APPROVAL_LEDGER.md` | A-01 deny; A-02 pending; A-03–A-10 approved |
| `OWNER_RUNBOOK.md` | Clicks only the owner can make |
| `DATA_MODEL.md` | Zones Z0–Z5 and stores |
| `REVIEW.md` | How invited reviewers should perfect this |
| `INVITE.md` | How to add people |
| `schemas/qsrc.schema.json` | Ledger JSON shape |
| `.github/workflows/guard.yml` | Reject credential filenames / token-shaped strings |

## Deliberately not in this repo

- Grok / Google / X session tokens
- `auth.json`, `mcp_credentials.json`
- Live r-sus source until exported from Grok Build into this private repo

## Live hooks outside git

- Grok Automation `qsrc-sentinel-daily` (`4342b9fb-277a-460c-9aed-2348c11b7df2`), daily 09:00 America/Chicago, observe-only
