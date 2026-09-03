# MITRE ATT&CK Mapping

| Observed / simulated behavior | Technique | ID | Relevance |
|---|---|---|---|
| Distributed failed authentication against many accounts | Brute Force: Password Spraying | T1110.003 | Primary initial-access technique represented by the dataset |
| Successful authentication using valid credentials | Valid Accounts | T1078 | Represents the credential-success stage |
| Cloud identity used for successful access | Valid Accounts: Cloud Accounts | T1078.004 | Applicable to cloud authentication scenarios |

## Analyst interpretation

The mapping should describe what the telemetry supports rather than speculate beyond the dataset.

The supplied ADX dataset does **not** contain mailbox audit events, so techniques related to mailbox forwarding rules are not claimed as observed behavior.
