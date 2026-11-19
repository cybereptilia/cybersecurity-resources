---
layout: post
title: "Data Recovery: Getting Your Data Back When Things Go Wrong"
date: 2026-11-15 09:00:00 -0400
categories: [data-recovery]
---

Every organization will eventually lose data. A disk fails, an employee deletes the wrong folder, ransomware encrypts a file server, or a hurricane takes out power to a data center for days. **Data recovery** is the set of processes and tools used to restore data that has been lost, corrupted, deleted, or made inaccessible, and to bring it back to a usable state. This post explains how data recovery works, the main techniques, and the practices that separate organizations that recover quickly from those that do not.

## Why data gets lost

Data loss usually comes from one of five causes:

1. **Hardware failure.** Hard drives, SSDs, controllers, and servers wear out or fail without warning.
2. **Human error.** Accidental deletion, overwriting a file, or running the wrong command on a production database.
3. **Software problems.** Bugs, failed updates, or corrupted file systems and databases.
4. **Cyberattacks.** Ransomware encrypts data and often tries to destroy backups too; other attacks delete or alter data.
5. **Physical disasters.** Hurricanes, floods, fires, and long power outages. For anyone in Puerto Rico, Hurricane María in 2017 is a reminder that a whole region can lose power and connectivity for weeks.

The cause matters because it decides which recovery method will work. A deleted file can be restored from last night's backup in minutes; a building that is underwater needs a copy of the data somewhere else entirely.

## Two numbers that drive every recovery plan

Before choosing any tool, an organization has to decide how much loss it can tolerate. Two measures capture this:

- **Recovery Point Objective (RPO):** the maximum amount of data, measured in time, the business can afford to lose. If backups run once a night, the RPO is up to 24 hours: anything created since the last backup could be gone.
- **Recovery Time Objective (RTO):** the maximum time a system can be down before the impact becomes unacceptable.

**Example:** an online store might decide its order database needs an RPO of 15 minutes and an RTO of 1 hour, because every lost order is lost revenue. The same company's internal training videos might tolerate an RPO of a week and an RTO of several days. Different data deserves different protection, and the cost rises quickly as RPO and RTO approach zero.

## Backup types

Backups are the foundation of data recovery. There are three classic types:

| Type | What it copies | Advantage | Disadvantage |
|---|---|---|---|
| **Full** | Everything, every time | Simplest and fastest to restore | Slow to run and uses the most storage |
| **Incremental** | Only what changed since the *last backup of any kind* | Fast and small | Restoring requires the last full backup plus *every* incremental since |
| **Differential** | Everything that changed since the *last full backup* | Restore needs only the full plus the latest differential | Grows larger each day until the next full backup |

**Example schedule:** a full backup every Sunday and an incremental backup every weeknight. If the server fails on Thursday morning, the team restores Sunday's full backup, then Monday's, Tuesday's, and Wednesday's incrementals, in order. If any one of those files is damaged, everything after it is lost, which is why the next practice matters so much.

## The 3-2-1 rule and its modern version

The most widely used backup guideline is the **3-2-1 rule**: keep **3** copies of the data, on **2** different types of media, with **1** copy offsite. The U.S. Cybersecurity and Infrastructure Security Agency (CISA) recommends it for both businesses and government agencies.

Ransomware changed the picture, because attackers now look for backups and delete or encrypt them before demanding payment. CISA's #StopRansomware Guide therefore recommends keeping **offline, encrypted backups** of critical data and **regularly testing** their availability and integrity in a disaster recovery scenario. Many organizations now follow an extended **3-2-1-1-0** rule:

- **3** copies, **2** media types, **1** offsite (as before),
- **1** copy offline, air-gapped, or *immutable* (it cannot be changed or deleted, even by an administrator, for a set period),
- **0** errors when restores are tested.

The last number makes the key point: **a backup that has never been tested is not a reliable backup.**

## Recovery techniques

Backups are one technique among several, each with a different speed and cost:

- **File-level restore:** recovering individual files or folders from a backup. Best for accidental deletions.
- **Image-based (bare-metal) restore:** restoring an entire server, including the operating system and applications, from a disk image. Useful when a machine fails completely.
- **Snapshots:** point-in-time copies taken by storage systems or virtualization platforms. They allow very fast rollback but usually live on the same system, so they do not protect against the loss of that system.
- **Replication:** continuously copying data to a second system or site. It gives very low RPO but copies mistakes and encryption too, so it complements backups rather than replacing them.
- **Disaster Recovery as a Service (DRaaS):** a cloud provider keeps copies of systems ready to start in its data center if the primary site is lost.
- **Physical and logical recovery:** when a drive is damaged and there is no backup, specialized labs can sometimes recover data from the hardware (physical), and software tools can sometimes rebuild deleted files or corrupted file systems (logical). These are last resorts: slow, expensive, and not guaranteed.

## Data recovery in practice: a ransomware scenario

Imagine a medical clinic whose file server is hit by ransomware on a Monday morning.

1. **Contain.** The IT team disconnects the infected server from the network so the ransomware cannot spread to other machines or reach the backups.
2. **Identify a clean restore point.** The team checks when the infection started. Restoring a backup taken *after* the attacker got in would bring the malware back.
3. **Restore.** The team rebuilds the server and restores Friday's offline backup. Because the clinic kept an offline copy, the ransomware never reached it.
4. **Verify.** Staff confirm that the restored patient files open correctly before the server returns to service.
5. **Report and learn.** Patient data may have been accessed, so the clinic evaluates its breach-notification obligations (see the post on ethics and legislation) and reviews how the attack got in.

The clinic loses one weekend of changes (its RPO) and about a day of downtime (its RTO), instead of paying a ransom with no guarantee of getting its data back.

## How data recovery fits into systems management

In *IT Systems Management*, Schiesser uses this exact relationship to define systems management: a contract with a disaster recovery provider is only useful if a dependable backup and restore process stands behind it. Data recovery connects several of his processes: **storage management** (where backups live), **business continuity** (keeping the business running during a disaster), **security** (protecting backups from attackers), and **change management** (making sure system changes do not break backups).

## Key takeaways

- Decide your **RPO and RTO** first; they determine which tools you need.
- Follow **3-2-1**, and add an **offline or immutable** copy to protect against ransomware.
- **Test restores regularly**; an untested backup is an assumption, not a plan.
- Match the technique to the problem: snapshots and file restores for everyday mistakes, offsite and cloud copies for disasters.

### Sources

- CISA. *#StopRansomware Guide*. <https://www.cisa.gov/stopransomware/ransomware-guide>
- CISA. *Back Up Business Data*. <https://www.cisa.gov/back-business-data>
- Schiesser, R. (2010). *IT Systems Management* (2nd ed.). Prentice Hall.
