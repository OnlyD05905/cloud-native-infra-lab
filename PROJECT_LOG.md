# Project Journey Log — Cloud Native Infrastructure Lab

## 1. Project Overview

* **Project name:** Cloud Native Infrastructure Lab
* **Repository:** `cloud-native-infra-lab`
* **GitHub:** https://github.com/OnlyD05905/cloud-native-infra-lab
* **Started tracking:** 2026-10-09
* **Current phase:** Phase 1 — Environment & Foundation
* **Current status:** Development environment restored and verified

### Project Direction

Build a personal infrastructure and cloud-native engineering project, starting locally and keeping the architecture cloud-ready.

The project aims to demonstrate practical skills in:

* Infrastructure and Linux environments
* Docker and Kubernetes
* Networking and system operations
* Observability and troubleshooting
* Security and system hardening
* Automation and CI/CD
* Technical documentation and architecture design

Prefer free and open-source technologies where practical. Cloud deployment is optional and should only be considered when justified.

> These are the current project directions. Specific technologies, architecture, and scope must be evaluated before implementation.

---

## 2. Current Position

### Confirmed Environment Status

* [x] Git repository initialized
* [x] GitHub remote configured
* [x] Initial commit created
* [x] Local branch `main` synchronized with `origin/main`
* [x] Git working tree clean
* [x] WSL2 Ubuntu environment available
* [x] Python 3 and virtual environment configured
* [x] Docker Desktop running Linux containers
* [x] Docker `hello-world` test succeeded previously
* [x] Local Kubernetes cluster `infra-lab` created using kind
* [x] Kubernetes node reports `Ready`
* [x] Kubernetes system Pods report `Running` and `Ready`

### Important Notes

* The local Kubernetes cluster was preserved when Docker was shut down.
* Cluster deletion previously failed because Docker was already stopped.
* The cluster was subsequently recovered and verified; it was not necessary to recreate it.
* A clean Git working tree means there are no uncommitted changes at the last check. It does not, by itself, prove every environment component is fully configured.

---

## 3. Overall Roadmap

### Phase 1 — Environment & Foundation

**Status: Mostly verified**

* [x] Set up the development environment
* [x] Configure Git and GitHub
* [x] Configure Docker Desktop
* [x] Create and verify the local Kubernetes cluster
* [ ] Inspect the current repository structure
* [ ] Finalize project goals and boundaries
* [ ] Draft the initial architecture
* [ ] Record key technical decisions

**Completion criteria:** The environment is reproducible, project scope is clear, and an initial architecture has been documented.

### Phase 2 — Infrastructure Baseline

**Status: Not started**

* [ ] Define the system requirements
* [ ] Identify core components and their responsibilities
* [ ] Design the initial architecture and communication paths
* [ ] Decide how configuration and infrastructure files will be organized
* [ ] Review resource constraints and technical trade-offs

**Completion criteria:** The architecture and implementation plan are agreed upon before workloads are introduced.

### Phase 3 — Containerization & Kubernetes

**Status: Not started**

* [ ] Select or prepare a suitable test workload
* [ ] Define the container build and configuration approach
* [ ] Deploy the workload to local Kubernetes
* [ ] Verify access, health, and lifecycle behavior
* [ ] Document deployment and troubleshooting procedures

**Completion criteria:** A documented, repeatable deployment works locally.

### Phase 4 — Observability & Operations

**Status: Not started**

* [ ] Define operational signals to monitor
* [ ] Establish logging and metrics collection
* [ ] Verify workload health and basic failure detection
* [ ] Practice troubleshooting and recovery
* [ ] Document observations and results

**Completion criteria:** System behavior can be inspected and common problems can be diagnosed.

### Phase 5 — Security & Hardening

**Status: Not started**

* [ ] Identify the relevant threats and security boundaries
* [ ] Review access controls and permissions
* [ ] Review secrets and configuration handling
* [ ] Apply appropriate container and Kubernetes hardening
* [ ] Perform security checks and record evidence

**Completion criteria:** Security controls are documented and their effectiveness is tested where practical.

### Phase 6 — Automation & CI/CD

**Status: Not started**

* [ ] Identify repetitive tasks worth automating
* [ ] Add appropriate automated checks
* [ ] Introduce CI/CD where it provides clear value
* [ ] Make deployment and configuration changes repeatable
* [ ] Verify the automation workflow

**Completion criteria:** Selected checks and workflows can run consistently with less manual effort.

### Phase 7 — Validation & Portfolio

**Status: Not started**

* [ ] Validate the system against the defined requirements
* [ ] Record test results and known limitations
* [ ] Finalize architecture diagrams
* [ ] Write the public-facing README
* [ ] Document setup, operation, and troubleshooting
* [ ] Prepare a demonstration suitable for GitHub and a technical portfolio
* [ ] Evaluate whether cloud deployment is justified

**Completion criteria:** Another person can understand the design, reproduce the environment, verify the results, and evaluate the engineering decisions.

---

## 4. Current TODO — Next Actions

Only work on the following items for now:

* [ ] Inspect the existing repository files without modifying them.
* [ ] Confirm the initial project scope and intended outcomes.
* [ ] Draft and review the initial architecture.
* [ ] Agree on the next implementation step.

**Current next action:** Inspect the repository structure.

**Do not deploy application workloads or install additional tools until the relevant design decision has been made.**

---

## 5. Technical Decisions & Constraints

Record decisions here as the project evolves.

| Topic                     | Current decision or status                      |
| ------------------------- | ----------------------------------------------- |
| Development environment   | WSL2 + Ubuntu                                   |
| Container runtime         | Docker Desktop, Linux containers                |
| Local Kubernetes          | kind                                            |
| Version control           | Git + GitHub                                    |
| Initial deployment target | Local environment                               |
| Cloud deployment          | Optional; evaluate later                        |
| Technology selection      | Prefer free/open-source options where practical |
| Resource usage            | Consider available machine memory and CPU       |
| Implementation approach   | Small, verifiable steps                         |
| Project scope             | Must be agreed upon before implementation       |

### Decision Record Template

For each significant technical decision, record:

* **Decision:**
* **Context / problem:**
* **Options considered:**
* **Reason for selection:**
* **Trade-offs:**
* **Date:**

---

## 6. Work Session Log

### Session 01 — Environment Recovery

**Date:** 2026-10-09

**Completed**

* Opened Docker Desktop.
* Confirmed the existing kind control-plane container was running.
* Verified the Kubernetes node was `Ready`.
* Verified Kubernetes system Pods were `Running` and `Ready`.
* Opened the WSL project directory.
* Confirmed branch `main` was synchronized with `origin/main`.
* Confirmed the Git working tree was clean.

**Outcome**

The development environment is operational based on the checks performed. No application workload has been implemented as part of this session.

**Next session**

* Inspect the repository structure.
* Confirm project scope.
* Draft the initial architecture.

---

## 7. How to Resume After a Break

Whenever returning to the project:

1. Read this file, especially Sections 2, 4, and 6.
2. Check the current environment if necessary.
3. Review the latest Git status and repository contents.
4. Continue from the first incomplete TODO.
5. Update the session log after meaningful progress.

Before making a significant change, record the intended action and its expected result.

### Working Rules

* Work in small steps and verify each result.
* Do not install tools without a clear reason.
* Do not implement features before the scope and design are sufficiently clear.
* Keep technical decisions and trade-offs documented.
* Update this file when the roadmap, decisions, or progress changes.
* Never record passwords, access tokens, or other secrets in this file.
