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
---

# Session 02 — Approved Technical Design

**Date:** 2026-10-09
**Stage:** Phase 2 — Repository & Architecture
**Status:** Design approved; implementation not started.

## 1. Official Project Scope

Project: `cloud-native-infra-lab`

Goal: Build a local-first Cloud-Native lab demonstrating infrastructure,
networking, container orchestration, operations, and security skills.

The project has three integrated pillars:

1. **Infrastructure & Networking**
   - Linux environment, networking, connectivity, resource management,
     and troubleshooting.
2. **Cloud-Native & Platform**
   - Docker, Kubernetes workloads, declarative configuration,
     workload lifecycle, and deployment automation.
3. **Security & Operations**
   - Least privilege, container hardening, access control, network
     policy validation, logging, health checks, and security testing.

AI, a large SIEM/SOAR stack, production deployment, and paid cloud
services are not part of the initial scope. Future expansion requires
a clear need and an explicit design decision.

## 2. Approved Environment and Constraints

- Windows host with WSL2 and Ubuntu.
- Docker Desktop for container runtime.
- Existing `kind` cluster: `infra-lab`.
- Existing `kubectl`, Git, GitHub, and Python environment.
- Local-first; prefer free and open-source tools.
- Existing WSL2 resource configuration is approximately:
  6 GB RAM, 8 CPUs, and 8 GB swap.
- Do not create another cluster unless a documented requirement emerges.
- Do not install additional tools without a specific need.
- Add components incrementally and check resource usage.
- Swap is not equivalent to physical RAM.

## 3. Logical Architecture

### Development and source control
- Windows, VS Code, WSL2, Git, and GitHub.
- Git manages changes; GitHub stores committed source and documentation.
- Credentials and secrets must not be committed to the repository.

### Local platform
- Docker Desktop builds and runs container images.
- `kind` provides the local Kubernetes cluster.
- `kubectl` manages Kubernetes resources through the Kubernetes API.
- Docker access and kubeconfig are privileged control paths and must
  be protected.

### Workload zone
- A small Python HTTP service is the first planned workload.
- A test client sends requests to the service.
- Operations uses Kubernetes logs, Events, status, and health checks.
- Security controls are introduced incrementally and tested.
- Each logical role does not necessarily require a separate Pod
  or Kubernetes resource.

### Initial request path
Test client -> `kubectl port-forward` -> Kubernetes Service/Pod
-> Python HTTP service -> HTTP response.

The exact Kubernetes resources and application implementation will be
defined during the implementation phase. This section describes the
intended logical path, not a deployed system.

## 4. Communication Flows

| ID | Source -> Destination | Purpose | Control |
|---|---|---|---|
| F1 | WSL2 <-> GitHub | Source and documentation sync | Protect credentials; no committed secrets |
| F2 | WSL2 -> Docker | Build/manage images | Use Docker privileges only when needed |
| F3 | `kubectl` -> Kubernetes API | Manage cluster resources | Protect kubeconfig; avoid unnecessary broad permissions |
| F4 | Test client -> HTTP service | Test application behavior | Initially prefer `kubectl port-forward` |
| F5 | Kubernetes -> application | Health checks | Checks should not cause unintended state changes |
| F6 | Operator -> logs/Events | Troubleshooting | Treat logs as operational evidence, not inherently immutable evidence |
| F7 | Workload -> workload | Internal service communication, if needed | Allow only justified communication paths |

F7 is not required for the first workload because the initial service
does not require a database or another supporting service.

## 5. Trust Boundaries and Threat Model

Trust boundaries:

- Developer/source-control environment.
- Local platform and privileged management interfaces.
- Application workloads and their runtime permissions.
- Internal workload communication.

Initial risks and intended checks:

- Excessive container privileges:
  validate non-root execution and remove unnecessary capabilities
  where compatible.
- Unnecessary Kubernetes API access:
  restrict ServiceAccount permissions and consider disabling
  automatic token mounting when not required.
- Unnecessary network access:
  define intended communication paths and test allowed/blocked traffic.
- Secret leakage:
  exclude secrets from Git and use dummy data in the lab.
- Unsafe image/configuration:
  record image provenance, versions, and applicable validation results.
- Application failures:
  verify health checks and use logs/Events to investigate test failures.

NetworkPolicy implementation is deferred to the Security phase.
First verify whether the existing `kind` networking environment can
enforce the intended policy. Do not assume that creating a policy
resource proves enforcement.

Local tests do not demonstrate isolation equivalent to separate
physical hosts or independent cloud accounts. Kubernetes logs alone
do not prove tamper-resistant or immutable logging.

## 6. Technical Decision Register

| ID | Decision | Status |
|---|---|---|
| D-01 | Local-first; prefer free tools | Approved |
| D-02 | Integrate Infrastructure, Cloud-Native, and Security | Approved |
| D-03 | Reuse existing `infra-lab` kind cluster | Approved |
| D-04 | Start with a small HTTP service without a database | Approved |
| D-05 | Use Python for the HTTP service | Approved |
| D-06 | Start with plain Kubernetes YAML | Approved default |
| D-07 | Prefer locally built images | Approved default |
| D-08 | Initially access the service with `kubectl port-forward` | Approved default |
| D-09 | Start operations checks with existing Kubernetes commands | Approved default |
| D-10 | Decide and test NetworkPolicy during the Security phase | Approved |
| D-11 | Add centralized logging, metrics, or CI only when justified | Approved default |
| D-12 | Never commit secrets to the repository | Approved |

These decisions may be revised if testing reveals a limitation.
Record the reason and impact before changing a decision.

## 7. Target Repository Structure

Planned structure, to be created incrementally as needed:

- `README.md` — project overview and entry point.
- `docs/architecture.md` — architecture and communication flows.
- `docs/decisions/` — technical decision records.
- `docs/operations/` — operation and troubleshooting guides.
- `docs/security/` — threat model and security test results.
- `app/` — HTTP service source code.
- `container/` — container image build definition.
- `k8s/` — Kubernetes configuration.
- `scripts/` — repeatable operational tasks.
- `tests/` — functional, operational, and security tests.

Do not create empty directories solely to match this target structure.
Create each file or directory when it has a defined purpose.

## 8. Roadmap and Acceptance Criteria

### Phase 1 — Environment & Foundation
Status: environment setup previously verified.
Maintain a working Git/GitHub workflow and the existing local cluster.

### Phase 2 — Repository & Architecture
Acceptance criteria:
- Document the logical architecture and trust boundaries.
- Document the primary communication flows.
- Record technical decisions and known limitations.
- Agree on repository structure before adding implementation files.

### Phase 3 — Container & Kubernetes Baseline
Acceptance criteria:
- Build the application image using documented steps.
- Deploy the workload to the existing cluster.
- Verify HTTP behavior, health checks, and resource configuration.
- Demonstrate an update and a documented cleanup procedure.

### Phase 4 — Operations & Observability
Acceptance criteria:
- Locate relevant logs and Events for a controlled test failure.
- Record workload status and relevant resource usage.
- Document a reproducible troubleshooting procedure.

### Phase 5 — Security & Hardening
Acceptance criteria:
- Verify application runtime privileges and API access configuration.
- Test at least one permitted and one denied access case.
- Verify network policy enforcement before claiming it is effective.
- Document limitations of the local environment.

### Phase 6 — Automation & CI
Acceptance criteria:
- Automate stable, repeatable tasks.
- Add CI only when checks and deployment steps are sufficiently stable.
- Verify automation results rather than assuming success.

### Phase 7 — Validation & Portfolio
Acceptance criteria:
- Provide a clear README and architecture documentation.
- Document setup, operation, testing, cleanup, and known limitations.
- Include actual test evidence and distinguish verified features
  from planned features.

## 9. Current Status and Next Action

**Design approved:**

* Project scope and three integrated pillars.
* Logical architecture and initial communication flows.
* Trust boundaries, initial threat model, and technical decisions.
* Roadmap and acceptance criteria.

**Documentation update:**

* The approved design has been recorded in `PROJECT_LOG.md`.
* The changes are under review and have not yet been committed.

**Still pending:**

* Review and commit the documentation changes.
* Complete dedicated architecture documentation and any other Phase 2 deliverables.
* Verify the Phase 2 acceptance criteria before starting workload implementation.

**Implementation status:**

* No workload deployed as part of this design update.
* No deployment configuration created as part of this design update.
* No additional tools installed as part of this design update.
* NetworkPolicy enforcement has not been tested.
* No observability stack installed.

**Next action:**

1. Complete the documentation review.
2. Commit and push the approved documentation update.
3. Complete any remaining Phase 2 deliverables.
4. Start implementation only as a separately tracked next phase.
