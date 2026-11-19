---
layout: post
title: "Paper Review – Incident Response Planning: Learning from Cyber Security Incidents"
date: 2026-11-19 09:00:00 -0400
categories: [paper-review, incident-response]
excerpt: "A review of Patterson, Nurse, and Franqueira (2023), a systematic review of how organizations learn from cyber security incidents."
---

## Bibliography

Patterson, C. M., Nurse, J. R. C., & Franqueira, V. N. L. (2023). Learning from cyber security incidents: A systematic review and future research agenda. *Computers & Security, 132*, Article 103309. <https://doi.org/10.1016/j.cose.2023.103309>

## Summary

Every incident response plan ends with a "lessons learned" phase, and standards such as ISO/IEC 27035 and NIST SP 800-61 recommend it, but they say little about how to do it. This article reviews what research has found about how organizations learn from cyber security incidents. Following the PRISMA method, the authors searched eight databases, including the ACM Digital Library, IEEE Xplore, ScienceDirect, and Scopus, and narrowed 3,986 records down to 30 studies. They found that formal post-incident learning is usually reserved for major incidents, that review teams are mostly limited to technical staff, that lessons are rarely shared beyond the incident team, and that causal investigations tend to be shallow. Improvements focus on the incident response team rather than on the organization's wider security. None of the studies measured whether learning actually reduced future incidents. The authors organize the findings into a five-phase learning process and propose 14 questions for future research.

## Review

The quality of this paper is high, and it addresses a weak point in most incident response plans. Its method is transparent: it reports the search string, the eight databases, the inclusion and exclusion criteria, and each step of the selection, and its numbers add up from 3,986 records to the final 30 studies. A strength is that it borrows from safety science, a field with a longer tradition of learning from accidents, which brings in useful concepts such as double-loop learning: fixing the underlying assumptions that allowed an incident, not just the immediate technical flaw. The five-phase process, from participation and causal analysis through to evaluating whether learning worked, is a practical structure that an organization could use to design its own post-incident reviews.

The authors did thorough research, but the evidence base they found is thin. Thirty studies is a small number, most are case studies or interviews from a few countries and sectors, such as energy in Norway and healthcare in the UK, and many are five to ten years old. The paper also does not describe a formal quality appraisal of the included studies, so a small case study counts about as much as a larger one. The search terms could have been broader, since phrases such as "post-incident review" and "root cause analysis" were not included and might have found more relevant work. The authors also state that their data is not available, which makes the coding difficult to reproduce.

Some elements of the argument could have gone further. The paper explains well why organizations fail to learn, citing low priority, cost pressure, lack of management commitment, and a culture of blame, but it offers less on how to overcome those barriers. A useful follow-up article would test the five-phase process inside real organizations over time, measuring whether incidents of the same type become less frequent after lessons are applied. It would also be valuable to study how organizations learn together with their suppliers, since many incidents today begin at a third-party provider.

I agree with the article, and it changed the way I think about incident response planning. I used to see the plan as mainly about the response itself: detecting, containing, and recovering. The paper convinced me that the last phase is where long-term value comes from, and that a plan should assign clear owners and deadlines for every lesson learned. It also connects to what Schiesser says about executive support: without management commitment, even good lessons are never implemented.
