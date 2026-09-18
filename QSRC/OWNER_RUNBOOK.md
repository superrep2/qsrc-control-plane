# Owner runbook after approve A-03 through A-10

Approved: 2026-09-18 15:35 CDT
A-01 remains DENIED. A-02 remains PENDING.

## Done from this session

- A-06 landing zone: private repo https://github.com/superrep2/qsrc-control-plane
- A-08 policy: sibling apps stay public; no takedown
- A-10: Automation qsrc-sentinel-daily id 4342b9fb-277a-460c-9aed-2348c11b7df2
  next run 2026-09-19 09:00 America/Chicago, app notification only, observe-only prompt
- A-09: extra GitHub scope card was unavailable this turn; current connector created the repo

## You still have to click (agents cannot)

### A-03 IP/geo (r-sus)
In Grok Build project 01a09664-f0f0-7013-8458-613f472387be:
- Do not strip the Help bypass (A-01 denied).
- Guest Overview: do not show IP / city / region / coordinates.
- Signed-in archive: off unless a new ticket says opt-in.
- If an archive exists, retention 24h then delete.
- Republish only that privacy change.

### A-04 r-sus visibility
Grok Build access: author only or anyone-with-link. Remix off if the control exists.

### A-05 rotation (owner only)
Google, X, Grok, GitHub: sign out all sessions, enable 2FA, grok login again, revoke old PATs.

### A-06 export
Grok Build Export to GitHub to superrep2/qsrc-control-plane (private). No mcp_credentials.json or auth.json.

### A-07 MCP
grok --version >= 1.0.36 before re-auth. Never paste client secrets into chat.

### A-09
Reconnect GitHub in Grok connectors if notifications still 403.
