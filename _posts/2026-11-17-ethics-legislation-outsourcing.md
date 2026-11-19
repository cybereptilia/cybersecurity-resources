---
layout: post
title: "Ethics, Legislation, and Outsourcing in IT"
date: 2026-11-17 09:00:00 -0400
categories: [ethics, legislation, outsourcing]
---

Technical skill is only part of working in IT and cybersecurity. Professionals also handle other people's data, sign off on systems that produce financial reports, and decide which work to hand to outside companies. This post explains three connected topics: **ethics**, the **laws** that grew out of ethical failures, and **outsourcing**, which many companies consider partly because of those laws.

## Part 1: Ethics

### Personal ethics and business ethics

**Personal ethics** are the values that guide how a person behaves in private life, such as honesty, trust, and responsibility. They usually form early in life. **Business ethics** are the values that guide how a person behaves at work.

The difference is mostly about **scale**. If someone lies to a friend, a few people are hurt. If a chief financial officer hides losses from investors, thousands of employees, shareholders, and pensioners can be hurt.

**Example:** an IT administrator who reads a coworker's email out of curiosity breaks personal trust. An administrator who sells customer records to a marketing firm breaks business ethics, and probably the law, and affects every customer in the database.

### When business ethics fail: the early-2000s scandals

In *IT Systems Management*, Schiesser uses several corporate scandals from the early 2000s to show what happens when executives abandon business ethics:

- **Enron:** an energy company that hid debt and losses in offshore partnerships. It collapsed in 2001, its executives were convicted, and its auditor, Arthur Andersen, lost nearly all its clients. Thousands of employees lost their retirement savings.
- **WorldCom:** hid its declining finances with fraudulent accounting until internal auditors found about $3.8 billion in improper entries in 2002. It filed the largest bankruptcy in U.S. history at that time, and its CEO received a 25-year sentence.
- **Tyco:** its CEO and CFO were convicted of stealing more than $150 million from the company.

These cases matter to IT because the fraud ran through financial systems. The response from lawmakers placed new responsibilities directly on the people who build and run those systems.

### Ethics codes for cybersecurity professionals

Cybersecurity professionals have their own codes of conduct. The best known is the **ISC2 Code of Ethics**, which every holder of an ISC2 certification (such as the CISSP) must follow. Its four canons are:

1. Protect society, the common good, necessary public trust and confidence, and the infrastructure.
2. Act honorably, honestly, justly, responsibly, and legally.
3. Provide diligent and competent service to principals.
4. Advance and protect the profession.

**Example:** a penetration tester who discovers a serious vulnerability in a client's system should report it to the client promptly and confidentially (canons 2 and 3), not publish it online for attention or keep exploring systems outside the agreed scope.

## Part 2: Legislation

### Sarbanes-Oxley Act (SOX), 2002

SOX was the main U.S. response to the scandals. It applies to publicly traded companies and requires stronger controls over financial reporting.

- **Section 302:** the CEO and CFO must personally certify that financial reports are accurate and that internal controls exist and have been evaluated.
- **Section 404:** management must report each year on how effective those internal controls are, and outside auditors must assess them.

**Why IT cares:** financial reports come out of IT systems such as ERP platforms and databases. Access controls, change management, audit logs, and backups therefore become part of SOX compliance. **Example:** if any developer can change the accounting database directly in production with no approval and no log, auditors will flag it as a control weakness.

### Gramm-Leach-Bliley Act (GLBA), 1999

The GLBA regulates how financial institutions handle customers' **non-public personal information (NPI)**, such as account numbers and Social Security numbers. Institutions must explain their privacy practices and let customers **opt out** of having their information shared with unaffiliated companies.

The law keeps evolving. The Federal Trade Commission's **Safeguards Rule**, issued under the GLBA, now requires covered non-bank financial institutions (such as mortgage lenders and finance companies) to notify the FTC **within 30 days** of discovering that unencrypted customer information involving **at least 500 consumers** was acquired without authorization. That requirement took effect on **May 13, 2024**.

### California SB 1386 and state breach-notification laws

**California Senate Bill 1386**, enacted in 2002, was the first state law requiring organizations to notify people when their computerized personal information is exposed in a security breach. It became a model for the rest of the country: **all 50 states**, the District of Columbia, Guam, Puerto Rico, and the U.S. Virgin Islands now have breach-notification laws, with Alabama and South Dakota the last states to adopt one, in 2018.

**Puerto Rico's own law** is the *Citizen Information on Data Banks Security Act* (Law 111 of September 7, 2005, effective January 5, 2006, and later amended). It requires organizations that own or hold databases with personal information of Puerto Rico residents to notify those residents when unprotected personal information is exposed in a breach.

### SEC cybersecurity disclosure rules, 2023

A newer rule extends the idea of SOX to cybersecurity. Since December 18, 2023, public companies must disclose a **material cybersecurity incident** on SEC Form 8-K (Item 1.05) **within four business days** of determining that the incident is material, and they must describe their cybersecurity risk management and governance in their annual reports.

**Example:** if ransomware shuts down a public company's manufacturing plants for a week, the company must decide quickly whether the incident is material and, if it is, report it publicly within four business days.

## Part 3: Outsourcing

**Outsourcing** means contracting an outside company to perform IT functions: running data centers, staffing the service desk, developing software, or monitoring security around the clock. Schiesser notes that the growing accountability placed on executives by laws like SOX is one reason many companies consider it.

### Advantages

- **Cost savings**, especially when work moves to lower-cost regions.
- **Scalability:** capacity grows or shrinks without hiring or layoffs.
- **Expertise:** specialized providers bring skills and tools a company may not have, such as a 24/7 security operations center.
- **Focus:** internal staff can concentrate on work that differentiates the business.

### Disadvantages

- **Loss of control** over priorities, quality, and how work is done.
- **The cost of managing the contract**, which can reduce the expected savings.
- **Conflicting priorities:** the provider serves many clients.
- **Time zones, language, and cultural differences** that slow communication.
- **Third-party risk:** the provider becomes a path into the company's systems and data.

### Responsibility cannot be outsourced

The most important point is that **a company can outsource work, but not accountability**. If a provider loses customer data, the company that collected the data still has to meet its breach-notification obligations, and under the SEC rules a serious incident at a third-party service provider can still require disclosure by the public company that relies on it. That is why many organizations now evaluate a provider's **security controls and regulatory compliance** before signing, and keep auditing them afterward.

**Example:** a hospital outsources its billing to a processing company. If the processor is breached, the hospital must still notify affected patients under the applicable laws, so its contract should require the processor to report incidents immediately, encrypt patient data, and allow security audits.

## Key takeaways

- **Business ethics** failures harm far more people than personal ones, and they led directly to new laws.
- **SOX, the GLBA, state breach laws (including Puerto Rico's Law 111), and the SEC rules** all place responsibilities on IT systems and the people who run them.
- **Outsourcing** can save money and add expertise, but responsibility for data and compliance stays with the company.

### Sources

- ISC2. *Code of Ethics*. <https://www.isc2.org/ethics>
- Federal Register (Nov. 13, 2023). *Standards for Safeguarding Customer Information* (FTC Safeguards Rule amendment). <https://www.govinfo.gov/content/pkg/FR-2023-11-13/html/2023-24412.htm>
- Jackson Lewis. *State Data Breach Notification Laws: Overview of the Patchwork*. <https://www.jacksonlewis.com/insights/state-data-breach-notification-laws-overview-patchwork>
- Davis Wright Tremaine. *Summary of U.S. State Data Breach Notification Statutes*. <https://dwt.com/statedatabreachstatutes>
- Jones Day (2023). *SEC Adopts Rules on Cybersecurity Risk Management, Strategy, Governance, and Incident Disclosure*. <https://jonesday.com/de/insights/2023/08/sec-adopts-rules-on-cybersecurity-risk-management>
- Schiesser, R. (2010). *IT Systems Management* (2nd ed.). Prentice Hall. Chapter 5.
