# Access Approval Room

A Switch room where five agents turn an access request into a decision.

| Agent | Job |
|-------|-----|
| requester | Collects a complete request |
| router | Finds the resource owner and their manager |
| approver | Applies tiered gating: auto-approve low risk, escalate high risk |
| scheduler | Finds a common meeting slot across all calendars |
| logger | Appends every decision to `decisions.md` |

## Files
- `policy.md`: tier rules
- `directory.json`: people, managers, resources (mock data)
- `calendars.json`: busy slots (mock data)
- `agents/*.md`: agent prompts

## Demo
1. "I'm Dev, read access to github-repo for 2 days to verify the changelog on release/2.4" -> LOW, auto-approved.
2. "I'm Ben, write access to analytics-db for 10 days, DATA-91" -> MEDIUM, owner is requester so manager approves.
3. "I'm Asha, admin on prod-database for 1 day, TLS rotation" -> HIGH, owner + manager approve, meeting booked.

Approvals from people outside the room are relayed by a human and logged as "relayed, not verified directly".

Calendar and directory are mocked. Real calendar integration is future work.
