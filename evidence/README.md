# Evidence Screenshot Plan

Add your screenshots to this folder using the exact names below. **Do not upload screenshots containing passwords, subscription IDs, tenant IDs, access keys, tokens, or personal information.**

| # | Filename | Capture when | What must be visible |
|---|---|---|---|
| 01 | `01-adx-environment.png` | ADX opened | Cluster + database context |
| 02 | `02-database-table.png` | Database/table created | `CEOAccountTakeoverDB` and `SigninLogs_CL` |
| 03 | `03-csv-ingestion-preview.png` | During CSV upload | File name + column preview/mapping |
| 04 | `04-ingestion-success.png` | After ingestion | Successful ingestion/result |
| 05 | `05-raw-data.png` | Run `SigninLogs_CL \| take 10` | Query + returned rows |
| 06 | `06-ceo-baseline.png` | Run baseline query | Query + baseline results |
| 07 | `07-suspicious-ceo-login.png` | Run suspicious-login query | Query + suspicious CEO event |
| 08 | `08-password-spray.png` | Run spray hunt | Query + IP/failed attempts/distinct users |
| 09 | `09-spray-to-success.png` | Run pivot | Query + source IP linked to success |
| 10 | `10-comparison-event.png` | Run benign comparison | Query + colleague/normal event |

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
