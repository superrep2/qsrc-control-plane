# QSRC Data Structure

## Trust zones

Z0 owner devices
Z1 Grok account + Grok Build project
Z2 published *.grok.me apps
Z3 Google / X
Z4 connectors (GitHub, Voice, Automations)
Z5 visitor browsers hitting r-sus — untrusted

## Stores discovered

| Store | Zone | Risk |
|---|---|---|
| sessionStorage r-sus-login-bypass | Z5 | Auth theater |
| sessionStorage r-sus-obs-session | Z5 | Tracking |
| localStorage r-sus-monitor-v1 | Z5 | Tamperable toy state |
| /api/auth/get-session | Z2 | Real auth if enforced |
| Cookie __Host-grok_gate_session | Z2 | Must be HttpOnly/Secure |
| ~/.grok/mcp_credentials.json | Z0 | Device secret — never commit |
| ~/.grok/auth.json | Z0 | Device secret — never commit |
| session server logs | Z1/Z2 | PII if enabled |
| Grok project 01a09664-f0f0-7013-8458-613f472387be | Z1 | Remix / collaborator risk |

Do not put secrets in ledger records. Handles and last-rotated timestamps only.
