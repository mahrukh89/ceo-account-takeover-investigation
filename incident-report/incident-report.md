# Incident Report — Simulated CEO Account Takeover

**Platform:** Microsoft Azure Data Explorer  
**Investigation type:** SOC / Threat Hunting Lab  
**Severity:** High (simulated)  
**Status:** Investigation demonstrated; containment recommendations documented  
**Data classification:** Simulated

## Executive Summary

A simulated authentication dataset was investigated for indicators of a CEO account takeover. KQL analysis in Azure Data Explorer was used to establish a CEO authentication baseline, identify an unusual successful login, detect distributed password-spray activity, and pivot from suspicious source infrastructure to successful authentication.

The scenario is designed to demonstrate a realistic SOC investigation workflow without using real credentials or production telemetry.

## Investigation Scope

- `ceo@company.com` authentication events
- failed authentication activity across multiple accounts
- source IP analysis
- geographic and temporal baseline
- successful-login correlation

## Key Findings

### 1. Suspicious CEO authentication

The dataset contains a successful CEO authentication that is intentionally positioned as an anomalous event for the investigation.

### 2. Password-spray behavior

Failed authentication events are distributed across multiple accounts. Grouping by source IP and one-hour window exposes the spray pattern more effectively than looking at a single account.

### 3. Spray-to-success relationship

The pivot query checks whether candidate spray infrastructure later produced successful authentication events, providing an evidence chain from attempted credential access to successful access.

## Impact Assessment

The simulated scenario represents compromise of a high-value executive account. In a real environment, potential impact would include access to corporate email, files, applications, and any privileged resources assigned to the account.

No real data access or exfiltration is demonstrated by this lab.

## Root Cause Hypothesis

The scenario is consistent with weak authentication defenses against distributed password spraying and insufficient controls around anomalous executive sign-ins.

## Recommendations

1. Enforce MFA for executive and privileged accounts.
2. Use identity-risk and conditional-access controls where available.
3. Monitor distributed password-spray behavior across many accounts.
4. Review anomalous geographic and time-of-day authentication.
5. Revoke sessions and reset credentials after confirmed compromise.
6. Review cloud audit logs for post-compromise activity.

## Evidence

| Finding | Evidence |
|---|---|
| ADX environment/table | `01-adx-environment.png`, `02-database-table.png` |
| Ingestion | `03-csv-ingestion-preview.png`, `04-ingestion-success.png` |
| Raw telemetry | `05-raw-data.png` |
| CEO baseline | `06-ceo-baseline.png` |
| Suspicious login | `07-suspicious-ceo-login.png` |
| Password spray | `08-password-spray.png` |
| Spray → success | `09-spray-to-success.png` |
| Comparison | `10-comparison-event.png` |

## Conclusion

This project demonstrates an end-to-end analyst workflow using Azure Data Explorer: **ingest → baseline → detect → hunt → pivot → document → recommend**.

The evidence screenshots should be added only after the queries have been run in the analyst's own ADX environment.
