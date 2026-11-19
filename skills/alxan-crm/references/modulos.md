# Módulos do Alxan CRM

Cada conta tem só os módulos do plano dela. Módulo desligado = ferramentas invisíveis no MCP.
Para achar as ferramentas de um módulo, use `search_tools` com uma palavra da etiqueta (em inglês).


## Automation & AI (17)
- `agent_bots` · Agent Bots (ligado por padrão): Programmable agent bots on inboxes. · ajuda: https://crm.alxan.com.br/hc/ajuda/articles/automation-flows-bots-e-captain-pt-br
- `automations` · Automations (ligado por padrão): Event-driven automation rules.
- `custom_tools` · Custom Tools: Custom IA nativa tools.
- `advanced_assignment` · Advanced Assignment: Advanced auto-assignment selector.
- `flow_builder` · Flow Builder: Visual node-graph flow builder with a resumable engine.
- `account_brain` · Account Brain: Maestro Account Brain: knowledge ingestion and account grounding.
- `smart_routing` · Smart Routing: Round-robin / balanced / skill-based conversation routing. · combina com: granular_permissions
- `mcp` · MCP (Model Context Protocol): Native MCP: expose the account (and Maestro departments) as tools to external AI clients; curated toolsets, read-only mode and per-account tokens.
- `setup_blueprints` · Setup Blueprints: SetupBlueprint engine: vertical templates, generative blueprints and the platform one-call setup payload. · combina com: account_brain
- `maestro_byok` · Maestro BYOK (Account LLM Keys) (ligado por padrão): Account-level LLM provider keys (BYOK) mirrored to the Maestro sidecar; off forces the installation-global keys.
- `flow_builder_runtime_v2` · Flow Builder Runtime V2: Compile newly published flows into the immutable Flow Builder runtime v2 contract. · exige: flow_builder
- `maestro_global_keys` · Maestro Installation LLM Keys (Global Fallback): Lets the account fall back to the installation's own LLM keys. Off: the default for a new signup: means the account spends only on the keys it brought. · combina com: maestro_byok
- `delayed_automations` · Delayed Automations: Automation rules whose actions run after a configured delay.

## Channels & Inboxes (27)
- `inbound_emails` · Inbound Emails (ligado por padrão): Process inbound email as conversations.
- `channel_email` · Email Channel (ligado por padrão): Connect an email address as a support inbox. · ajuda: https://crm.alxan.com.br/hc/ajuda/articles/inboxes-channels-canal-email-pt-br
- `channel_facebook` · Facebook Channel (ligado por padrão): Facebook Messenger as an inbox. · ajuda: https://crm.alxan.com.br/hc/ajuda/articles/inboxes-channels-canais-sociais-pt-br
- `email_continuity_on_api_channel` · Email Continuity on API Channel: Keep email threading continuity on the API channel.
- `channel_website` · Website Channel (ligado por padrão): Embeddable live-chat widget for websites.
- `custom_reply_email` · Custom Reply Email: Send replies from a custom reply-to email address.
- `custom_reply_domain` · Custom Reply Domain: Send replies from a custom reply domain.
- `branded_email_templates` · Branded Email Templates: Branded templates for the transactional emails sent to customers.
- `channel_instagram` · Instagram Channel (ligado por padrão): Instagram Direct as an inbox.
- `channel_voice` · Voice Channel: Twilio Voice inbox channel (Enterprise). WhatsApp calling now rides the Inbox Suite.
- `channel_tiktok` · TikTok Channel (ligado por padrão): TikTok messaging as an inbox.
- `whatsapp_hub` · WhatsApp Hub: Manage WhatsApp groups, communities, channels and status.
- `whatsapp_inbox_suite` · WhatsApp Inbox Suite: In-inbox WhatsApp templates, Meta Flows and AI realtime calls.
- `whatsapp_hybrid_inbox` · WhatsApp Hybrid Inbox: Pair a Coexistence (Cloud) and a WhatsApp Web inbox on one number.
- `whatsapp_hybrid_unified_inbox` · WhatsApp Hybrid Unified Inbox: Single operational inbox for a Cloud-authoritative pair: opt-in per pair and reversible; history stays in its original inbox. · exige: whatsapp_hybrid_inbox
- `whatsapp_web_proxy` · WhatsApp Web Global Proxy: Assign installation-managed proxies to WhatsApp Web inboxes with regional routing and automatic failover.
- `whatsapp_mobile_egress` · WhatsApp Web Mobile Connection: Route a WhatsApp Web inbox through an account-owned phone with explicit fail-closed fallback.
- `whatsapp_manual_transfer` · WhatsApp Manual Transfer: Manually transfer a WhatsApp Cloud phone number to this installation.
- `whatsapp_reconfigure` · WhatsApp Reconfigure: Reconfigure the credentials of an existing WhatsApp Cloud inbox.
- `whatsapp_embedded_signup_inbox_creation` · WhatsApp Embedded Signup Flow: Create WhatsApp Cloud inboxes through the Meta embedded signup flow.
- `native_twilio_voice` · Twilio Voice: Native Twilio voice calls. Independent of WhatsApp Inbox Suite. · ajuda: https://crm.alxan.com.br/hc/ajuda/articles/inboxes-channels-canal-voz-pt-br
- `whatsapp_hybrid_weighted_routing` · WhatsApp Hybrid Weighted Routing: Deterministic per-contact Web/Cloud percentage for human replies on an active unified pair; opt-in per pair. · exige: whatsapp_hybrid_inbox, whatsapp_hybrid_unified_inbox · ajuda: https://crm.alxan.com.br/hc/ajuda/articles/inboxes-channels-whatsapp-outbound-optimization-pt-br
- `whatsapp_outbound_batching` · WhatsApp Outbound Batching: Consolidate an agent's confirmed WhatsApp text fragments into one reply before sending, with durable per-conversation order. · ajuda: https://crm.alxan.com.br/hc/ajuda/articles/inboxes-channels-whatsapp-outbound-optimization-pt-br
- `whatsapp_outbound_maestro` · WhatsApp Outbound Maestro Review: Let an allowlisted Maestro profile suggest or automatically apply authorized edits to the consolidated reply; never sends. · exige: whatsapp_outbound_batching · ajuda: https://crm.alxan.com.br/hc/ajuda/articles/inboxes-channels-whatsapp-outbound-optimization-pt-br
- `whatsapp_outbound_rich_transform` · WhatsApp Outbound Rich Transform: Convert a consolidated reply into allowlisted formats (buttons, list, CTA, published WhatsApp Flow). · exige: whatsapp_outbound_maestro · ajuda: https://crm.alxan.com.br/hc/ajuda/articles/inboxes-channels-whatsapp-outbound-optimization-pt-br
- `whatsapp_direct_send` · WhatsApp Direct Send: Direct WhatsApp utility and authentication messaging, subject to Meta eligibility and Cloud inbox category opt-in. · ajuda: https://crm.alxan.com.br/hc/ajuda/articles/inboxes-channels-whatsapp-direct-send-pt-br

## Contacts, CRM & Catalog (8)
- `ip_lookup` · IP Lookup: Enrich contacts with IP-based geolocation.
- `custom_attributes` · Custom Attributes (ligado por padrão): Custom attributes on contacts and conversations. · ajuda: https://crm.alxan.com.br/hc/ajuda/articles/contacts-crm-atributos-personalizados-pt-br
- `crm` · CRM (ligado por padrão): Core CRM records and contact management.
- `companies` · Companies: Group contacts under companies.
- `crm_pipelines` · CRM Pipelines (ligado por padrão): Deal pipelines and kanban stages. · combina com: crm
- `catalog` · Product Catalog (ligado por padrão): Native product and service catalog.
- `organizations` · Organizations (Companies & Relationships): First-class companies with roles, relationships and fiscal identity. · combina com: crm
- `data_import` · Data Import: Import contacts and conversations from Intercom, Freshdesk and CSV files.

## Contracts (1)
- `contracts` · Contracts & E-signature: Contract templates, e-signature tiers and signed-PDF audit trail.

## Conversations & Productivity (17)
- `conversation_glance_signals` · Conversation Glance Signals: At-a-glance signals surfaced on conversations.
- `macros` · Macros (ligado por padrão): One-click multi-step conversation actions.
- `labels` · Labels (ligado por padrão): Tag and organize conversations with labels. · ajuda: https://crm.alxan.com.br/hc/ajuda/articles/administration-horarios-labels-atributos-pt-br
- `canned_responses` · Canned Responses (ligado por padrão): Reusable saved replies for agents. · ajuda: https://crm.alxan.com.br/hc/ajuda/articles/conversations-respostas-rapidas-pt-br
- `voice_recorder` · Voice Recorder (ligado por padrão): Record voice notes directly in the composer.
- `auto_resolve_conversations` · Auto Resolve Conversations (ligado por padrão): Auto-resolve stale conversations after a period.
- `assignment_v2` · Assignment V2 (ligado por padrão): Improved conversation assignment engine.
- `advanced_search` · Advanced Search: EE OpenSearch full-text search (Enterprise).
- `conversation_required_attributes` · Required Conversation Attributes: Require conversation attributes before resolving.
- `tasks` · Tasks: Native Tasks module (Asana-style) for agents.
- `calendar` · Calendar: Native agenda with Google Calendar sync and public booking.
- `internal_chat` · Internal Chat: Internal team chat: channels, directs and announcements.
- `media_library` · Media Library (ligado por padrão): Account-global reusable media store, re-sent without re-uploading.
- `native_advanced_search` · Advanced Search (Native): Native ranked full-text search with date, sender and inbox filters.
- `outbound_agent_name_header` · Outbound Agent Name Header: Prefix outbound messages with the sender's display name in bold while preserving personal signatures.
- `realtime_translation` · Realtime Translation: Per-inbox and per-conversation automatic translation with an individual viewer language for each agent. · combina com: integrations
- `message_scheduling` · Message Scheduling: Create, review and safely deliver one-time, sequenced or recurring native scheduled messages.

## Governance & Security (9)
- `audit_logs` · Audit Logs: Account audit log trail.
- `custom_roles` · Custom Roles: Custom agent roles.
- `saml` · SAML: SAML single sign-on.
- `granular_permissions` · Granular Permissions (ligado por padrão): Native deep RBAC: permission matrix with team / inbox scope.
- `field_level_permissions` · Field-level Permissions (ligado por padrão): Per-field PII masking on top of the RBAC matrix. · combina com: granular_permissions
- `platform_governance` · Platform Governance (ligado por padrão): Super-admin role templates and entitlements. · combina com: granular_permissions
- `governance_lgpd` · Governance & LGPD: Governance & LGPD hub: presentation mode (PII blur), consent registry, data-subject requests (export/erasure), retention and DPO data. · combina com: granular_permissions
- `native_audit_trail` · Audit Trail (Native): Native account audit trail (CE-safe, dedicated table) consumed by the Governance hub.
- `native_event_pipeline_v2` · Native Event Pipeline V2: Structured, idempotent conversation activity projections backed by the canonical domain-event ledger. · combina com: native_audit_trail

## Growth & Marketing (15)
- `campaigns` · Campaigns (ligado por padrão): Outbound and ongoing campaigns. · ajuda: https://crm.alxan.com.br/hc/ajuda/articles/campaigns-overview-pt-br
- `whatsapp_campaign` · WhatsApp Campaign: WhatsApp broadcast campaigns.
- `follow_ups` · Follow-up: Re-engagement cadence sequences with reply-exit.
- `launch_group_distribution` · Launch Group Distribution: Capacity-aware auto-rotating WhatsApp group distribution for launches. · combina com: whatsapp_hub
- `growth_social` · Growth Social (Comment-to-DM): Comment-to-DM: auto-DM commenters and funnel them in. · combina com: follow_ups
- `growth_ads` · Growth Ads (CTWA & Lead Ads): Click-to-WhatsApp attribution and Meta lead-ad ingestion.
- `ads_conversion_tracking` · Ad Conversion Tracking (Meta CAPI): Send the funnel back to Meta Conversions API (needs ad capture). · exige: growth_ads
- `growth_social_automation` · Growth Social Automation (IG/TikTok/YouTube): IG / TikTok / YouTube monitoring and engagement automation.
- `social_collaboration` · Social Collaboration Network (Matrix): Collaborative organic-engagement affiliate network on the social engine. · exige: growth_social_automation
- `engagement_tracking` · Engagement & Lead Score: Engagement timeline and weighted lead score.
- `ads_manager` · Ads Manager: CTWA-first native ad manager over the Meta Marketing API. · combina com: growth_ads, ads_conversion_tracking
- `campaign_batched_dispatch` · Campaign Batched Dispatch: Dispatch WhatsApp Cloud campaigns through materialized recipients and parallel batch workers. · exige: whatsapp_campaign · ajuda: https://crm.alxan.com.br/hc/ajuda/articles/campaigns-whatsapp-campaign-results-pt-br
- `campaign_conversation_policy` · Campaign Conversation Policy: Per-campaign status, assignment and labels for the conversations a WhatsApp campaign creates. · exige: whatsapp_campaign · ajuda: https://crm.alxan.com.br/hc/ajuda/articles/campaigns-whatsapp-campaign-pt-br

## Help Center (1)
- `help_center` · Help Center (ligado por padrão): Public help center / knowledge base portal. · ajuda: https://crm.alxan.com.br/hc/ajuda/articles/getting-started-overview-pt-br

## Integrations (7)
- `integrations` · Integrations (ligado por padrão): Built-in integrations directory. · ajuda: https://crm.alxan.com.br/hc/ajuda/articles/administration-integracoes-pt-br
- `linear_integration` · Linear Integration: Linear issue integration.
- `shopify_integration` · Shopify Integration: Shopify connection, customer context and order actions. · exige: integrations · ajuda: https://crm.alxan.com.br/hc/ajuda/articles/administration-shopify-pt-br
- `crm_integration` · CRM Integration: External CRM integration.
- `notion_integration` · Notion Integration: Notion integration.
- `api_and_webhooks` · API and Webhooks (ligado por padrão): Account API access tokens and outgoing webhooks.

## Payments & Sales (8)
- `payments` · Payments: Multi-gateway payments (Asaas / Mercado Pago) with in-chat checkout.
- `sales_management` · Sales Management: Client portfolios, goals, gamification and a real-time wallboard. · combina com: granular_permissions, engagement_tracking
- `orders_registry` · CRM Orders Registry: Contact-centric purchase log across gateways (a log, not a gateway). · combina com: payments, catalog
- `unified_revenue_ledger` · Unified Revenue Ledger: Converges all revenue counting on the canonical order.paid axis (single credit per sale). · combina com: orders_registry, sales_management
- `affiliate_program` · Affiliate Program: Native affiliate entity with durable referral attribution and dual seller+affiliate commission. · combina com: unified_revenue_ledger, sales_management
- `commerce_recovery` · Commerce Recovery (Sales Recovery): Track abandoned purchases and coordinate recovery messages, outcomes and retries. · combina com: payments, catalog
- `payment_installment_plans` · Payment installment plans: Finite installment plans, capped recurrence and branded payment books. · combina com: payments · ajuda: https://crm.alxan.com.br/hc/ajuda/articles/payments-planos-de-cobranca-pt-br
- `sales_integrated_closing` · Integrated Sales Closing: Integrated sales closing with human authorization.

## Platform & Operation (15)
- `disable_branding` · Disable Branding (descontinuado): White-label: hide Alxan CRM / installation branding.
- `agent_management` · Agent Management (ligado por padrão): Manage agents and their access.
- `team_management` · Team Management (ligado por padrão): Manage teams and memberships. · ajuda: https://crm.alxan.com.br/hc/ajuda/articles/administration-conta-agentes-equipes-pt-br
- `inbox_management` · Inbox Management (ligado por padrão): Manage inbox settings and members.
- `guided_tours` · Guided Tours: Role-aware in-app onboarding tours with embedded videos. · ajuda: https://crm.alxan.com.br/hc/ajuda/articles/getting-started-tours-guiados-pt-br
- `workforce_management` · Team Management: Agent work / aux statuses, timers, adherence and monitoring.
- `bug_reports` · Bug Reports (ligado por padrão): In-app bug reporting with rich diagnostics to Linear.
- `white_label` · White Label: Hide Alxan CRM / installation branding on widget, portal and surveys (license-governed).
- `ai_onboarding` · AI Onboarding (Generative Setup): Generative onboarding: the SetupWizard and the account setup API (per-account override of the global onboarding mode). · combina com: setup_blueprints, guided_tours
- `usage_metering` · Usage Metering: Native monthly usage counters (messages, conversations, contacts, AI requests/tokens) with 80/100% threshold events.

## Reports & Quality (6)
- `report_rollup` · Report Rollup: Pre-aggregated report rollups.
- `reports` · Reports (ligado por padrão): Conversation, agent and account reports. · ajuda: https://crm.alxan.com.br/hc/ajuda/articles/reports-overview-pt-br
- `sla` · SLA: SLA policies and breach tracking. · ajuda: https://crm.alxan.com.br/hc/ajuda/articles/conversations-sla-pt-br
- `csat_review_notes` · CSAT Review Notes: Reviewer notes on CSAT responses.
- `session_analytics` · Session Analytics: Operator-controlled session-behavior analytics (Clarity / Amplitude).
- `whatsapp_cost_center` · WhatsApp cost center: Per-message WhatsApp Cloud cost ledger, usage by billing month and cost visibility inside conversations. · ajuda: https://crm.alxan.com.br/hc/ajuda/articles/reports-whatsapp-cost-center-pt-br

## Outros (12)
- `message_reply_to` · Message Reply To (descontinuado)
- `inbox_view` · Inbox View (interno)
- `help_center_embedding_search` · Help Center Embedding Search (interno)
- `search_with_gin` · Search messages with GIN (interno)
- `whatsapp_embedded_signup` · WhatsApp Embedded Signup (descontinuado)
- `crm_v2` · CRM V2 (interno)
- `advanced_search_indexing` · Advanced Search Indexing (interno)
- `reply_mailer_migration` · Reply Mailer Migration (interno)
- `unread_count_for_filters` · Unread Count For Filters (interno)

## Etiquetas de ferramentas no MCP (quantidade)

Access Roles (8), Account (5), Account AgentBots (1), Ads (45), Agent Capacity Policies (11), Agents (6), Assignable Agents (1), Assignment Policies (7), Audit Logs (1), Automation Rule (7), Branded Email Layout (1), Bug Reports (24), Bulk Actions (5), CRM (4), CRM Item Attachments (1), CRM Item Checklist (7), CRM Item Line Items (5), CRM Item Notes (6), CRM Item Participants (5), CRM Items (23), CRM Organizations (6), CRM Pipelines (10), CRM Reports (1), CRM Stages (9), CRM Templates (4), CSAT Survey Responses (3), Calendar (10), Calendar Availability (5), Calendar Connections (5), Calendar Event Types (3), Calendar Events (4), Calendar Reports (1), Calendar Settings (4), Calls (1), Campaign Suppressions (3), Campaigns (14), Canned Responses (5), IA nativa (64), Catalog (37), Catalog Categories (6), Catalog Products (7), Catalog Reports (1), Catalog Sync Runs (3), Catalog Sync Sources (7), Catalog Variants (3), Commerce (24), Companies (15), Contact Inboxes (1), Contact Labels (2), Contacts (28), Contracts (37), Conversation Assignments (2), Conversation Sidebar Layout (3), Conversations (55), Custom Attributes (6), Custom Filters (6), Custom Roles (6), Custom Scripts (8), Dashboard Apps (10), Data Imports (5), Engagement (17), Flow Builder (43), Follow-up (21), Governance (15), Growth Distribution (12), Growth Social (101), Guided Tours (1), Help Center (27), Inboxes (70), Integrations (23), Internal Chat (23), Labels (6), Limits (1), Live Reports (2), Macros (8), Maestro (82), Media Library (23), Message Schedules (9), Message Scheduling (3), Messages (4), Notifications (12), Onboarding (3), Organization Memberships (6), Organizations (13), Payment Charges (9), Payment Connections (9), Payment Demo (2), Payment Installment Plans (1), Payment Offers (12), Payment Plans (11), Payment Reports (1), Payment Subscriptions (4), Payments (18), Relationship Types (6), Relationships (5), Reports (14), Routing Policies (15), SAML (5), SLA Policies (8), Sales (113), Search (7), Setup (6), Summary Reports (1), Task Attachments (2), Task Checklist (7), Task Comments (5), Task Dependencies (3), Task Links (3), Task Lists (9), Task Reminders (3), Task SLA Policies (6), Task Templates (8), Task Watchers (3), Tasks (20), Team Management (50), Teams (10), Usage (1), Webhooks (4), WhatsApp (54), WhatsApp Calls (4), WhatsApp Hub (37), WhatsApp Web (69), WhatsApp Web Calls (16), Year In Review (1)
