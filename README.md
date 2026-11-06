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
1. "I need read access to the github-repo for 3 days to review a PR" -> auto-approved.
2. "I need write access to analytics-db for 14 days" -> owner approval.
3. "I need admin on prod-database for a migration" -> owner + manager approval, meeting booked.

Calendar and directory are mocked. Real calendar integration is future work.
