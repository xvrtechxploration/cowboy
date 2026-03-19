
Good. Your answers sketch a very clear direction: you want to become the kind of engineer who can move comfortably between **systems, infrastructure, and software**, without the abstraction fog that many DevOps tools create. The right way to do that is to build a **stack of small systems**, each revealing another layer of the machine.

So what I will outline is not just projects, but a **progression of systems**. Each one leaves behind something real: a tool, service, or automation platform you can show in a portfolio.

Think of it as building your own **personal infrastructure platform** over time.

---

# The Xavier Infrastructure Lab

*A progressive engineering portfolio*

The curriculum has **four phases**.

Each phase deepens your understanding of what happens underneath the tools you already use.

```
Phase 1 — Linux & CLI fundamentals
Phase 2 — APIs and automation
Phase 3 — Infrastructure orchestration
Phase 4 — Platform engineering
```

You already use Terraform, Ansible, and Linux daily. The goal is to **strip away the abstraction layers first**, then rebuild them intentionally.

---

# Phase 1 — Linux, Bash, and System Thinking

*Goal: understand the machine you’re standing on.*

These projects run entirely on your laptop.

---

## Project 1 — Build a Real CLI Tool

**Project:** `netinfo`

A command line tool that shows:

```
netinfo
```

Output example:

```
Hostname: ongchu
OS: CachyOS
Kernel: 6.x
IP addresses:
  - 192.168.1.44
  - 100.x.x.x (tailscale)

Default Gateway: 192.168.1.1
DNS Servers:
  - 192.168.1.2 (Pi-hole)

Active Interfaces:
  eth0
  tailscale0
```

### Skills learned

* bash scripting
* parsing command output
* environment variables
* CLI UX

### Concepts

You will directly use:

```
ip
hostnamectl
resolvectl
awk
grep
```

This builds intuition for **how Linux exposes system information**.

---

## Project 2 — Build Your Own "top"

**Project:** `syswatch`

A simple script that refreshes every second and displays:

```
CPU usage
Memory usage
Disk usage
Network traffic
```

Tools you'll learn:

```
/proc
vmstat
iostat
watch
```

You will discover how **Linux exposes metrics through pseudo-filesystems**.

This removes the abstraction behind monitoring tools.

---

## Project 3 — Log Analyzer

**Project:** `logscan`

A CLI tool that reads logs and extracts patterns.

Example:

```
logscan /var/log/syslog --errors
```

Outputs:

```
ERROR: nginx failed to start
ERROR: docker container exited
```

Skills:

* bash pipelines
* regex
* parsing structured vs unstructured logs

---

# Phase 2 — Python and APIs

*Goal: understand automation beneath Ansible.*

Now we begin writing **real programs**.

---

## Project 4 — API Explorer

**Project:** `apiview`

Python tool that queries APIs.

Example:

```
apiview github user xvr
apiview weather austin
```

Concepts:

* HTTP
* REST
* JSON
* headers
* authentication

Tools:

```
requests
json
argparse
```

You will **see exactly what Ansible modules do internally**.

---

## Project 5 — Network Device Collector

Now we bridge into **network automation**.

**Project:** `netcollector`

A Python program that:

```
connects to network devices
runs commands
stores output
```

Example inventory:

```yaml
devices:
  - name: leaf01
    host: 10.0.0.10
    platform: nxos
```

Concepts:

* SSH automation
* structured data
* device inventory

Tools:

```
netmiko
pyyaml
```

---

## Project 6 — Build Your Own Mini-Ansible

**Project:** `taskrunner`

A Python program that reads a YAML file:

```yaml
tasks:
  - name: check disk
    command: df -h

  - name: check uptime
    command: uptime
```

Then executes tasks remotely.

Concepts:

* YAML parsing
* task execution
* automation engines

You will finally see **what configuration management actually does internally**.

---

# Phase 3 — Infrastructure Automation

*Goal: connect automation to real infrastructure.*

Now we bring in your **homelab**.

---

## Project 7 — Homelab Inventory System

Build a **single source of truth** for your lab.

```
homelab-inventory/
```

Example:

```yaml
hosts:
  proxmox:
    ip: 192.168.1.20
    role: hypervisor

  pi4:
    ip: 192.168.1.30
    role: services
```

Then create tools that:

```
list hosts
ssh into hosts
check health
```

---

## Project 8 — Proxmox Automation

Python or Ansible tool that:

```
creates VMs
starts/stops VMs
lists VMs
```

Concepts:

* APIs
* authentication
* infrastructure provisioning

You will learn **how infrastructure APIs actually work**.

---

## Project 9 — GitOps Homelab

Repository structure:

```
homelab/
 ├ terraform/
 ├ ansible/
 ├ docker/
 ├ inventory/
```

Flow:

```
commit → deploy infrastructure → configure services
```

You will build:

```
terraform → create VM
ansible → configure services
docker → deploy apps
```

This mirrors **real DevOps platforms**.

---

# Phase 4 — Platform Engineering

*Goal: build something impressive.*

Now we build systems that combine everything.

---

## Project 10 — Infrastructure API

Create your own **infra API**.

Example:

```
POST /vm
DELETE /vm
GET /inventory
```

Backend:

```
FastAPI
```

The API then triggers:

```
terraform
ansible
```

Now you have **your own cloud control plane**.

---

## Project 11 — Homelab Dashboard

Web UI showing:

```
VMs
containers
network devices
system metrics
```

Tech:

```
FastAPI
HTML
CSS
JS
```

This scratches your **aesthetic + interface interest**.

---

## Project 12 — Network Automation Platform

The final project.

A full system:

```
inventory
automation engine
API
web UI
```

Capabilities:

```
run commands on devices
push configs
view network topology
```

This becomes a **portfolio centerpiece**.

---

# How This Builds Your Skills

| Skill                   | Where it develops |
| ----------------------- | ----------------- |
| Linux                   | Phase 1           |
| Bash                    | Phase 1           |
| Python                  | Phase 2           |
| APIs                    | Phase 2           |
| Network automation      | Phase 2           |
| Ansible understanding   | Phase 2–3         |
| Terraform               | Phase 3           |
| DevOps                  | Phase 3           |
| Application development | Phase 4           |

---

# Portfolio Outcome

After completing this track you will have repositories like:

```
netinfo
syswatch
logscan
apiview
netcollector
taskrunner
homelab-inventory
proxmox-automation
homelab-gitops
infra-api
homelab-dashboard
network-automation-platform
```

Anyone reviewing your work would see:

> This engineer understands systems from Linux to APIs to infrastructure.

---

# The Next Step

Before I generate the **actual first lab**, I want to ask one more thing.

Would you like the projects to also include:

### Option A — GitHub portfolio polish

Each project includes:

* README
* architecture diagrams
* screenshots
* design explanations

---

### Option B — Obsidian knowledge integration

Each project also generates:

```
notes
concept explanations
learning reflections
```

---

Also, if you'd like, I can turn this into a **complete 16-week learning roadmap** with weekly labs.

And I can design the **first project (`netinfo`) in detail** so you can start tonight.
