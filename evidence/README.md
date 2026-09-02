# Evidence Screenshot Plan

Add your screenshots to this folder using the exact names below. **Do not upload screenshots containing passwords, subscription IDs, tenant IDs, access keys, tokens, or personal information.**

| # | Filename | Capture when | What must be visible |
|---|---|---|---|
| 01 | `01-adx-environment.png` | ADX opened | Cluster + database context |
| 02 | `02-database-table.png` | Database/table created | `CEOAccountTakeoverDB` and `SigninLogs_CL` |
| 03 | `03-ceo-baseline.png` | Run CEO profile query | CEO identity details (`UserPrincipalName`, `NormalLocation`, `NormalDevice`) |
| 04 | `04-ceo-normal-baseline.png` | Run normal login baseline | Aggregated successful logins, locations, and normal devices |
| 05 | `05-password-spray-hunt.png` | Run spray hunt query | Top source IPs (`IPAddress`), `TargetedAccounts`, `Attempts`, and date ranges |
| 06 | `06-password-spray-evidence.png` | Run spray evidence query | Failed attempts (`50126`), attacker IP (`102.89.44.17`), and targeted application |
| 07 | `07-ceo-targeted.png` | Run targeted attack query | Detailed failed login events for `ceo@cloudora.com` |
| 08 | `08-ceo-compromise.png` | Run compromise query | Successful high-risk logins (`atRisk`, `Linux`, `Chrome 116.0`) from attacker IP |
| 09 | `09-post-compromise-activity.png` | Run timeline comparison | Sequence comparing normal Lahore/Windows logins to Lagos/Linux activity |
| 10 | `10-kql-correlation.png` | Run KQL correlation query | Stage tagging (`Password Spray - Other A
## Screenshot rules

- Keep the **KQL query and result grid visible in the same screenshot** whenever possible.
- Make the table/database context visible when it helps prove the query ran against the intended dataset.
- Avoid cropping away query names or result headers.
- Use one screenshot per proof point; do not submit multiple near-identical screenshots unless required.
- Number screenshots exactly as above so they match the report.

## Evidence mapping

- Ingestion proof → 01–05
- Detection → 06–07
- Threat hunting → 08–09
- Comparison / validation → 10

The screenshots are intentionally left empty in the repository so you can add evidence from **your own Azure Data Explorer session**.
