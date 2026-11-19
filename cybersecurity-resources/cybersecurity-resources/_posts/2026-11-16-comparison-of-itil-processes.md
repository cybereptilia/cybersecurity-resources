---
layout: post
title: "Comparing ITIL Processes with Schiesser's 12 Systems Management Processes"
date: 2026-11-16 09:00:00 -0400
categories: [itil, it-service-management]
---

Anyone who studies IT operations runs into **ITIL**, the most widely used framework for IT service management (ITSM). This post explains what ITIL is, how its processes have changed across versions, and how they compare with the 12 systems management processes in Rich Schiesser's *IT Systems Management*. The two overlap heavily, but they are not the same, and the differences say a lot about what each one is for.

## What ITIL is and how it evolved

ITIL (originally the *Information Technology Infrastructure Library*) is a collection of best practices for delivering IT as a service to the business. It was created by the UK government in the late 1980s and has gone through several major versions:

- **ITIL v2 (around 2000–2001):** organized mainly into two books. *Service Support* covered the day-to-day processes (incident, problem, change, release, and configuration management, plus the service desk as a function). *Service Delivery* covered the planning processes (service level, financial, capacity, availability, and IT service continuity management). Security management was covered in a separate book.
- **ITIL v3 (2007, updated in 2011):** reorganized everything around a service lifecycle (strategy, design, transition, operation, continual improvement), with **26 processes and 4 functions**.
- **ITIL 4 (2019):** replaced "processes" with **34 practices**, grouped into 14 general management practices, 17 service management practices, and 3 technical management practices. A practice is broader than a process: it includes the people, tools, and partners needed to do the work.

## Schiesser's 12 processes

Schiesser's book focuses on the **infrastructure**: the people, processes, and technology that keep systems stable and responsive. His 12 processes are availability, performance and tuning, production acceptance, change management, problem management, storage management, network management, configuration management, capacity planning, strategic security, business continuity, and facilities management.

## Side-by-side comparison

The table maps each of Schiesser's processes to its closest equivalent in ITIL v2 (the version his comparison builds on) and in ITIL 4 (the current version).

| Schiesser's process | Closest ITIL v2 process | Closest ITIL 4 practice |
|---|---|---|
| Availability | Availability management | Availability management |
| Performance and tuning | Partly capacity management | Capacity and performance management |
| Production acceptance | Release management | Release management; deployment management; service validation and testing |
| Change management | Change management | Change enablement |
| Problem management | Problem management (and incident management) | Problem management; incident management |
| Storage management | *No direct equivalent* | Partly infrastructure and platform management |
| Network management | *No direct equivalent* | Partly infrastructure and platform management |
| Configuration management | Configuration management | Service configuration management |
| Capacity planning | Capacity management | Capacity and performance management |
| Strategic security | Security management | Information security management |
| Business continuity | IT service continuity management | Service continuity management |
| Facilities management | *No direct equivalent* | Partly infrastructure and platform management |

And in the other direction, these ITIL components have **no equivalent among Schiesser's 12**:

| ITIL component | What it does |
|---|---|
| Service level management | Negotiates and monitors service level agreements (SLAs) with customers |
| Financial management for IT services | Budgets, accounts for, and sometimes charges for IT services |
| Service desk | The single point of contact between users and IT (a *function* in v2 and v3, a *practice* in ITIL 4) |
| Incident management (as a separate process) | Restores normal service as quickly as possible after an interruption |

## What the comparison shows

**1. Most of the processes match.** Availability, change, problem, configuration, capacity, security, and continuity appear in both. That is expected: any organization running IT services needs to control changes, fix recurring problems, plan capacity, and survive disasters.

**2. Schiesser covers the physical infrastructure that ITIL leaves out.** Storage management, network management, and facilities management (power, cooling, and physical space) have no ITIL v2 counterpart. ITIL describes *what* services the business receives; Schiesser also describes the hardware, networks, and buildings those services run on. ITIL 4 narrows the gap with its "infrastructure and platform management" practice, but it treats that area at a high level.

**3. ITIL covers the business relationship that Schiesser leaves out.** Service level management and financial management are about the agreement and the money between IT and its customers. Schiesser discusses SLAs and business cases in his early chapters on executive support and customer service, but he does not treat them as separate processes.

**4. They draw some boundaries differently.**
- ITIL separates **incident management** (get the user working again quickly) from **problem management** (find and remove the root cause). Schiesser's problem management covers much of both.
- Schiesser treats **performance and tuning** separately from **capacity planning**. ITIL v2 folded performance into capacity management, and ITIL 4 names the two together in one practice.
- Schiesser's **production acceptance** (deciding whether a new application is ready to run in production) is closest to ITIL's **release management**, but it is more focused on operations being ready to support the system.

**5. Version matters.** Many comparisons use ITIL v2's short list because it is easy to line up one to one. ITIL 4's 34 practices are broader and include areas such as risk management, supplier management, knowledge management, and workforce and talent management, which go well beyond either list.

## A practical example

Suppose a bank is moving its online banking application to a new server.

- Under **Schiesser's model**, the team uses *production acceptance* to confirm operations can support the new system, *change management* to schedule the move, *capacity planning* and *performance and tuning* to size the server, *storage* and *network management* to prepare the infrastructure, and *facilities management* to confirm power and cooling in the data center.
- Under **ITIL 4**, the team uses *change enablement*, *release management*, *deployment management*, *capacity and performance management*, and *service validation and testing*, and *service level management* checks that the new setup will still meet the uptime promised in the SLA.

Both approaches get the job done. Schiesser's view makes sure the infrastructure is solid; ITIL's view makes sure the service promised to the customer is kept.

## Key takeaways

- ITIL and Schiesser's processes **overlap in most core areas**: availability, change, problem, configuration, capacity, security, and continuity.
- **Only Schiesser** treats storage, network, and facilities management as separate processes.
- **Only ITIL** treats service level management, financial management, the service desk, and incident management as separate components.
- The frameworks complement each other: ITIL for **service and customer** focus, Schiesser for **infrastructure** depth.

### Sources

- Schiesser, R. (2010). *IT Systems Management* (2nd ed.). Prentice Hall. Chapter 6, "Comparison to ITIL Processes."
- ITSM.tools. *ITIL 4 Management Practices Explained: Full List and Purposes*. <https://itsm.tools/34-itil-4-management-practices/>
- Fortra. *ITIL Service Delivery* (ITIL v2). <https://www.fortra.com/solutions/automation/infrastructure/itil/itil-version-2/service-delivery>
