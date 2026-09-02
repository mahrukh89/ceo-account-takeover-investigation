# 02 — Baseline Analysis

A baseline prevents an analyst from treating every unusual location as malicious.

The baseline query summarizes successful CEO sign-ins by:

- location;
- hour of day.

The analyst compares the suspicious event against those normal patterns.

## Expected interpretation

A login is more suspicious when multiple independent indicators align:

- unusual geography;
- unusual time;
- successful authentication;
- source IP associated with earlier failed attempts.

**Evidence:** `06-ceo-baseline.png`

A benign comparison event is included in the dataset to demonstrate why context matters.
