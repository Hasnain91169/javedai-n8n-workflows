# JavedAI n8n Workflows

Twelve reference n8n workflows for lead capture, prospecting, email outreach, AI voice calls, CRM updates, reporting, and error handling. These are reusable portfolio templates, not a connected production deployment.

## Workflows

| File | Purpose |
| --- | --- |
| [`01_voiceflow_speed_to_lead_webhook.json`](01_voiceflow_speed_to_lead_webhook.json) | Validate a Voiceflow lead and create or update a HubSpot contact. |
| [`02_company_discovery.json`](02_company_discovery.json) | Discover and rank target companies. |
| [`03_decision_maker_discovery.json`](03_decision_maker_discovery.json) | Find and rank decision makers. |
| [`04_email_find_and_verify.json`](04_email_find_and_verify.json) | Find and verify work email addresses. |
| [`05_personalisation_and_approval.json`](05_personalisation_and_approval.json) | Draft personalised outreach for approval. |
| [`06_instantly_enrolment.json`](06_instantly_enrolment.json) | Enrol approved leads in Instantly. |
| [`07_instantly_events.json`](07_instantly_events.json) | Process Instantly events and update CRM status. |
| [`10_vapi_outbound_orchestrator.json`](10_vapi_outbound_orchestrator.json) | Orchestrate outbound Vapi calls. |
| [`11_vapi_inbound_events.json`](11_vapi_inbound_events.json) | Receive Vapi inbound server events. |
| [`12_call_analysis_and_crm_sync.json`](12_call_analysis_and_crm_sync.json) | Analyse calls and sync results to the CRM. |
| [`90_weekly_kpi_report.json`](90_weekly_kpi_report.json) | Build a weekly KPI report. |
| [`99_error_handler.json`](99_error_handler.json) | Handle workflow errors centrally. |

## Import and configure

1. Import the JSON files into n8n. They are exported as **inactive** workflows.
2. Read the setup sticky note in each workflow. Configure its required environment variables, credentials, webhook security, and service accounts in your own n8n instance. Credentials are not included in these files.
3. After importing all workflows, select **JavedAI 99 - Central Error Handler** in the settings of workflows that use it. The exports do not embed a static error-workflow ID.
4. Review any dry-run settings and every node that calls an external service. Test with sample data before activating a workflow or allowing it to send messages, place calls, or update records.

The workflows use services including Voiceflow, Google Places, Apollo, Anymail Finder, NeverBounce, Instantly, Vapi, and HubSpot. Each workflow's notes describe its specific requirements.
