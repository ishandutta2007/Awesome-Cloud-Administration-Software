# Awesome-Cloud-Administration-Software

# Awesome-Cloud-Administration-Software
**Top Cloud Administration Software (Opensource) 🌟 Star if you like it! 🌟**

**Curated List of SaaS Products & Open-Source GitHub Projects**
*Focused on SaaS Management Platforms, Identity & Access Management, Tenant Administration & Shadow IT Discovery*
**Last updated: October 2026**

This repository tracks notable **SaaS platforms** and **open-source projects** for **Cloud Administration Software**. These tools enable IT teams to discover and manage SaaS applications, govern user access, administer cloud tenants, and rationalize spend—from fully managed platforms with automated onboarding and license optimization to self-hosted dashboards and IAM servers that give organizations complete control over their cloud administration workflows.

**Examples** include BetterCloud, Torii, Zylo, Productiv, JumpCloud, Lumos, Rippling, Google Workspace Admin, Microsoft 365 Admin Center, and Atlassian Administration (the category leaders in commercial space).

**Open-source emphasis**: This section is expanded with every relevant project for self-hosted SaaS management, identity governance, and open administration infrastructure. **Critical note**: The open-source landscape for dedicated SaaS administration is nascent—**SaaS Security Posture & Rationalization Dashboard** is the only purpose-built open-source alternative to Torii/Zylo/Productiv for SaaS inventory and spend analysis . For identity and access management (the foundational layer of cloud administration), **Nubus**, **Hanzo IAM**, and **Idenplane** offer production-oriented self-hosted options. No open-source project matches BetterCloud's automated workflow depth or Lumos's app request/approval experience.

Contributions welcome! Open a PR to add/update entries. Keep descriptions factual and link to official sites.

## Table of Contents
- [SaaS/Hosted Platforms](#saas-hosted-platforms)
- [Open-Source GitHub Projects](#open-source-github-projects)
- [How to Contribute](#how-to-contribute)
- [Disclaimer](#disclaimer)

## SaaS/Hosted Platforms

- **[BetterCloud](https://www.bettercloud.com/)**
  **SaaS management and operations platform** with automated workflows, onboarding/offboarding, and security policies across Google Workspace, Microsoft 365, and 100+ SaaS apps. **Pricing**: Quote-only; tiered by users and integrations. **Free tier**: None. **Best for**: IT teams wanting to automate SaaS administration workflows and enforce security policies across the SaaS stack.

- **[Torii](https://www.torii.com/)**
  **SaaS management platform** with discovery, license optimization, and automated workflows. **Pricing**: Quote-only; tiered by SaaS spend or user count. **Free tier**: None. **Best for**: organizations wanting to discover shadow IT, optimize SaaS spend, and automate onboarding/offboarding.

- **[Zylo](https://www.zylo.com/)**
  **SaaS management and optimization** platform with license utilization analytics and renewal management. **Pricing**: Quote-only. **Free tier**: None. **Best for**: finance and IT teams wanting to rationalize SaaS spend and avoid unused license renewals.

- **[Productiv](https://www.productiv.com/)**
  **SaaS engagement and spend analytics** platform with app usage insights and license optimization. **Pricing**: Quote-only. **Free tier**: None. **Best for**: organizations wanting to understand how SaaS applications are actually used to optimize spend.

- **[JumpCloud](https://jumpcloud.com/)**
  **Directory platform** for identity, access, and device management across cloud and on-premise resources. **Pricing**: Tiered per-user pricing; free tier for small teams. **Free tier**: Yes, up to 10 users. **Best for**: IT teams wanting a unified directory for identity and device management without Active Directory.

- **[Lumos](https://www.lumos.com/)**
  **SaaS management and app access platform** with automated app requests, approvals, and access reviews. **Pricing**: Quote-only. **Free tier**: None. **Best for**: IT teams wanting self-service app access with governance and automatic provisioning.

- **[Rippling](https://www.rippling.com/)**
  **Unified HR, IT, and finance platform** with SaaS app management, device management, and identity governance. **Pricing**: Quote-only; modular per-user pricing. **Free tier**: None. **Best for**: companies wanting HR and IT administration unified in one platform.

- **[Google Workspace Admin](https://admin.google.com/)**
  **Native administration console** for Google Workspace users, groups, devices, and security settings. **Pricing**: Included with Google Workspace subscriptions. **Free tier**: Limited on Workspace free tier. **Best for**: Google Workspace organizations managing users and policies natively.

- **[Microsoft 365 Admin Center](https://admin.microsoft.com/)**
  **Native administration console** for Microsoft 365 users, licenses, and services. **Pricing**: Included with Microsoft 365 subscriptions. **Free tier**: Limited on M365 free tier. **Best for**: Microsoft 365 organizations managing users and licenses natively.

- **[Atlassian Administration](https://admin.atlassian.com/)**
  **Native administration** for Atlassian Cloud products (Jira, Confluence, etc.) with user provisioning and security controls. **Pricing**: Included with Atlassian subscriptions. **Free tier**: Limited on Atlassian Free. **Best for**: Atlassian customers managing users and access across Atlassian products.

## Open-Source GitHub Projects

- **[SaaS Security Posture & Rationalization Dashboard](https://github.com/CyberEnthusiastic/saas-security-posture)**
  **Self-hosted SaaS inventory analysis and cost optimization** (MIT, ~v1.0) — **the only purpose-built open-source alternative to Torii, Zylo, and Productiv** found in this research . **Features**: **SaaS inventory ingestion** and analysis; **shadow IT detection**—identifies unapproved tools with no SSO, DLP, or data sovereignty controls; **redundancy analysis**—flags duplicate subscriptions across categories (e.g., Asana + Monday + Trello); **OAuth risk scoring**—flags excessive permissions across connected integrations; **cost optimization**—calculates exact savings from consolidation; **HTML dashboard** with dark mode and filtering; **zero runtime dependencies**—pure Python stdlib, no database, no cloud platform . **Demo results**: 29 tools analyzed, $1.24M annual spend, $277K (22.4%) potential savings, 11 shadow IT tools, 11 redundant tools, 118 security findings . **Tech stack**: Python (pure stdlib), HTML report generation. **Deploy**: `git clone && python analyzer.py` (Linux/macOS/WSL) or `.\install.ps1` (Windows). **Trade-off**: **Analysis tool, not a live administration platform**—it ingests a static SaaS inventory and produces a report; it does not connect to SaaS APIs for real-time discovery, automate onboarding/offboarding, or provision users. **Best for**: IT and finance teams wanting a free, self-hosted way to audit SaaS sprawl, detect shadow IT, and quantify consolidation savings—without a SaaS subscription.

- **[Nubus](https://github.com/univention/nubus)**
  **Modular open-source identity and access management (IAM)** (AGPL-3.0-or-later) — **the most mature open-source IAM option for organizations**, used by Orange S.A., German state education ministries, and ZenDiS GmbH . **Features**: **Central web portal** for user management and access control; **Single Sign-On (SSO)** for integrated application access; **self-service** for password changes and profile updates; **user lifecycle management**—connects to existing identity sources; **prebuilt integrations** for common open-source systems; **open standards and APIs**; Kubernetes, on-premises, and hybrid deployment; designed for data protection-sensitive environments . **Tech stack**: Per repository (Univention ecosystem). **Deploy**: Self-hosted (Kubernetes, on-premises, hybrid). **Trade-off**: **IAM foundation, not SaaS administration**—it governs identity and access to applications, but does not discover shadow SaaS, optimize licenses, or automate SaaS onboarding workflows. **Best for**: organizations needing a self-hosted, open-standards IAM portal with SSO and user lifecycle management—especially public sector and European organizations with data sovereignty requirements.

- **[Hanzo IAM](https://github.com/hanzoai/iam)**
  **AI-first identity and access management server** (Apache-2.0) — **the most protocol-rich open-source IAM server**, with broad enterprise federation support . **Features**: **OAuth 2.0 / OIDC provider**; **SAML / CAS / LDAP** federation; **WebAuthn / Passkeys** (FIDO2); **TOTP / MFA**; **40+ social login providers**; **RBAC** with fine-grained permissions; **multi-tenancy**; **SCIM provisioning** for automated user lifecycle; **RADIUS**; full REST API; web UI . **Tech stack**: Go. **Deploy**: Docker (`docker run -d -p 8000:8000 hanzoai/iam:latest`) . **Trade-off**: **IAM server, not SaaS management**—it authenticates and authorizes users across applications, but does not inventory SaaS apps or manage spend. **Best for**: organizations wanting a modern, protocol-complete self-hosted IAM server with AI/MCP gateway capabilities and broad federation support.

- **[Idenplane](https://github.com/idenplane/idenplane)**
  **Lightweight self-hosted IAM server** (license per repo) — **the most resource-efficient open-source IAM option**, designed as a Keycloak/Auth0 alternative that runs in ~150 MB RAM (vs. Keycloak's 1 GB+) . **Features**: **OAuth 2.0 / OIDC / SAML 2.0 / WebAuthn / TOTP / SCIM**; **multi-tenancy via realms**; **RBAC + ABAC**; **LDAP federation**; **external IdP brokering**; **adaptive auth**—risk-based step-up, impossible-travel detection, IP reputation, device fingerprinting; **stateless with horizontal scaling**; Prometheus metrics; **10 client SDKs** (TypeScript, React, Next.js, Angular, Vue, Android, iOS, CLI, Python, Go, Java); **migration importers** for Auth0 and Keycloak . **Tech stack**: TypeScript (NestJS), PostgreSQL/MySQL/SQLite. **Deploy**: Docker Compose; stateless horizontal scaling (`docker compose up -d --scale app=3`) . **Trade-off**: **IAM server, not SaaS administration**—no SaaS discovery, license optimization, or workflow automation. **Best for**: teams wanting a lightweight, modern IAM server with adaptive authentication and easy migration from Keycloak/Auth0—without the resource overhead of Keycloak.

### Additional Strong Open-Source Options

- **Qisutu** — Open-source ticket system with OAuth2/XOAUTH2 for Microsoft 365 and Google Workspace, LDAP/AD authentication, CMDB, and REST API (AGPL-3.0) . **Note**: **Helpdesk/ITSM**, not SaaS administration—it handles tickets and service management, not SaaS inventory or license optimization. **Best for**: IT teams needing self-hosted ticketing with Microsoft 365/Google Workspace integration.
- **OpenFrame** — Open-source MSP platform with deep Microsoft 365 and Google Workspace tenant management, remote access, and patching (v1.5.0) . **Note**: **MSP-focused RMM/ITSM**, not general SaaS administration—it manages tenants and endpoints for managed service providers. **Best for**: MSPs wanting an open-source alternative to commercial RMM platforms.
- **osTicket** — Widely-used open-source support ticket system (GPL) . **Note**: **Helpdesk only**—no SaaS discovery, license management, or cloud administration features. **Best for**: organizations needing basic self-hosted ticketing, not cloud administration.

**Frameworks for building custom systems**: Combine **SaaS Security Posture & Rationalization Dashboard** for SaaS inventory analysis with **Nubus** or **Idenplane** for identity and access governance, and **Qisutu** or **OpenFrame** for IT service management—creating a cloud administration stack. **None of these match BetterCloud's automated SaaS workflows or Lumos's app request/approval experience**; those require commercial platforms or significant custom development.

## How to Contribute

1. Fork the repo.
2. Add/edit entries in `README.md` (follow existing format).
3. Include: name, link, 1–2 sentence description, license (for open-source), and whether it's SaaS or open-source.
4. Submit PR with a short explanation.

Star the repo if you find it useful!

## Disclaimer

- This is a **community-curated** list — not exhaustive and not an endorsement.
- Cloud administration platforms handling user identities and SaaS inventory must comply with data protection regulations (GDPR, CCPA, etc.) and implement appropriate access controls for administrative credentials.
- **The "SaaS management platform" vs. "IAM server" vs. "ITSM/helpdesk" distinction is critical.** **BetterCloud, Torii, Zylo, Productiv, and Lumos** are **SaaS management platforms**—they discover SaaS apps, optimize licenses, and automate administration workflows. **JumpCloud, Rippling, Nubus, Hanzo IAM, and Idenplane** are **IAM/directory platforms**—they govern identity and access, not SaaS inventory or spend. **Google Workspace Admin, Microsoft 365 Admin Center, and Atlassian Administration** are **native tenant consoles**—they administer their own platforms, not cross-SaaS. **Qisutu and osTicket** are **ITSM/helpdesk**—ticketing, not SaaS administration. **SaaS Security Posture & Rationalization Dashboard** is the **only open-source SaaS management analysis tool**—but it is static analysis, not live administration . **Choose based on whether you need SaaS inventory, identity governance, tenant administration, or service management.**
- **SaaS Security Posture & Rationalization Dashboard is the only open-source answer to Torii/Zylo/Productiv**—it detects shadow IT, flags redundancy, scores OAuth risk, and quantifies savings . **The trade-off**: it is an analysis tool, not a live platform. It ingests a static inventory and produces a report; it does not connect to SaaS APIs for real-time discovery, automate onboarding/offboarding, or provision users. **For teams wanting a free SaaS audit without a subscription, it is the pragmatic starting point.**
- **Nubus is the most production-proven open-source IAM option**, used by Orange S.A. and German state ministries, with SSO, self-service, and user lifecycle management . **Idenplane is the lightweight Keycloak alternative**—150 MB RAM vs. 1 GB+, with adaptive auth and built-in Auth0/Keycloak migration . **Hanzo IAM is the protocol-rich option** with 40+ social logins and SCIM provisioning . **Choose based on your priority: proven European adoption (Nubus), resource efficiency and migration (Idenplane), or protocol breadth (Hanzo).**
- **No open-source project matches BetterCloud's automated workflows or Lumos's app request/approval experience.** Those platforms provide self-service app access, automated provisioning/deprovisioning, and policy enforcement across SaaS apps—capabilities that require deep integrations with each SaaS app's API and a workflow engine. **Open-source IAM provides the identity foundation but not the SaaS-specific automation layer.**
- **Pricing opacity is universal across commercial vendors.** BetterCloud, Torii, Zylo, Productiv, JumpCloud (enterprise), Lumos, and Rippling require sales contact or quote-based estimation. Google Workspace Admin and Microsoft 365 Admin Center are included with subscriptions. **Validate with direct vendor conversations against your SaaS app count and administration workflow requirements.**
- Self-hosted open-source solutions require proper infrastructure, security hardening for administrative credentials, and ongoing maintenance. **Cloud administration data includes user identities and SaaS inventory**—ensure your deployment meets your organization's security and privacy requirements before connecting production systems.

---

**Made for IT administrators, security teams, and organizations building transparent cloud administration solutions.**
Let's make Cloud Administration Software more open, data-driven, and SaaS-aware.
