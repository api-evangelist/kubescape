# Kubescape

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

Kubescape is an open-source (Apache 2.0) Kubernetes security platform and CNCF incubating project, originally contributed by ARMO. It provides risk analysis, security and compliance posture scanning, misconfiguration detection, image and runtime vulnerability scanning, and eBPF-based runtime threat detection across the IDE, CI/CD pipelines, and live clusters. The core Kubescape is a CLI and an in-cluster Operator whose components expose OpenAPI/Swagger-documented HTTP APIs in-cluster (there is no single hosted public REST endpoint for the open-source tool). ARMO Platform is the commercial multi-cluster, multi-cloud SaaS built on Kubescape and exposes a documented hosted Customer API (base https://api.armosec.io) for posture, compliance, vulnerabilities, runtime incidents, attack paths, network policies, and registry/repository scanning, authenticated with an X-API-KEY access key.

**Areas:** Kubernetes Security · Cloud Native Security · Container Security · DevSecOps · Kubernetes · Vulnerability Scanning · Compliance · Runtime Security · CNCF · Open Source

## Kubescape on APIs.io

Everything profiled for Kubescape is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/kubescape/](https://apis.io/providers/kubescape/)** — or go straight to one of the APIs or properties below.

### APIs (7)

- [Kubescape In-Cluster Component API (Open Source)](https://apis.io/apis/kubescape/kubescape-in-cluster-component-api/) — The open-source Kubescape Operator's in-cluster components (storage, kubevuln, gateway, operator, node-agent) each expose an OpenAPI/Swagger-documented HTTP…
- [Kubescape Access Keys API](https://apis.io/apis/kubescape/kubescape-access-keys-api/) — Agent access keys and exception policies.
- [Kubescape Network Policies API](https://apis.io/apis/kubescape/kubescape-network-policies-api/) — Generated NetworkPolicies and seccomp profiles.
- [Kubescape Posture & Compliance API](https://apis.io/apis/kubescape/kubescape-posture-compliance-api/) — Framework, control, and resource posture results.
- [Kubescape Registry & Repository API](https://apis.io/apis/kubescape/kubescape-registry-repository-api/) — Registry scans and Git repository posture.
- [Kubescape Runtime Security API](https://apis.io/apis/kubescape/kubescape-runtime-security-api/) — Runtime incidents, attack chains, and security risks.
- [Kubescape Vulnerabilities API](https://apis.io/apis/kubescape/kubescape-vulnerabilities-api/) — Image and workload vulnerability scanning and results.

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### Agentic access (1)

Which operations an agent can call, which act, and which need a human in the loop.

- [Kubescape Agentic Access](https://apis.io/agentic-access/kubescape/kubescape-agentic-access/)

#### Collections (7)

Postman and Open Collection request collections.

- [ARMO Platform Customer API (Kubescape)](https://apis.io/collections/kubescape/open-kubescape/)
- [ARMO Platform Customer API (Kubescape) Access Keys API](https://apis.io/collections/kubescape/open-kubescape-access-keys-api/)
- [ARMO Platform Customer API (Kubescape) Access Keys Network Policies API](https://apis.io/collections/kubescape/open-kubescape-network-policies-api/)
- [ARMO Platform Customer API (Kubescape) Access Keys Posture & Compliance API](https://apis.io/collections/kubescape/open-kubescape-posture-compliance-api/)
- [ARMO Platform Customer API (Kubescape) Access Keys Registry & Repository API](https://apis.io/collections/kubescape/open-kubescape-registry-repository-api/)
- [ARMO Platform Customer API (Kubescape) Access Keys Runtime Security API](https://apis.io/collections/kubescape/open-kubescape-runtime-security-api/)
- [ARMO Platform Customer API (Kubescape) Access Keys Vulnerabilities API](https://apis.io/collections/kubescape/open-kubescape-vulnerabilities-api/)

#### Security (2)

Authentication, trust centre, and vulnerability disclosure.

- [Kubescape Authentication](https://apis.io/security/kubescape/kubescape-authentication/)
- [Kubescape Domain Security](https://apis.io/security/kubescape/kubescape-domain-security/)

#### Plans and pricing (1)

Published plans, tiers and prices.

- [Kubescape Plans Pricing](https://apis.io/plans/kubescape/kubescape-plans-pricing/)

#### Rate limits (1)

Published request limits.

- [Kubescape Rate Limits](https://apis.io/rate-limits/kubescape/kubescape-rate-limits/)

#### FinOps (1)

What the API costs to run, by operation.

- [Kubescape Finops](https://apis.io/finops/kubescape/kubescape-finops/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://kubescape.io)
- [Documentation](https://kubescape.io/docs/)
- [Blog](https://kubescape.io/blog/)
- [GitHub](https://github.com/kubescape)

## API Evangelist rating

**Kin Score 26.0** — emerging · rubric 0.24.0 · scored 2026-10-17

| Facet | Score |
|---|---|
| Discoverability | 66.1 |
| Contract quality | 47.8 |
| Contract governance | 0.0 |
| Operational transparency | 10.5 |
| Developer ergonomics | 28.6 |
| Access clarity | 7.9 |

**Agent readiness 17.9** — agent-aware

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | yes |
| Agentic Access | derived (partial credit) |
| Reversibility Documented | — |
| MCP Server | — |
| Auth Clarity | bearer (partial credit) |
| Idempotency | — |
| Error Semantics | — |
| OpenAPI Examples | — |
| Rate Limit Signal | derived (partial credit) |
| Event Surface Described | — |
| Agent Skills | — |
| Well Known Catalog | — |
| Consent Identity | — |
| Agent Card | — |
| Dry Run Mode | — |
| Delegated Identity | — |
| Protected Resource Metadata | — |
| Dynamic Client Registration | — |
| Agentic Commerce | — |

**Regulatory alignment 11.8** — Horizontal (data, software, accessibility, platform)

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/kubescape/](https://apis.io/providers/kubescape/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for Kubescape: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/kubescape/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
