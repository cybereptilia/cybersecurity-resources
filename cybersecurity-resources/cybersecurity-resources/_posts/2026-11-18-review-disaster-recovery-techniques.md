---
layout: post
title: "Paper Review – Disaster Recovery Plan: Restoring IT Systems After Cyberattacks"
date: 2026-11-18 09:00:00 -0400
categories: [paper-review, disaster-recovery]
---

## Bibliography

Nawrocka, M. (2026). A review and comparative analysis of techniques for restoring IT system continuity after cyberattacks. *Safety & Defense, 12*(1), 35–43. <https://doi.org/10.37105/sd.280>

## Summary

This article reviews the techniques organizations use to restore their IT systems after a cyberattack and compares them on the two metrics that drive every disaster recovery plan: recovery time objective (RTO) and recovery point objective (RPO). Using a systematic literature review based on the Kitchenham and Charters guidelines, the author searched IEEE Xplore, Scopus, Web of Science, and ScienceDirect and analyzed 40 qualifying studies. Four groups of techniques are compared: traditional backups, redundant systems (such as high-availability clusters, multi-cloud setups, and secondary data centers), virtualization (snapshots and virtual machine migration), and cloud-based Disaster Recovery as a Service (DRaaS). The article concludes that traditional backups are the slowest option, with recovery times of hours to days, while redundancy, virtualization, and DRaaS can restore service in minutes to hours. It recommends hybrid recovery that combines local redundancy with cloud recovery sites, automation of recovery, regular testing with cyberattack simulations, and staff training.

## Review

The topic of this article is very relevant, because a disaster recovery plan written for fires and floods is not automatically ready for ransomware. Its most useful contribution is the comparison table, which places four families of recovery techniques side by side on RTO and RPO. For someone designing a disaster recovery plan, this makes the trade-off clear: faster recovery requires more investment in redundancy, virtualization, or cloud services. The recommendations, especially hybrid recovery and regular testing, are practical and agree with current government guidance, such as CISA's advice to keep offline backups and test them in disaster recovery scenarios.

However, the research is not as rigorous as the method section suggests. The author describes a systematic review but does not report how many records were found and screened, does not list the 40 included studies, and does not report the quality scores even though a scoring method is described. The years covered are also inconsistent: the text gives 2011 to 2025, while the inclusion table gives 2013 to 2025. Most importantly, the RTO and RPO ranges in the comparison table are not tied to specific measured results, and they do not always match the text: traditional backups have an RPO of 12 to 24 hours in the table but anywhere from several hours to a full day in the discussion. A reader cannot tell where the numbers come from.

Several parts of the argument needed more detail. Although the title focuses on cyberattacks, much of the evidence concerns general failures, and ransomware-specific problems, such as attackers deleting backups, malware hiding in backups, and the need for a clean recovery environment, receive only brief mention. The article also promises an economic comparison but offers no cost figures. A useful follow-up would test these techniques in a controlled environment, simulating a ransomware attack and measuring actual recovery times and data loss for each method, and would estimate the cost of each option for small and large organizations.

I agree with the article's main conclusion that no single technique is enough and that a layered approach is the safest choice. It supported my opinion that backups alone are not a complete disaster recovery plan, since restoring from traditional backups can take days. However, the article did not change my view that **tested, offline backups** remain the foundation: replication and cloud recovery can copy an attacker's damage just as quickly as they copy good data, so an isolated backup is still the last line of defense.
