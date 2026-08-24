<p align="center">
  <a href="https://github.com/umars28"><img src="../assets/title-toolbox.svg" width="100%" alt="Toolbox" /></a>
</p>

<p align="center">
  <sub><a href="https://github.com/umars28">← back to profile</a> &nbsp;·&nbsp; <a href="PROJECTS.md">projects</a> &nbsp;·&nbsp; <a href="COLLAB.md">collaboration</a> &nbsp;·&nbsp; <a href="https://umars28.github.io">labs</a></sub>
</p>

The full inventory. Things I have shipped with, not things I have read about.

<img src="../assets/divider.svg" width="100%" alt="" />

| Area | Stack |
| ---: | :--- |
| **Languages** | Go *(primary)* · Rust · C · PHP / Laravel · Java / Spring Boot · Groovy / Grails · Bash |
| **Cloud** | AWS — EC2 · EKS · S3 · RDS · IAM · VPC |
| **Containers** | Docker · Kubernetes · OCI runtime internals |
| **Systems & Virtualization** | Linux · Proxmox · QEMU / KVM (QMP) · LXC / LXD · ZFS · bare-metal provisioning · PXE / netboot · cloud-init |
| **IaC & CaC** | Terraform · Ansible · Packer |
| **CI/CD** | Jenkins · GitHub Actions · GitLab CI · Bitbucket · Infracost cost gates |
| **Observability** | Prometheus · Grafana · Loki · Tempo · Mimir · Pyroscope · ELK · eBPF · OpenTelemetry |
| **Security** | CIS / STIG hardening · Vault · OPA / Rego · Kyverno · Trivy · Snyk · SonarQube · SAST · DAST · RBAC · 2FA · mTLS / TLS |
| **Reliability** | SLI / SLO / SLA · error budgets · incident response · RCA · postmortems · MTTR / MTTD |
| **Data & Messaging** | PostgreSQL · MySQL · MongoDB · Redis · Elasticsearch · Kafka · RabbitMQ · SQS |
| **Architecture & APIs** | Distributed systems · microservices · event-driven · multi-tenant · DDD · gRPC · REST · WebSocket |
| **AI & LLM** | LLM product integration · prompt engineering · LLM-based PR review · AI-assisted CI/CD remediation & alerting · AI-assisted root-cause analysis |
| **Web & Proxy** | Nginx · HAProxy |
| **Networking** | XDP / eBPF datapath · nftables · OpenVPN · DNS · IPv6 / SLAAC |

<img src="../assets/divider-mirror.svg" width="100%" alt="" />

## Where the depth is

Breadth is cheap; here is what I have actually taken apart.

| | |
|---|---|
| **Kernel-level networking** | Wrote an L4 load balancer on the XDP hook — C datapath, Rust control plane, maglev consistent hashing, bidirectional LRU conntrack. Built a self-service LBaaS on HAProxy + nftables. |
| **Container internals** | Wrote an OCI runtime from scratch: namespaces, cgroup v2, OverlayFS, capabilities, seccomp. Passes 26 OCI validation cases, 4 more than `runc` on the same host. |
| **Virtualization** | Orchestrated VMs directly over QEMU/QMP rather than through libvirt, with boot down to roughly 2 seconds. |
| **Go at scale** | Multiplexed 19,400+ concurrent gRPC/SSE streams from 194 agents through one engine. |
| **Hardening as a build step** | CIS/STIG benchmarked golden images produced by Packer and scanned in CI — not remediated afterwards in a patch window. |
| **Cost as a gate** | Infracost in the pipeline, so the bill is a build failure rather than an end-of-month surprise. |

<img src="../assets/divider.svg" width="100%" alt="" />

## What I am deliberately not claiming

Honest edges, so nobody wastes an interview slot on them.

- **eBPF beyond the datapath** — I have shipped XDP; broad `kprobe`/`uprobe`-based production tracing is in progress, not behind me.
- **Multi-cloud** — AWS is where my depth is. GCP and Azure are transferable, not lived-in.
- **Service mesh** — I know what Istio and Linkerd solve and have run neither at scale.
- **Rootless containers** — explicitly out of scope in my runtime work.

<img src="../assets/divider-mirror.svg" width="100%" alt="" />

<p align="center">
  <a href="mailto:umarsabirin369@gmail.com"><img src="https://img.shields.io/badge/Let's%20talk-umarsabirin369@gmail.com-EA4335?style=for-the-badge&logo=gmail&logoColor=white" alt="Email" /></a>
</p>
