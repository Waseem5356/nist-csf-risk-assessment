# Cybersecurity Risk Assessment Report: Northbank Freight Services (fictional)

**Analyst:** Waseem Akram Shaik
**Report date:** 2026-10-15
**Framework:** NIST Cybersecurity Framework 2.0
**Status:** Complete

> Northbank Freight Services is a fictional company created for a training exercise. The findings are made up, and the work shows my assessment method.

## 1. Executive summary
I scored Northbank Freight Services on all 22 categories of NIST CSF 2. 0 on 20 evidence findings, and identified and entered 14 risks into a risk register (1 Critical, 6 High, 7 Medium). The company most severely gaps in the Detect and Recover functions; it can't see an attack, and has never tested whether it would be able to recover. The most important risk is a Remote Desktop service exposed to the internet on its file server, risking ransomware or driver and payroll data theft. My recommend actions would close this risk and require multi-factor authentication for all users within 30 days and meet the January 2027 cyber insurance renewal deadline. This would leave no Critical or High risks, and 8 of the 14 remaining Low.



## 2. Scope and method
**Scope:** the systems, data and people described in `scenario/company-profile.md`: Microsoft 365, the cloud transport system, the on-premises warehouse server, file server, backup device, network, laptops, scanners, the partner VPN and the payroll provider.

**Method** (see `methodology.md`):
1. Read the company profile and the 20 evidence findings (F-01 to F-20).
2. Rated 14 assets for business criticality (1 to 5).
3. Scored current and target maturity (0 to 4) for all 22 CSF categories, citing evidence IDs.
4. Wrote 14 risks as cause, event and impact, linked to evidence, assets and a CSF category.
5. Scored each risk by likelihood (1 to 5) and impact (1 to 5). Score = likelihood x impact. Ratings: Low 1 to 5, Medium 6 to 11, High 12 to 19, Critical 20 to 25.
6. Chose a treatment, a recommended action and an owner role for each risk, then re-scored it as it would be after the action (residual).

All data and the scoring scales are in `risk-register.xlsx`.

## 3. CSF gap assessment
The average gap (target minus current maturity) is 1.7 across the 22 categories. Detect and Recover have the largest gaps at 2.0 each, because current maturity there is only 0.5 on average. Respond has the smallest gap at 1.3.

| Function | Average current | Average target | Average gap |
|---|---|---|---|
| Govern | 1.2 | 2.8 | 1.7 |
| Identify | 1.0 | 2.7 | 1.7 |
| Protect | 1.2 | 3.0 | 1.8 |
| Detect | 0.5 | 2.5 | 2.0 |
| Respond | 1.0 | 2.3 | 1.3 |
| Recover | 0.5 | 2.5 | 2.0 |

| Category | Current | Target | Gap | Evidence |
|---|---|---|---|---|
| GV.OC Organizational Context | 2 | 3 | 1 | F-15 |
| GV.RM Risk Management Strategy | 1 | 3 | 2 | F-15 |
| GV.RR Roles, Responsibilities, and Authorities | 1 | 3 | 2 | F-15, F-08 |
| GV.PO Policy | 2 | 3 | 1 | F-02, F-08 |
| GV.OV Oversight | 0 | 2 | 2 | F-15 |
| GV.SC Cybersecurity Supply Chain Risk Management | 1 | 3 | 2 | F-13, F-09 |
| ID.AM Asset Management | 1 | 3 | 2 | F-03 |
| ID.RA Risk Assessment | 1 | 3 | 2 | F-04, F-15 |
| ID.IM Improvement | 1 | 2 | 1 | F-08 |
| PR.AA Identity Management, Authentication, and Access Control | 1 | 3 | 2 | F-01, F-02, F-11, F-16, F-19 |
| PR.AT Awareness and Training | 2 | 3 | 1 | F-06 |
| PR.DS Data Security | 1 | 3 | 2 | F-10, F-14, F-05 |
| PR.PS Platform Security | 1 | 3 | 2 | F-04, F-12, F-17 |
| PR.IR Technology Infrastructure Resilience | 1 | 3 | 2 | F-09, F-05, F-19 |
| DE.CM Continuous Monitoring | 1 | 3 | 2 | F-07, F-17 |
| DE.AE Adverse Event Analysis | 0 | 2 | 2 | F-07, F-17 |
| RS.MA Incident Management | 1 | 3 | 2 | F-08 |
| RS.AN Incident Analysis | 1 | 2 | 1 | F-06, F-07 |
| RS.CO Incident Response Reporting and Communication | 1 | 2 | 1 | F-08 |
| RS.MI Incident Mitigation | 1 | 2 | 1 | F-17 |
| RC.RP Incident Recovery Plan Execution | 1 | 3 | 2 | F-05, F-20 |
| RC.CO Incident Recovery Communication | 0 | 2 | 2 | None provided |

Maturity scale: 0 not in place, 1 ad hoc, 2 partial, 3 defined, 4 managed. This is a simple scale I used, because CSF 2.0 does not prescribe scores for each category. Targets are 3 where a gap drives a top risk, and 2 where a small company would not run a heavy process.

## 4. Risk results
| Rating | Inherent (today) | Residual (after actions) |
|---|---|---|
| Critical | 1 | 0 |
| High | 6 | 0 |
| Medium | 7 | 6 |
| Low | 0 | 8 |
| Total | 14 | 14 |

Risks by CSF Function: Protect 8, Govern 3, Detect 1, Respond 1, Recover 1.

Top five risks, ranked by score, with ties broken by impact and then by the size of the CSF gap behind them:

| Rank | ID | Risk | Score | Rating | Treatment |
|---|---|---|---|---|---|
| 1 | R-01 | Internet-exposed Remote Desktop leads to ransomware | 20 | Critical | Mitigate |
| 2 | R-03 | Email accounts taken over because MFA is missing | 16 | High | Mitigate |
| 3 | R-04 | Backups unusable when needed | 15 | High | Mitigate |
| 4 | R-02 | Unsupported warehouse server fails or is compromised | 12 | High | Mitigate |
| 5 | R-07 | An attack goes unnoticed (no logging or alert review) | 12 | High | Mitigate |

R-05 (departed staff and shared logins) and R-14 (no leadership oversight) also score 12 and are High, and they are in the 60-day plan.

## 5. Top risks in detail

**R-01: Internet-exposed Remote Desktop leads to ransomware (score 20, Critical).** Remote Desktop to the file server is reachable from the internet through a port forward set up "temporarily" in 2023 (F-19). Passwords are weak and accounts are never locked (F-02), and backups sit on the same network (F-05). An attacker could guess or buy a password, then encrypt or steal the file server data, including driver licenses, payroll exports and customer contracts (F-14). I scored likelihood 4 because internet-facing Remote Desktop is scanned constantly and nothing slows an attacker down, and impact 5 because the data, contracts and backups are all in reach and the flat network (F-09) could let it spread. The action is to close the port forward immediately, require a VPN with MFA for remote access, set lockout and review the firewall rules. Residual risk is 8 (Medium), because impact stays high until backups are fixed under R-04.

**R-03: Email accounts taken over because MFA is missing (score 16, High).** MFA covers only 3 of 140 users (F-01), and staff entered credentials on fake pages three times last year (F-06). A phished password would open an account, enabling fraudulent payment requests and exposure of customer data. Likelihood 4 reflects that this has already happened. Impact 4 reflects a possible loss above $250,000 under the assumed scale. Enforcing MFA for all users lowers likelihood to 2 and impact to 3 (residual 6), and it is also a stated requirement of the January 2027 insurance renewal.

**R-04: Backups unusable when needed (score 15, High).** Backups go to a device on the same network with an administrator share mapped, restores have never been tested and there is no offline copy (F-05). The company also has no recovery time or recovery point targets (F-20). Ransomware or a hardware failure could destroy the backups, and recovery could take over a week. I scored likelihood 3 and impact 5. The fix is an offline or immutable copy, removal of the mapped share and a quarterly restore test, which brings the residual score to 6.

**R-02: Unsupported warehouse server fails or is compromised (score 12, High).** The warehouse management server runs Windows Server 2012 R2 with no security updates, and the vendor cannot upgrade it before 2028 (F-04). It is on a flat network reachable from a partner VPN (F-09), and operations can work manually for only about 4 hours (F-20). Likelihood is 3 because it is exposed internally rather than to the internet, and impact is 4 because the warehouse is the core of the business. The action is to isolate the server in its own network segment, limit VPN access, test a restore and plan the migration before 2028. Residual risk is 8 until the migration is done.

**R-07: An attack goes unnoticed (score 12, High).** Firewall logs are kept for 7 days, nothing is centrally collected (F-07) and Defender alerts go to a mailbox nobody reads daily (F-17). An intruder could stay inside for weeks, and there would be no evidence for an investigation or an insurance claim. This risk raises the cost of every other event. The action is to assign alert review to named people, extend log retention to at least 90 days and evaluate a low-cost central logging or managed monitoring service.

## 6. Action plan
Priorities in the register put Critical risks first (30 days) and High risks within 60 days. I moved some quick, low-cost High-risk fixes into the first 30 days, because they are inexpensive and reduce more than one risk.

| Timeframe | Actions | Risks addressed | Owner (role) |
|---|---|---|---|
| Next 30 days | Close the Remote Desktop port forward; enforce MFA for all Microsoft 365 users; remove the mapped admin share on the backup device; disable accounts of leavers and set a leaver checklist; name an executive risk owner; assign review of Defender alerts | R-01, R-03, R-04, R-05, R-14, R-07 | IT Manager, System Administrator, HR Manager, executive team |
| 31 to 60 days | Add an offline or immutable backup copy and run a restore test; require VPN with MFA for remote access; isolate the warehouse server; give each scanner user an individual login and change the Wi-Fi password; extend log retention to 90 days; encrypt the 8 travelling sales laptops | R-04, R-01, R-02, R-05, R-07, R-09 | IT Manager, System Administrator, Warehouse Manager |
| 61 to 90 days | Update the incident response plan and run a tabletop exercise; restrict sensitive folders and classify data; automate laptop patching and report compliance; send security questionnaires to the top vendors; limit server room keys and add a visitor log; review and limit the partner VPN | R-08, R-10, R-11, R-12, R-13, R-06 | IT Manager, System Administrator, Facilities Manager |
| Longer term | Migrate the warehouse server off the unsupported system before 2028; evaluate central logging or managed monitoring; review this register every quarter | R-02, R-07, all | IT Manager, executive team |

## 7. Residual risk
If the actions are completed, no risks remain Critical or High: 6 are Medium and 8 are Low. The highest remaining scores are R-01 and R-02 at 8. R-02 stays at 8 until the warehouse server is migrated, because the vendor limits what can be done earlier. The company would still carry the risk of a determined attacker and of failures in systems it does not control, such as the cloud transport system and the payroll provider. Leadership should accept those consciously and review them each quarter.

## 8. Lessons learned
- Risks are connected. The impact of R-01 stays high until the backup problem in R-04 is fixed, so fixing one risk can lower another.
- Some of the highest risks are cheap to fix. Closing one port forward and turning on MFA cost little compared with the harm they prevent.
- A score needs a reason. Writing why I chose each likelihood and impact from the evidence made me change several scores that first felt arbitrary.
- A gap assessment and a risk register answer different questions. The gap assessment shows where the company is weak across the framework, and the register shows what could actually go wrong and how badly.
- Targets should be realistic. A 140-person company with a two-person IT team should aim for "defined" in key areas, not "managed" everywhere.

## 9. Limitations
- The company and all findings are fictional, so no real organization was assessed and no one was interviewed.
- Scores are qualitative and based on my judgement, and another analyst could score some risks differently.
- Dollar ranges in the impact scale are assumptions for this scenario.
- Where the evidence said nothing (for example recovery communication), I scored the category 0 and noted "none provided."
- The maturity scale is my own simple scale, because CSF 2.0 does not prescribe scores for each category.
