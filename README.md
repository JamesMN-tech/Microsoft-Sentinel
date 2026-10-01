# Microsoft Sentinel Portfolio

Hands-on Microsoft Sentinel lab documentation focused on data onboarding, connector validation, identity telemetry, and evidence-based security operations.

This portfolio records what I configured, the results I could verify, and the work still needed. It distinguishes completed lab activities from proposed exercises and untested query examples.

## Featured lab

### Microsoft Entra ID and threat intelligence onboarding

[Read the full technical report](labs/01-entra-id-and-threat-intelligence/README.md) · [Download the Word report](labs/01-entra-id-and-threat-intelligence/reports/microsoft-sentinel-data-ingestion-lab-report.docx)

| Area | Evidence-backed outcome |
| --- | --- |
| Entra ID solution | Connector available after installation |
| Entra ID connection | Blocked by diagnostic-settings and tenant-permission prerequisites |
| Threat intelligence solutions | Installation supported by notes and Manage controls |
| Microsoft Threat Intelligence connector | Connected status confirmed |
| IOC ingestion | Unverified: final screenshots show zero received data and no last-log timestamp |
| Detection and automation | No executed KQL, enabled analytics rules, generated alerts, or playbook runs demonstrated |

The report includes 14 captioned screenshots, chronological implementation notes, permission troubleshooting, validation results, SOC relevance, and an interview-ready skills summary. Screenshots show more than one workspace context; the report documents that limitation.

## Skills demonstrated

- Reviewing and installing Content hub solutions.
- Distinguishing solution installation from connector configuration and data receipt.
- Identifying failed source-side permissions despite passing workspace access.
- Enabling the Microsoft Threat Intelligence connector.
- Assessing connector status, receipt timestamps, and ingestion counters.
- Communicating verified results and unresolved visibility gaps accurately.

## Repository guide

```text
labs/01-entra-id-and-threat-intelligence/
  README.md       Detailed mentor-ready lab report
  evidence/       Original screenshots with descriptive filenames
  reports/        Downloadable Word report
queries/
  README.md       Query catalog, prerequisites, and validation status
  ingestion/      Table-specific ingestion checks
  identity/       Sign-in investigation starters
  threat-intelligence/  Indicator receipt checks
docs/
  learning-roadmap.md
  github-publishing.md
```

## KQL query library

[Browse the query catalog](queries/README.md). No existing KQL files were available when this portfolio was assembled. The included queries are newly prepared, untested starter examples for follow-up practice, not evidence of queries I ran during the lab.

## Next learning milestones

Resolve the Entra ID permission issue, prove data arrival with query results, investigate identity events, and then validate a detection rule and a controlled automation workflow. See the [learning roadmap](docs/learning-roadmap.md).

## Evidence and publication

The lab conclusions rely on supplied notes and screenshots. External references in the query catalog support follow-up query development only. Original images retain lab workspace and tenant labels. Repository: [JamesMN-tech/Microsoft-Sentinel](https://github.com/JamesMN-tech/Microsoft-Sentinel).

[GitHub publishing instructions](docs/github-publishing.md)
