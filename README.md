<div align="center">

# Umar Sabirin

**DevOps Engineer** &nbsp;·&nbsp; Platform &nbsp;·&nbsp; SRE &nbsp;·&nbsp; Cloud

Infrastructure from bare-metal to cloud — with AI wired into CI/CD, observability, and incident response.

<a href="https://www.linkedin.com/in/umar-sabirin-5896481a5"><img src="https://img.shields.io/badge/LinkedIn-umar--sabirin-0A66C2?style=flat-square&logo=linkedin&logoColor=white&labelColor=0D1117" alt="LinkedIn"></a>
<a href="mailto:umarsabirin369@gmail.com"><img src="https://img.shields.io/badge/Email-umarsabirin369@gmail.com-EA4335?style=flat-square&logo=gmail&logoColor=white&labelColor=0D1117" alt="Email"></a>
<img src="https://img.shields.io/badge/Location-Indonesia%20·%20GMT%2B7-30A14C?style=flat-square&logo=googlemaps&logoColor=white&labelColor=0D1117" alt="Location">
<img src="https://img.shields.io/badge/Status-open%20to%20remote-8957E5?style=flat-square&labelColor=0D1117" alt="Status">

</div>

---

```console
$ whoami
umar sabirin — devops engineer @ Apple Developer Institute × S-Quantum Engine

$ cat /etc/profile.d/umar.env
EXPERIENCE="5 years — backend → platform → devops"
FOCUS="CI/CD · IaC · observability · hardening · virtualization"
PRIMARY_LANG="Go"
SCALE="19,400+ concurrent streams · 194 agents · multi-tenant"
AI_IN_THE_LOOP="true"

$ uptime
building things that stay up
```

## Delivery pipeline I build

```mermaid
flowchart TB
    A["COMMIT<br/>pull request"]
    B["CI GATES<br/>lint · unit · integration"]
    C["SECURITY + COST<br/>SAST · DAST · Trivy<br/>Snyk · Infracost"]
    D["GOLDEN IMAGE<br/>Packer · CIS / STIG"]
    E["PROVISION<br/>Terraform · Ansible"]
    F["Kubernetes · Docker"]
    G["Proxmox · QEMU / KVM"]
    H["OBSERVE<br/>Prometheus · Grafana · Loki<br/>Tempo · ELK · eBPF"]
    I(["AI<br/>root-cause · auto-fix"])

    A --> B --> C --> D --> E
    E --> F
    E --> G
    F --> H
    G --> H
    H --> I
    I -.->|feedback| B

    classDef edge stroke-width:2px
    class A,I edge
```

## The stack, by layer

| Layer | Tooling |
| :--- | :--- |
| `app` | Go *(primary)* · PHP / Laravel · Java / Spring Boot · Groovy / Grails · Bash |
| `ci-cd` | Jenkins · GitHub Actions · GitLab CI · Bitbucket |
| `iac-cac` | Terraform · Ansible · Packer · cloud-init · PXE / netboot |
| `runtime` | Docker · Kubernetes · Proxmox · QEMU / KVM (QMP) · LXC / LXD · ZFS |
| `cloud` | AWS — EC2 · EKS · S3 · RDS · IAM · VPC |
| `data` | PostgreSQL · MySQL · MongoDB · Redis · Elasticsearch · Kafka · RabbitMQ · SQS |
| `observability` | Prometheus · Grafana · Loki · Tempo · Mimir · Pyroscope · ELK · eBPF · OpenTelemetry |
| `security` | CIS / STIG hardening · Vault · OPA / Rego · Kyverno · Trivy · Snyk · SonarQube · SAST / DAST · mTLS · 2FA |
| `network` | Nginx · HAProxy · nftables · OpenVPN · DNS · IPv6 / SLAAC |
| `reliability` | SLI / SLO / SLA · error budgets · incident response · RCA · postmortems · MTTR / MTTD |
| `ai` | LLM-based PR review · AI-assisted CI/CD remediation · AI root-cause analysis |

## Signals from production

| Result | What it was | Where |
| :--- | :--- | :--- |
| **19,400+** concurrent streams | Go engine multiplexing gRPC/SSE from 194 agents at ms latency | Maxcloud |
| **~83%** faster pipelines | Parallelization, dependency caching, selective re-runs in Jenkins | ADI × S-Quantum |
| **~300%** faster VM boot | Custom Go orchestrator over QEMU/QMP — boot down to ~2s | Maxcloud |
| **45 min → <5s** | Tenant branding deploys via a JSON-driven config system, 6+ tenants | Maxcloud |
| **~40%** less provisioning time | Self-service LBaaS on HAProxy + nftables at the kernel level | Maxcloud |
| **2,683 req/s** | Kafka-backed async pipeline, ~3 orders of magnitude over the sync baseline | Freelance |
| **~99.9%+** payment availability | Multi-gateway failover with rate limiting and 2FA | Maxcloud |
| **~50%** faster queries | Targeted indexing + SQL refactoring on high-traffic multi-tenant tables | Fairtech |

## What I'm doing now

- Building infrastructure CI/CD in **Jenkins** for Terraform and Ansible — lint, test, security, and cost gates before anything is provisioned.
- Automating hardened golden images with **Packer**, benchmarked against CIS/STIG and scanned with Trivy.
- Wiring **AI** into monitoring and CI/CD for root-cause detection and auto-remediation.
- Cost- and security-aware observability with **Prometheus, Grafana, and ELK** plus automated alerting.

## Selected repositories

| Repo | What it is |
| :--- | :--- |
| [`job-board`](https://github.com/umars28/job-board) | Spring Boot microservices platform — modular services, independent deploys |
| [`spring-sync-vs-async-benchmark`](https://github.com/umars28/spring-sync-vs-async-benchmark) | Benchmark of 5 concurrency strategies; Kafka path sustained 2,683 req/s |
| [`mock-pilot`](https://github.com/umars28/mock-pilot) | Pluggable mock API server for REST and GraphQL with dynamic config |
| [`personal-finance-tracker`](https://github.com/umars28/personal-finance-tracker) | Laravel REST API on PostgreSQL + Redis, containerized with Docker |

---

<div align="center">

**Education** — B.Sc. Information Systems, Hasanuddin University · GPA 3.82 / 4.00

<img src="https://img.shields.io/github/followers/umars28?style=flat-square&logo=github&label=followers&labelColor=0D1117&color=1F6FEB" alt="Followers">
<img src="https://img.shields.io/github/stars/umars28?affiliations=OWNER&style=flat-square&logo=github&label=stars&labelColor=0D1117&color=1F6FEB" alt="Stars">

<sub>Reach me at <a href="mailto:umarsabirin369@gmail.com">umarsabirin369@gmail.com</a> or on <a href="https://www.linkedin.com/in/umar-sabirin-5896481a5">LinkedIn</a>.</sub>

</div>
