# 03 — Initial Access Investigation

## Hypothesis

The attacker may have used password spraying rather than repeatedly attacking a single account.

### Hunting logic

The password-spray query groups failed authentications by:

- source IP;
- one-hour window;
- failed-attempt count;
- number of distinct targeted users.

A source is treated as interesting when it has at least 20 failed attempts against at least 5 distinct accounts in the same hour.

## Pivot

After identifying candidate spray IPs, the investigation pivots back into all authentication events from those IPs.

The key question is:

> Did an IP that sprayed multiple accounts later achieve a successful login?

If the answer includes the CEO account, the evidence chain becomes substantially stronger.

**Evidence:** `08-password-spray.png` and `09-spray-to-success.png`
