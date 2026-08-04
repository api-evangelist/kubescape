# Kubescape (kubescape)

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
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

Kubescape is an open-source (Apache 2.0) Kubernetes security platform and CNCF incubating project, originally contributed by ARMO. It provides risk analysis, security and compliance posture scanning (NSA-CISA, MITRE ATT&CK, CIS, and more), misconfiguration detection, image and runtime vulnerability scanning (CVEs via Grype), and eBPF-based runtime threat detection across the IDE, CI/CD pipelines, and live clusters.

**Access model — read this first.** The core Kubescape is a **CLI** and an in-cluster **Operator**, not a single hosted HTTP API:

- The **CLI** (`kubescape scan ...`) is a command-line tool, not an HTTP API.
- The in-cluster **Operator** components (storage, kubevuln, gateway, operator, node-agent) each expose an **OpenAPI/Swagger-documented HTTP API reachable only inside the cluster** at `/openapi/v2/swaggerui`, `/openapi/v2/rapi`, and `/openapi/v2/docs`. There is no fixed public host for these, so they are documented (modeled) rather than called over the internet.
- **ARMO Platform** is the commercial multi-cluster, multi-cloud SaaS built on Kubescape and is where a **hosted public REST API** lives: the **Customer API** at `https://api.armosec.io/api/v1`, authenticated with an Agent Access Key in the `X-API-KEY` header. This is the concrete, callable HTTP surface documented in this entry.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/kubescape/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/kubescape/refs/heads/main/apis.yml)

## Tags

- Kubernetes Security
- Cloud Native Security
- Container Security
- DevSecOps
- Kubernetes
- Vulnerability Scanning
- Compliance
- Runtime Security
- CNCF
- Open Source

## Timestamps

- **Created:** 2026-07-11
- **Modified:** 2026-07-11

## APIs

The logical APIs below map the ARMO Platform Customer API (hosted) plus the open-source in-cluster component API. Endpoint **paths** come from the public ARMO Customer API reference; request/response **schemas** in the OpenAPI are honestly modeled, not copied from a published machine-readable spec.

### Kubescape Posture & Compliance API

Retrieve compliance posture across NSA-CISA, MITRE ATT&CK, CIS, and other frameworks — framework scan summaries, per-control run results (the 200+ Kubescape controls C-0001..C-0292), and affected Kubernetes resources.

- **Human URL:** [https://hub.armosec.io/reference/customer-api](https://hub.armosec.io/reference/customer-api)
- **Base URL:** `https://api.armosec.io/api/v1`

### Kubescape Vulnerabilities API

Initiate image vulnerability scans and read results — scan summaries and detailed CVE listings, severity metrics, top and over-time trends, and scoped views by vulnerability, image, or workload, including the "Vulnerabilities In Use" (runtime-observed) analysis.

- **Human URL:** [https://hub.armosec.io/reference/customer-api](https://hub.armosec.io/reference/customer-api)
- **Base URL:** `https://api.armosec.io/api/v1`

### Kubescape Runtime Security API

Read and triage eBPF-based runtime threat detection output — list runtime incidents and alerts, group by severity, resolve/unresolve incidents, and read attack-chain (attack path) analysis and prioritized security risks.

- **Human URL:** [https://hub.armosec.io/reference/customer-api](https://hub.armosec.io/reference/customer-api)
- **Base URL:** `https://api.armosec.io/api/v1`

### Kubescape Network Policies API

Generate and retrieve least-privilege Kubernetes NetworkPolicies and seccomp profiles derived from observed application behavior (the Bill of Behavior).

- **Human URL:** [https://hub.armosec.io/reference/customer-api](https://hub.armosec.io/reference/customer-api)
- **Base URL:** `https://api.armosec.io/api/v1`

### Kubescape Registry & Repository Scanning API

Schedule and manage container-registry scans (ECR, GAR, ACR, Harbor, Quay, Nexus, GitLab) and read Git repository posture, shifting Kubernetes security left into CI/CD pipelines.

- **Human URL:** [https://hub.armosec.io/reference/customer-api](https://hub.armosec.io/reference/customer-api)
- **Base URL:** `https://api.armosec.io/api/v1`

### Kubescape Access Keys API

Create, list, retrieve, and revoke the Agent Access Keys used to authenticate Customer API requests via `X-API-KEY`, plus manage posture and vulnerability exception policies.

- **Human URL:** [https://hub.armosec.io/docs/authentication](https://hub.armosec.io/docs/authentication)
- **Base URL:** `https://api.armosec.io/api/v1`

### Kubescape In-Cluster Component API (Open Source)

The open-source Operator's in-cluster components each expose an OpenAPI/Swagger-documented HTTP API inside the cluster (`/openapi/v2/swaggerui`). There is no hosted public endpoint — endpoints are modeled, not called over a fixed public host.

- **Human URL:** [https://www.armosec.io/blog/introducing-kubescape-open-api-framework/](https://www.armosec.io/blog/introducing-kubescape-open-api-framework/)
- **Base URL:** `http://<service-ip>:<service-port>`

## Common Properties

- [GitHub Organization](https://github.com/kubescape)
- [LinkedIn](https://www.linkedin.com/company/armosec)
- [Website](https://kubescape.io)
- [Documentation](https://kubescape.io/docs/)
- [Plans](plans/kubescape-plans-pricing.yml)
- [Rate Limits](rate-limits/kubescape-rate-limits.yml)
- [Fin Ops](finops/kubescape-finops.yml)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
