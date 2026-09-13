# Automation & System Integration Checklist

**Version:** 1.0  
**Maintainer:** [Touchstone Infotech](https://www.touchstoneinfotech.com/)  
**Implementation support:** [Sales Automation](https://www.touchstoneinfotech.com/technology/sales-automation/)

This framework contains **100 checks** across 20 areas. Mark non-applicable items as N/A rather than forcing every system into the same architecture.

---

## 1. Business Process Discovery
- [ ] The current manual process is documented before automation begins.
- [ ] The desired business outcome is defined in measurable terms.
- [ ] Process owners and operational stakeholders are identified.
- [ ] Known exceptions and edge cases are documented.
- [ ] Steps that require human judgment are separated from deterministic automation.

## 2. System Inventory
- [ ] Every application involved in the workflow is listed.
- [ ] Each system's business purpose and owner are documented.
- [ ] Existing integrations and dependencies are mapped.
- [ ] Duplicate tools performing the same function are identified.
- [ ] Vendor/API limitations relevant to the workflow are documented.

## 3. Data Ownership & Source of Truth
- [ ] A system of record is defined for each critical data object.
- [ ] Field ownership is documented for shared data.
- [ ] Unique identifiers exist for important entities such as contacts and transactions.
- [ ] Data synchronization direction is intentionally defined.
- [ ] Conflict-resolution rules exist when multiple systems can update the same record.

## 4. CRM Architecture
- [ ] Contact, company, opportunity and activity models match the sales process.
- [ ] Required CRM fields are standardized and documented.
- [ ] Pipeline stages have clear entry and exit criteria.
- [ ] Duplicate-contact handling rules are implemented.
- [ ] CRM permissions reflect actual user responsibilities.

## 5. API Readiness
- [ ] Official APIs are preferred over fragile browser-based workarounds when practical.
- [ ] Required endpoints and methods are confirmed before development.
- [ ] API rate limits and quotas are documented.
- [ ] Pagination and result limits are handled correctly.
- [ ] API versioning and deprecation risks are monitored.

## 6. Authentication & Secrets
- [ ] API credentials are never hard-coded in public source code.
- [ ] Secrets are stored in an appropriate secrets manager or protected environment.
- [ ] OAuth scopes or API permissions follow least-privilege principles.
- [ ] Credential rotation and revocation procedures are documented.
- [ ] Production and test credentials are separated.

## 7. Webhooks
- [ ] Webhook endpoints authenticate or verify incoming events where supported.
- [ ] Duplicate webhook deliveries can be processed safely.
- [ ] Event ordering assumptions are avoided or explicitly handled.
- [ ] Webhook failures have retry or recovery mechanisms.
- [ ] Payload schemas and relevant event versions are documented.

## 8. Lead Capture
- [ ] All intended lead sources are mapped into the destination system.
- [ ] Required lead fields are validated before processing.
- [ ] Source, campaign and attribution data are retained where available.
- [ ] Duplicate submissions are handled predictably.
- [ ] Consent and communication preferences are captured where required.

## 9. Lead Routing
- [ ] Routing rules reflect territory, product, language or other business requirements.
- [ ] Assignment occurs within a defined service-level target.
- [ ] Unassigned leads enter an exception queue rather than disappearing.
- [ ] Reassignment rules exist for unavailable or inactive owners.
- [ ] Routing outcomes are logged for later auditing.

## 10. Messaging Automation
- [ ] WhatsApp, email and SMS automations use the correct consent model.
- [ ] Message templates reflect the recipient's actual stage and context.
- [ ] Frequency limits prevent excessive automated communication.
- [ ] Replies can route to a human when needed.
- [ ] Opt-outs and channel preferences synchronize across relevant systems.

## 11. Appointment Automation
- [ ] Calendar availability reflects actual working hours and capacity.
- [ ] Time zones are handled explicitly.
- [ ] Confirmation and reminder messages contain accurate appointment information.
- [ ] Rescheduling and cancellation paths update connected systems.
- [ ] No-show outcomes can trigger an appropriate follow-up workflow.

## 12. Sales Pipeline Automation
- [ ] Opportunity creation rules prevent unnecessary duplicates.
- [ ] Stage changes trigger only relevant downstream actions.
- [ ] Closed-won and closed-lost states stop incompatible nurture sequences.
- [ ] Stale opportunities can be surfaced for review.
- [ ] Important pipeline changes retain an audit trail.

## 13. Payments & Billing Flows
- [ ] Payment success is verified from a trusted provider event rather than a browser redirect alone.
- [ ] Failed, pending and refunded payments are handled separately.
- [ ] Transaction identifiers are stored for reconciliation.
- [ ] Duplicate payment events are processed idempotently.
- [ ] Payment data handling avoids storing sensitive card information unnecessarily.

## 14. AI-Assisted Automation
- [ ] AI is used only where its probabilistic behavior is acceptable for the task.
- [ ] High-impact AI decisions have appropriate human review or safeguards.
- [ ] Prompts and system instructions are versioned for important workflows.
- [ ] Sensitive data exposure to AI providers is reviewed before deployment.
- [ ] AI output failures, hallucinations or low-confidence cases have fallback paths.

## 15. Error Handling
- [ ] Each critical integration defines expected failure modes.
- [ ] Transient failures use bounded retries with appropriate delays.
- [ ] Permanent failures are moved to an actionable exception path.
- [ ] Failed records can be replayed without creating duplicate side effects.
- [ ] User-facing workflows fail gracefully when dependencies are unavailable.

## 16. Observability & Logging
- [ ] Critical workflow executions produce searchable logs.
- [ ] Logs include correlation or transaction identifiers where useful.
- [ ] Success and failure rates can be measured for important automations.
- [ ] Alerts exist for material integration failures.
- [ ] Logs avoid unnecessarily exposing passwords, tokens or sensitive personal data.

## 17. Security & Access Control
- [ ] Integration accounts use only the permissions they need.
- [ ] Former staff and unused service accounts are removed promptly.
- [ ] Administrative actions are restricted and auditable.
- [ ] Sensitive data is encrypted in transit and appropriately protected at rest.
- [ ] Third-party integrations are periodically reviewed for continued necessity and risk.

## 18. Testing & QA
- [ ] A test environment or safe test strategy exists for critical integrations.
- [ ] Happy-path workflows are tested end to end.
- [ ] Missing fields, duplicates and malformed data are tested.
- [ ] Timeout, API failure and retry scenarios are tested.
- [ ] Production launch includes defined acceptance criteria and rollback planning.

## 19. Change Management
- [ ] Workflow changes have an identifiable owner.
- [ ] Material changes are documented before or during deployment.
- [ ] API, CRM-field and schema changes are assessed for downstream impact.
- [ ] Users are informed when automation changes alter their operational process.
- [ ] Old workflow versions and unused automations are retired safely.

## 20. Reliability & Governance
- [ ] Critical workflows have a documented business continuity fallback.
- [ ] Automation health is reviewed on a recurring schedule.
- [ ] Ownership is clear when a workflow fails outside business hours.
- [ ] Key integrations have measurable reliability or processing targets.
- [ ] Automation is periodically reviewed to confirm it still serves the intended business outcome.

---

## Audit Summary

| Area | Score | Priority | Key Finding | Owner |
|---|---:|---|---|---|
| Process & architecture |  |  |  |  |
| CRM & data |  |  |  |  |
| APIs & webhooks |  |  |  |  |
| Automation |  |  |  |  |
| Security & reliability |  |  |  |  |

## Priority model

**Critical:** security exposure, data loss, broken revenue flow or business-critical integration failure.  
**High:** substantial operational/reliability issue or major manual dependency.  
**Medium:** meaningful efficiency, quality or maintainability opportunity.  
**Low:** incremental cleanup and optimization.

## Need implementation support?

**[Explore Sales Automation & System Integration from Touchstone Infotech](https://www.touchstoneinfotech.com/technology/sales-automation/)**
