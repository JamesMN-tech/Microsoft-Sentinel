# KQL Query Catalog

All five queries are **untested starter examples** created when assembling this portfolio. No executed query or result was supplied with the lab. Schema references do not substitute for successful execution in a workspace.

| Query | Purpose | Required table | Status |
| --- | --- | --- | --- |
| [Sign-in ingestion](ingestion/signinlogs-ingestion-check.kql) | Count records and inspect the latest timestamp over 24 hours | SigninLogs | Untested |
| [Audit ingestion](ingestion/auditlogs-ingestion-check.kql) | Count records and inspect the latest timestamp over 24 hours | AuditLogs | Untested |
| [Indicator ingestion](threat-intelligence/indicator-ingestion-check.kql) | Check indicator receipt over seven days | ThreatIntelIndicators | Untested |
| [Recent unsuccessful sign-ins](identity/recent-signin-failures.kql) | Review up to 100 recent nonzero sign-in results | SigninLogs | Untested |
| [Unsuccessful sign-in summary](identity/signin-failure-summary.kql) | Group nonzero results by user and application | SigninLogs | Untested |

## How to validate

1. Select the intended Sentinel workspace and verify query permissions.
2. Confirm the required connector and log category are configured. Entra ID collection was blocked in the documented lab.
3. Open Logs and run one query at a time. Ensure the portal time range covers the query lookback.
4. Record the workspace, UTC execution time, selected range, result, and any errors.
5. Add a sanitized result screenshot to the relevant lab and update the query status only after execution is verified.

The ingestion queries return a record count and latest TimeGenerated value. A zero count and empty latest timestamp mean no matching records in that query window; a missing-table or permission error is a different outcome. Counts measure records, not distinct indicators or verified threats. A recent record does not establish completeness or sustained collection health.

Nonzero sign-in results require interpretation. They can include authentication or policy-related outcomes and do not by themselves establish malicious activity. These examples are investigation aids, not validated production detections. User names and IP addresses in results should be reviewed before adding screenshots to a public portfolio.

## Organization convention

Use descriptive kebab-case filenames. Keep ingestion checks separate from investigations. Each query should identify its required table and execution status. Future validated queries should link to a lab result rather than merely changing a status label.

## Microsoft reference material

- [SigninLogs table schema](https://learn.microsoft.com/en-us/azure/azure-monitor/reference/tables/signinlogs)
- [Microsoft SigninLogs query examples](https://learn.microsoft.com/en-us/azure/azure-monitor/reference/queries/signinlogs)
- [ThreatIntelIndicators table schema](https://learn.microsoft.com/en-us/azure/azure-monitor/reference/tables/threatintelindicators)

These references support the starter query work. They are not evidence of lab completion.
