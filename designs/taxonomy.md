# Client-Context Field Taxonomy — Piggy Banker

Use this as a prompt reference when designing UI flows in Paper.

---

## CLIENT / WORKSPACE

### Create Client Form
| Field | Type | Options | Required |
|-------|------|---------|----------|
| Client Name | text | Free text (e.g. "Freedom Travel") | Yes |
| Entity Type | dropdown | See below | Yes |
| Primary Contact Email | email | Client's main contact | Yes |
| Primary Contact Name | text | Contact person name | No |
| Phone | phone | Business phone | No |
| Industry | dropdown | See below | No |
| Deploy Baseline Agent | checkbox | Auto-deploy standard agent template | Default: checked |

### Entity Type Dropdown
| Value | Label |
|-------|-------|
| `llc` | LLC |
| `s_corp` | S-Corp |
| `c_corp` | C-Corp |
| `partnership` | Partnership |
| `sole_prop` | Sole Proprietorship |
| `trust` | Trust |
| `nonprofit` | Non-Profit / 501(c)(3) |
| `other` | Other |

### Industry Dropdown
| Value | Label |
|-------|-------|
| `travel_hospitality` | Travel & Hospitality |
| `real_estate` | Real Estate |
| `professional_services` | Professional Services |
| `healthcare` | Healthcare |
| `retail_ecommerce` | Retail & E-Commerce |
| `saas_technology` | SaaS / Technology |
| `manufacturing` | Manufacturing |
| `construction` | Construction |
| `media_entertainment` | Media & Entertainment |
| `food_beverage` | Food & Beverage |
| `financial_services` | Financial Services |
| `education` | Education |
| `other` | Other |

### Client Status
| Value | Label | Badge Color | Description |
|-------|-------|-------------|-------------|
| `active` | Active | Sage green | Fully operational workspace |
| `onboarding` | Onboarding | Neutral gray | Setup in progress |
| `trial` | Trial | Neutral gray | Trial period |
| `paused` | Paused | Coral | Temporarily suspended |
| `churned` | Churned | Red | No longer active |

### Client Table Columns (Mission Control)
| Column | Type | Format | Sort |
|--------|------|--------|------|
| Client | text + avatar | Initials badge + name | Alpha |
| Status | badge | Colored status pill | Enum |
| Last Sync | relative time | "23h ago", "2d ago", "never" | Timestamp |
| Cash | currency | "$129,418.00" | Numeric |
| Runway | text | "6mo", "—" (if unknown) | Numeric |
| Open Approvals | number | Integer count, coral if > 0 | Numeric |
| Agent Health | badge | "healthy", "mixed", "setup", "error" | Enum |

---

## AGENTS

### Agent Template Fields
| Field | Type | Options | Notes |
|-------|------|---------|-------|
| Template Name | text | e.g. "Weekly CFO Brief" | Required |
| Agent Type | dropdown | See below | Required |
| Description | textarea | What this agent does | Required |
| Trigger | dropdown | See below | When agent runs |
| Status | enum | See below | Template status |
| Default Enabled | toggle | On/Off | Auto-enable on deploy |

### Agent Type Dropdown
| Value | Label | Description |
|-------|-------|-------------|
| `cfo_brief` | Weekly CFO Brief | Generates weekly financial summary |
| `expense_categorizer` | Expense Categorizer | Auto-categorizes transactions |
| `cash_flow_forecast` | Cash Flow Forecast | Projects cash position |
| `invoice_processor` | Invoice Processor | Processes incoming invoices |
| `ap_automation` | AP Automation | Accounts payable workflows |
| `ar_tracker` | AR Tracker | Accounts receivable follow-ups |
| `tax_prep` | Tax Prep Assistant | Organizes tax documents |
| `financial_reporter` | Financial Reporter | Generates financial reports |
| `budget_monitor` | Budget Monitor | Tracks spending vs budget |
| `anomaly_detector` | Anomaly Detector | Flags unusual transactions |
| `reconciliation` | Reconciliation | Bank reconciliation assistant |
| `custom` | Custom Agent | User-defined agent |

### Agent Trigger Dropdown
| Value | Label |
|-------|-------|
| `daily` | Daily |
| `weekly` | Weekly |
| `biweekly` | Bi-Weekly |
| `monthly` | Monthly |
| `on_event` | On Event (webhook/trigger) |
| `on_demand` | On Demand (manual) |
| `real_time` | Real-Time (continuous) |

### Agent Status (per client deployment)
| Value | Label | Badge Color | Description |
|-------|-------|-------------|-------------|
| `healthy` | Healthy | Sage green | Running normally |
| `active` | Active | Sage green | Currently executing |
| `paused` | Paused | Neutral gray | Manually paused |
| `setup` | Setup Required | Coral | Needs configuration |
| `deploying` | Deploying | Neutral gray | In progress |
| `error` | Error | Red | Failed, needs attention |
| `disabled` | Disabled | Muted gray | Turned off |

### Agent Health (aggregate per client)
| Value | Label | Badge Color |
|-------|-------|-------------|
| `healthy` | Healthy | Sage green |
| `mixed` | Mixed | Coral |
| `degraded` | Degraded | Red |
| `setup` | Setup | Neutral gray |

---

## CONNECTORS / INTEGRATIONS

### Connector Categories & Options
| Category | Connectors | Description |
|----------|------------|-------------|
| **Accounting** | QuickBooks Online, Xero, FreshBooks, Wave, Sage | Core financial data |
| **Banking** | Plaid, Mercury, Chase, Stripe, Brex | Bank feeds & transactions |
| **Payroll / HR** | Gusto, ADP, Rippling, Justworks | Payroll data sync |
| **Communication** | Slack, Microsoft Teams, Email (SMTP) | Notifications & alerts |
| **Documents** | Notion, Google Workspace, Dropbox | Document storage & collaboration |
| **CRM** | Salesforce, HubSpot, Pipedrive | Revenue & pipeline data |
| **Payments** | Stripe, Square, PayPal, Bill.com | Payment processing |
| **Data / API** | Merge (universal), Zapier, Custom Webhook | Universal connectors |

### Connector Status
| Value | Label | Badge Color | Description |
|-------|-------|-------------|-------------|
| `connected` | Connected | Sage green | Active and syncing |
| `syncing` | Syncing | Neutral gray | Currently syncing data |
| `awaiting_setup` | Awaiting Setup | Coral | Needs credentials/config |
| `disconnected` | Disconnected | Red | Lost connection |
| `error` | Error | Red | Sync failed |
| `paused` | Paused | Neutral gray | Manually paused |

### Connector Config Fields
| Field | Type | Notes |
|-------|------|-------|
| Connector Type | dropdown | From categories above |
| API Key / OAuth | credential | Stored securely |
| Sync Frequency | dropdown | Real-time, Hourly, Daily, Weekly |
| Last Sync | timestamp | Auto-populated |
| Records Synced | number | Count of synced records |
| Sync Direction | dropdown | One-way (import), One-way (export), Bi-directional |

---

## APPROVALS

### Approval Types
| Value | Label | Description |
|-------|-------|-------------|
| `expense` | Expense Approval | Review flagged expense |
| `invoice_payment` | Invoice Payment | Approve invoice for payment |
| `budget_change` | Budget Change | Approve budget modification |
| `agent_action` | Agent Action | Approve AI-recommended action |
| `report_review` | Report Review | Review generated report |
| `vendor_add` | New Vendor | Approve new vendor addition |
| `transfer` | Fund Transfer | Approve fund movement |

### Approval Status
| Value | Label | Badge Color |
|-------|-------|-------------|
| `pending` | Pending | Coral |
| `approved` | Approved | Sage green |
| `rejected` | Rejected | Red |
| `expired` | Expired | Muted gray |
| `escalated` | Escalated | Coral |

### Approval Table Columns
| Column | Type | Format |
|--------|------|--------|
| Type | badge | Approval type pill |
| Description | text | What needs approval |
| Client | text | Which client workspace |
| Amount | currency | Dollar amount if applicable |
| Requested By | text | Agent name or user |
| Date | relative time | "2h ago", "1d ago" |
| Status | badge | Approval status pill |
| Priority | badge | `low`, `medium`, `high`, `urgent` |

### Priority Dropdown
| Value | Label | Badge Color |
|-------|-------|-------------|
| `low` | Low | Muted gray |
| `medium` | Medium | Neutral |
| `high` | High | Coral |
| `urgent` | Urgent | Red |

---

## DASHBOARD METRICS (Mission Control Stat Cards)
| Metric | Type | Format | Indicator Logic |
|--------|------|--------|-----------------|
| Active Clients | integer | "3" | Green dot if all operational |
| Open Approvals | integer | "5" | Coral dot if > 0, green if 0 |
| Agent Health | percentage | "87%" | Green if > 80%, coral if 50-80%, red if < 50% |
| Sync Coverage | percentage | "67%" | Green if 100%, coral if < 100% |

---

## CLIENT WORKSPACE VIEW (tabs when inside a client)

### Workspace Tabs
| Tab | Description |
|-----|-------------|
| **Overview** | Client summary, key metrics, recent activity |
| **Connections** | Manage connectors for this client |
| **Agents** | View/configure deployed agents |
| **Approvals** | Pending approvals for this client |
| **Reports** | Generated financial reports |
| **Settings** | Client-specific configuration |
| **Activity Log** | Audit trail of all actions |

### Client Overview Metrics
| Metric | Type | Format |
|--------|------|--------|
| Cash Position | currency | "$129,418.00" |
| Monthly Burn | currency | "$23,400/mo" |
| Runway | text | "5.5 months" |
| Active Agents | count | "4 of 6" |
| Open Approvals | count | "5 pending" |
| Last Sync | relative time | "23h ago" |

---

## PAGE MAP

| # | Page | Description |
|---|------|-------------|
| 1 | Login | Email/password + SSO |
| 2 | Mission Control | Admin dashboard overview |
| 3 | Agent Templates | Manage base agent templates |
| 4 | Settings | Platform settings |
| 5 | Client Workspace - Overview | Client summary |
| 6 | Client Workspace - Connections | Manage integrations |
| 7 | Client Workspace - Agents | Deployed agents |
| 8 | Client Workspace - Approvals | Approval queue |
| 9 | Client Workspace - Reports | Financial reports |
| 10 | Client Workspace - Settings | Client config |
| 11 | Add Client Modal | Create new client overlay |
| 12 | Deploy Agent Modal | Deploy agent to client overlay |
| 13 | Approval Detail | Single approval review |
