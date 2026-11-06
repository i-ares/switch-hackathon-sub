# Access Approval Policy

## Tiers
Decide tier from the resource sensitivity in `directory.json` and the request.

| Tier | Condition | Action |
|------|-----------|--------|
| LOW | sensitivity=low AND read-only AND duration <= 7 days | Auto-approve. Notify owner FYI. |
| MEDIUM | sensitivity=medium, OR low resource with write access, OR duration > 7 days | Owner approves. |
| HIGH | sensitivity=high, OR admin rights, OR PII/financial data | Owner AND owner's manager both approve. Schedule a meeting. |

## Rules
- Requests with no business reason are rejected back to the requester for more info.
- Duration over 30 days is always at least MEDIUM.
- If the owner is the requester, escalate to the owner's manager instead.
- Urgent requests (needed within 24h) still follow the tier; the scheduler picks the earliest slot.
- A meeting is scheduled only for HIGH tier, or when an approver asks for one.
- Never approve on behalf of a human. Only LOW tier is auto-approved.
