# Access Decisions

## 2026-11-07T11:04:02Z | dev -> github-repo | APPROVED
- tier: LOW
- reason: sensitivity=low, read-only, 2 days <= 7, business reason given (read, verify changelog on release/2.4); no human approval needed
- approvers: none (auto)
- meeting: none

## 2026-11-07T11:09:48Z | ben -> analytics-db | APPROVED
- tier: MEDIUM
- reason: sensitivity=medium and write access; owner is requester so manager approves (write, 10 days, DATA-91 dashboard metrics fix)
- approvers: priya (manager, relayed by sam, not verified directly)
- meeting: none

## 2026-11-07T11:10:50Z | asha -> prod-database | APPROVED
- tier: HIGH
- reason: sensitivity=high and admin rights; owner and manager must both approve (admin, 1 day, TLS certificate rotation)
- approvers: chen (owner), priya (manager), both relayed by sam, not verified directly
- meeting: 2026-11-09 17:30-18:00 IST (chen, priya, asha)

