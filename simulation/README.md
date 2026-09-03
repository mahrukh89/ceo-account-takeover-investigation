# Simulation Dataset

The simulation folder contains the source JSON dataset used to create the CSV used for Azure Data Explorer ingestion.

## Safe-lab purpose

The events are synthetic. They do not represent real people, credentials, organizations, or production security telemetry.

## Workflow

```text
simulated-signins.json
        ↓
cloudora_signin_logs.csv
        ↓
Azure Data Explorer ingestion
        ↓
SigninLogs_CL
        ↓
KQL investigation
```

The Python/API ingestion method from the earlier Sentinel-oriented version is intentionally not used here. The lab workflow is **Azure Data Explorer local-file ingestion**.
