# 01 — Triage

## Alert hypothesis

The investigation starts with a suspected compromise of `ceo@company.com`.

The first triage question is:

> Is the successful CEO authentication consistent with the account's normal behavior?

## Triage checks

1. Confirm the event is a successful authentication (`ResultType == 0`).
2. Review source IP and reported location.
3. Compare the event with the CEO baseline.
4. Determine whether the source IP appears in earlier failed-authentication activity.
5. Preserve the query result as evidence.

## Initial assessment

The supplied simulation is designed so that the CEO success event is geographically and temporally unusual and follows password-spray activity. The result should be validated directly in ADX before being described as a confirmed compromise.

**Evidence:** `07-suspicious-ceo-login.png`
