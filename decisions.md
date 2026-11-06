## 2026-11-06T15:15:25Z | ben -> github-repo | APPROVED
- tier: LOW
- reason: sensitivity=low, read-only, 3 days <= 7, business reason given
- approvers: none (auto)
- meeting: none

## 2026-11-06T15:20:44Z | ben -> prod-database | APPROVED
- tier: HIGH
- reason: sensitivity=high and admin rights; owner and manager must both approve (admin, 2 days, MIG-118 index + drop legacy_flags)
- approvers: chen (owner), priya (manager), both relayed by sam, not verified directly
- meeting: 2026-11-09 17:00-18:00 IST (chen, priya, ben)

## 2026-11-06T15:22:19Z | ben -> analytics-db | APPROVED
- tier: MEDIUM
- reason: sensitivity=medium and write access; owner is requester so manager approves (write, 14 days, DATA-77 metrics backfill)
- approvers: priya (manager, relayed by sam, not verified directly)
- meeting: none

