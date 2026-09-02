# 04 — Containment & Response Recommendations

This lab does **not** execute containment actions against a real tenant. The following are analyst recommendations that would normally follow confirmation.

## Immediate

1. Reset the affected account's password.
2. Revoke active sessions/tokens.
3. Enforce MFA for the account.
4. Review recent authentication activity.
5. Block or investigate confirmed malicious source infrastructure according to organizational policy.

## Follow-up

- Review mailbox and cloud audit logs if available.
- Search for OAuth/app-consent changes.
- Review privilege assignments.
- Check for additional compromised accounts.
- Tune password-spray detection thresholds.

## Portfolio note

These actions are documented as recommendations only. The ADX dataset supplied with this project contains sign-in telemetry, so it cannot prove mailbox persistence, data exfiltration, or token theft.
