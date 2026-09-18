# QSRC Playbook

## Standing orders

1. Observe first. Write second. Mutate never without an approval ID.
2. High-risk = anything that changes auth, visibility, secrets, DNS, billing, or other people's data.
3. The owner's written approve A-xx is the only promotion from PENDING_OWNER to IN_PROGRESS.
4. Prefer export-and-diff over the model said it fixed it.
5. If a finding sounds like intrusion and the code says login-bypass, treat it as an intentional control until git history says otherwise.

## Agent authorities

| Agent | May do without approval | May not do |
|---|---|---|
| Sentinel | Read public URLs, status pages, X public posts | Change apps, ban users, page third parties |
| Gatekeeper | Draft patches, point at the bypass module | Publish, delete OAuth clients |
| Archivist | Map data stores and retention | Wipe logs, change DB schemas in prod |
| Mesh | Diagram MCP / OAuth / connectors | Re-auth or revoke tokens |
| Publisher | List grok.me apps and access modes | Flip visibility, disable remix |
| Identity | List accounts that exist | Rotate or revoke |
| Counsel | Risk language | Speak as your lawyer |

## A-01 status

Owner denied A-01 on 2026-09-18 15:33 CDT. Do not remove the Help long-press bypass. Do not republish for that ticket.

## After A-02 through A-04

1. Export r-sus from Grok Build to this private git repo.
2. Leave the Help / sessionStorage bypass in place (A-01 denied).
3. Wrap `/`, `/_serverFn/*`, and log archive behind server session checks.
4. Drop IP/geo from guest view.
5. Add CSP + frame-ancestors 'none'.
6. Lock grok.me to author-only or link-gated.
7. Re-test: anonymous user must not reach observatory chrome if A-02 is approved.
