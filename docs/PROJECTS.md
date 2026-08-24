<p align="center">
  <a href="https://github.com/umars28"><img src="../assets/title-projects.svg" width="100%" alt="Featured work" /></a>
</p>

<p align="center">
  <sub><a href="https://github.com/umars28">← back to profile</a> &nbsp;·&nbsp; <a href="STACK.md">stack inventory</a> &nbsp;·&nbsp; <a href="COLLAB.md">collaboration</a> &nbsp;·&nbsp; <a href="https://umars28.github.io">labs</a></sub>
</p>

These are the repos I would actually want someone to open. Each one exists because reading about a
layer does not build a model of it — writing the layer does.

<img src="../assets/divider.svg" width="100%" alt="" />

## 🦀 [mars-container-runtime](https://github.com/umars28/mars-container-runtime) — Rust

An OCI-compliant container runtime written from scratch: the layer Docker and Kubernetes sit on top
of. It takes a filesystem bundle plus a `config.json` and turns it into an isolated process using
Linux namespaces, cgroup v2, OverlayFS, capabilities and seccomp.

```sh
$ docker run --rm --runtime=mars --memory=64m alpine:3.20 cat /sys/fs/cgroup/memory.max
67108864
```

That is Docker running `mars` instead of `runc`, enforcing a memory limit through a cgroup that
`mars` created and wrote itself.

| | |
|---|---|
| OCI validation suite | **26 passed** — `runc` 1.5.1 passes 22 on the same host |
| Integration suite | 128 assertions, all reading kernel state rather than the runtime's own claims |
| Docker drop-in | `run`, `run -it`, `exec`, `stop`, `--memory` |
| Startup tracing | OTLP spans per phase, accepted by Tempo |
| Deliberately out of scope | rootless without privilege, CNI networking, image pulling, cgroup v1 |

**Why it matters for ops.** Container failures in production happen in the layer Docker hides. The
repo reproduces nine of them with evidence read straight from the kernel — including three findings
worth stating outright:

- **An OOM kill does not reliably produce exit 137.** The kernel picks its victim by badness score,
  usually the allocating process rather than PID 1. Kill a child and PID 1 carries on: the container
  exits `0` having lost a process, with `oom_kill=1` in `memory.events` and nothing else to show for
  it. Kubernetes only marks a pod `OOMKilled` when PID 1 dies of signal 9 — so that case restarts
  nothing and alerts nobody.
- **A container can ignore `SIGTERM` for the entire grace period**, because PID 1 gets no default
  signal handlers.
- **A fix applied with `exec` survives a restart but not a recreate**, because it lived in the
  OverlayFS upper layer — which *is* the container.

<img src="../assets/divider-mirror.svg" width="100%" alt="" />

## ⚡ [xdp-lb](https://github.com/umars28/xdp-lb) — C + Rust

A layer-4 load balancer running on the XDP hook: packets are processed in the kernel, before they
reach the network stack. Datapath in C, control plane in Rust using [aya](https://aya-rs.dev) as the
loader.

```
                      ┌─────────────────────────────┐
                      │   control plane (Rust)      │
                      │  health check ──┐           │
                      │  maglev table ──┤           │
                      │  ARP resolve  ──┤           │
                      │  prom weights ──┤           │
                      │  drain API    ──┤           │
                      │  /metrics     ←─┘           │
                      └──────────┬──────────────────┘
                                 │ BPF maps
                                 ▼
   NIC ──▶ XDP hook ──▶ ┌──────────────────────┐ ──▶ XDP_TX ──▶ backend
                        │  datapath (C)        │
                        │  parse → conntrack   │ ──▶ XDP_PASS ──▶ kernel stack
                        │  → rate limit        │
                        │  → maglev → NAT      │ ──▶ XDP_DROP
                        └──────────────────────┘
```

**The design decision that matters.** The datapath never makes a decision that needs I/O. Anything
requiring external state — which backend is healthy, what weight it carries, which MAC address to
use — is computed in the control plane and written into a BPF map. The datapath only reads maps.

The consequence: however complex the control-plane logic gets, the per-packet cost stays flat.
Weights that track backend CPU utilisation in real time still resolve to a single array lookup in the
datapath.

| | |
|---|---|
| Backend selection | Maglev consistent hashing, weighted |
| Flow persistence | Bidirectional LRU conntrack, one million entries |
| Return path | `XDP_TX` — never touches the kernel network stack |

<img src="../assets/divider.svg" width="100%" alt="" />

## 🦍 [GorillaGate](https://github.com/umars28/GorillaGate) — Go

A lightweight, high-performance API gateway inspired by Kong. Request routing, authentication, rate
limiting and observability for cloud-native and microservices architectures.

## 💼 [job-board](https://github.com/umars28/job-board) — Java / Spring Boot

A job board information system on a microservices architecture — each service runs independently and
talks over REST. Split out into its own services, which are separate repos:

- [job-board-chat-service](https://github.com/umars28/job-board-chat-service) — chat
- [job-board-notification-service](https://github.com/umars28/job-board-notification-service) — notifications

<img src="../assets/divider-mirror.svg" width="100%" alt="" />

## Also on the shelf

| Repo | What it is |
|---|---|
| [Aegis](https://github.com/umars28/Aegis) | Cloud image control plane — enforced immutability, validation pipelines, lifecycle governance |
| [floci](https://github.com/umars28/floci) | A light, free AWS local emulator alternative |
| [sshm](https://github.com/umars28/sshm) | SSH host manager, Go |
| [mock-pilot](https://github.com/umars28/mock-pilot) | Pluggable mock API server for REST and GraphQL, Spring Boot |
| [spring-sync-vs-async-benchmark](https://github.com/umars28/spring-sync-vs-async-benchmark) | Benchmarking sync vs async execution — thread pools, Kafka, RabbitMQ, Redis |
| [agent-skills](https://github.com/umars28/agent-skills) | Production-grade engineering skills for AI coding agents |
| [laravel-github-actions-pipeline](https://github.com/umars28/laravel-github-actions-pipeline) | CI/CD with GitHub Actions — staging and production promotion |

<img src="../assets/divider.svg" width="100%" alt="" />

<p align="center">
  <sub>The production infrastructure work lives in company repos. Happy to walk through any of it in a call.</sub>
</p>

<p align="center">
  <a href="mailto:umarsabirin369@gmail.com"><img src="https://img.shields.io/badge/Let's%20talk-umarsabirin369@gmail.com-EA4335?style=for-the-badge&logo=gmail&logoColor=white" alt="Email" /></a>
</p>
