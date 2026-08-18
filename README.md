<div align="center">

# Umar Sabirin

### DevOps Engineer &nbsp;·&nbsp; Platform &nbsp;·&nbsp; SRE &nbsp;·&nbsp; Cloud

**I build infrastructure from bare-metal to cloud — with AI wired into CI/CD, observability, and incident response.**

<a href="https://www.linkedin.com/in/umar-sabirin-5896481a5"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn"></a>
<a href="mailto:umarsabirin369@gmail.com"><img src="https://img.shields.io/badge/Email-EA4335?style=for-the-badge&logo=gmail&logoColor=white" alt="Email"></a>
<img src="https://img.shields.io/badge/Indonesia_·_GMT%2B7-30A14C?style=for-the-badge&logo=googlemaps&logoColor=white" alt="Location">
<img src="https://img.shields.io/badge/Open_to_remote-8957E5?style=for-the-badge&logo=protondrive&logoColor=white" alt="Open to remote">

</div>

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

## 🧰 Tech Stack

<div align="center">
<table>
<tr>
<td align="right"><b>&nbsp;Cloud&nbsp;&&nbsp;Systems&nbsp;</b></td>
<td><img src="https://skillicons.dev/icons?i=aws,linux,docker,kubernetes,nginx" alt="AWS, Linux, Docker, Kubernetes, Nginx"></td>
</tr>
<tr>
<td align="right"><b>&nbsp;IaC&nbsp;&&nbsp;CI/CD&nbsp;</b></td>
<td><img src="https://skillicons.dev/icons?i=terraform,ansible,jenkins,githubactions,gitlab,git" alt="Terraform, Ansible, Jenkins, GitHub Actions, GitLab CI, Git"></td>
</tr>
<tr>
<td align="right"><b>&nbsp;Observability&nbsp;</b></td>
<td><img src="https://skillicons.dev/icons?i=prometheus,grafana,elasticsearch" alt="Prometheus, Grafana, Elasticsearch"></td>
</tr>
<tr>
<td align="right"><b>&nbsp;Languages&nbsp;</b></td>
<td><img src="https://skillicons.dev/icons?i=go,php,java,spring,laravel,bash" alt="Go, PHP, Java, Spring Boot, Laravel, Bash"></td>
</tr>
<tr>
<td align="right"><b>&nbsp;Data&nbsp;&&nbsp;Messaging&nbsp;</b></td>
<td><img src="https://skillicons.dev/icons?i=postgres,mysql,mongodb,redis,kafka,rabbitmq" alt="PostgreSQL, MySQL, MongoDB, Redis, Kafka, RabbitMQ"></td>
</tr>
</table>
</div>

<div align="center">

<img src="https://img.shields.io/badge/Packer-02A8EF?style=for-the-badge&logo=packer&logoColor=white" alt="Packer">
<img src="https://img.shields.io/badge/Proxmox-E57000?style=for-the-badge&logo=proxmox&logoColor=white" alt="Proxmox">
<img src="https://img.shields.io/badge/QEMU_/_KVM-FF6600?style=for-the-badge&logo=qemu&logoColor=white" alt="QEMU/KVM">
<img src="https://img.shields.io/badge/cloud--init-1B3A57?style=for-the-badge&logo=cloudfoundry&logoColor=white" alt="cloud-init">
<img src="https://img.shields.io/badge/ZFS-1E88E5?style=for-the-badge&logo=openzfs&logoColor=white" alt="ZFS">
<br>
<img src="https://img.shields.io/badge/Vault-FFEC6E?style=for-the-badge&logo=vault&logoColor=black" alt="Vault">
<img src="https://img.shields.io/badge/Trivy-1904DA?style=for-the-badge&logo=trivy&logoColor=white" alt="Trivy">
<img src="https://img.shields.io/badge/Snyk-4C4A73?style=for-the-badge&logo=snyk&logoColor=white" alt="Snyk">
<img src="https://img.shields.io/badge/SonarQube-4E9BCD?style=for-the-badge&logo=sonarqube&logoColor=white" alt="SonarQube">
<img src="https://img.shields.io/badge/OPA_/_Rego-7D9199?style=for-the-badge&logo=openpolicyagent&logoColor=white" alt="OPA">
<img src="https://img.shields.io/badge/CIS_/_STIG-486581?style=for-the-badge&logo=letsencrypt&logoColor=white" alt="CIS/STIG">
<br>
<img src="https://img.shields.io/badge/Loki-F46800?style=for-the-badge&logo=grafana&logoColor=white" alt="Loki">
<img src="https://img.shields.io/badge/Tempo-F46800?style=for-the-badge&logo=grafana&logoColor=white" alt="Tempo">
<img src="https://img.shields.io/badge/OpenTelemetry-4F62AD?style=for-the-badge&logo=opentelemetry&logoColor=white" alt="OpenTelemetry">
<img src="https://img.shields.io/badge/eBPF-C4451D?style=for-the-badge&logo=linux&logoColor=white" alt="eBPF">
<img src="https://img.shields.io/badge/HAProxy-106DA9?style=for-the-badge&logo=haproxy&logoColor=white" alt="HAProxy">
<img src="https://img.shields.io/badge/nftables-2E4053?style=for-the-badge&logo=wireguard&logoColor=white" alt="nftables">

</div>

## ⚙️ The pipeline I build

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

## 📈 Numbers I've shipped

<div align="center">

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

</div>

## 🔭 What I'm doing now

- Infrastructure CI/CD in **Jenkins** for Terraform and Ansible — lint, test, security, and cost gates before anything is provisioned.
- Hardened golden images with **Packer**, benchmarked against CIS/STIG and scanned with Trivy.
- **AI** wired into monitoring and CI/CD for root-cause detection and auto-remediation.
- Cost- and security-aware observability on **Prometheus, Grafana, and ELK** with automated alerting.

## 🚀 Selected repositories

| Repo | What it is |
| :--- | :--- |
| [`job-board`](https://github.com/umars28/job-board) | Spring Boot microservices platform — modular services, independent deploys |
| [`spring-sync-vs-async-benchmark`](https://github.com/umars28/spring-sync-vs-async-benchmark) | Benchmark of 5 concurrency strategies; Kafka path sustained 2,683 req/s |
| [`mock-pilot`](https://github.com/umars28/mock-pilot) | Pluggable mock API server for REST and GraphQL with dynamic config |
| [`personal-finance-tracker`](https://github.com/umars28/personal-finance-tracker) | Laravel REST API on PostgreSQL + Redis, containerized with Docker |

---

<div align="center">

**B.Sc. Information Systems** — Hasanuddin University · GPA 3.82 / 4.00

<img src="https://img.shields.io/github/followers/umars28?style=for-the-badge&logo=github&label=Followers&labelColor=0D1117&color=1F6FEB" alt="Followers">
<img src="https://img.shields.io/github/stars/umars28?affiliations=OWNER&style=for-the-badge&logo=github&label=Stars&labelColor=0D1117&color=1F6FEB" alt="Stars">

<sub>Let's talk infrastructure — <a href="mailto:umarsabirin369@gmail.com">umarsabirin369@gmail.com</a> · <a href="https://www.linkedin.com/in/umar-sabirin-5896481a5">LinkedIn</a></sub>

</div>
