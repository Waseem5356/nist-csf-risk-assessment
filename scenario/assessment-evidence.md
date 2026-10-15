# Assessment Evidence (fictional)

> These findings come from a made-up interview and document review at Northbank Freight Services. They are the evidence you cite (by ID, such as F-01) when you score the CSF gap assessment and write risks in the register.

| ID | Source | Finding |
|---|---|---|
| F-01 | Microsoft 365 admin settings | Multi-factor authentication (MFA) is enforced only for the 3 global administrators. The other 137 users sign in with a password only. |
| F-02 | Password policy document | Passwords need 8 characters minimum, with no lockout after failed attempts, and expire every 90 days. |
| F-03 | Interview, IT Manager | There is no central asset inventory. Laptops are tracked in a spreadsheet updated "when someone remembers." The 30 handheld scanners are not tracked at all. |
| F-04 | System check | The warehouse management server runs Windows Server 2012 R2, which no longer receives security updates from Microsoft. The WMS vendor says an upgrade is not possible before 2028. |
| F-05 | Interview, System Administrator | Nightly backups go to a NAS on the same network as the servers, with an administrator share left mapped. Restores have never been tested. There is no offline or off-site copy. |
| F-06 | Training records | Security awareness training is one 45-minute video per year. There are no phishing simulations. IT recorded 3 incidents last year where staff entered credentials on fake sign-in pages. |
| F-07 | Interview, System Administrator | There is no central log collection or SIEM. Firewall logs are kept 7 days on the device. Microsoft 365 audit logs use default retention. |
| F-08 | Document review | The incident response plan is a 2-page document from 2021. It has never been exercised, has no defined roles, and lists a former employee as the contact. |
| F-09 | Network diagram | A partner's site-to-site VPN has had access to the warehouse network since 2019 and has never been reviewed. The network is flat, with no separation between office, warehouse and the WMS server. |
| F-10 | Sample check of devices | 60 of 85 laptops have disk encryption turned on. The 25 without it include 8 laptops used by the sales team while travelling. |
| F-11 | Warehouse walk-through | All 30 scanners share one login known to every shift worker. The warehouse Wi-Fi password has not changed since 2020 and has been given to contractors. |
| F-12 | Sample check of 20 laptops | Patching is manual, done monthly by the System Administrator. There is no reporting, and 5 of the 20 laptops checked were missing the last two monthly updates. |
| F-13 | Interview, IT Manager | There is no vendor risk process. The company uses 12 IT and software vendors, none were sent security questionnaires, and contracts were not checked for security or breach notification terms. |
| F-14 | File server review | There is no data classification. Folders with driver licenses, payroll exports and customer contracts are readable by the broad "Domain Users" group. |
| F-15 | Interview, executive team | Cyber risk is not reported to executives. No one is named as risk owner. Cyber spending is not tracked separately from general IT. |
| F-16 | Sample of 10 recent leavers | Access removal depends on HR emailing IT. 3 of the 10 accounts were still active more than 30 days after the person left. |
| F-17 | Interview, System Administrator | Microsoft Defender runs on all laptops, but its alerts go to a shared mailbox that nobody reads every day. There is no response process for alerts. |
| F-18 | Physical walk-through | The server room has a key lock, and 6 people have a key. There is no visitor log at the office. CCTV covers the warehouse dock doors only. |
| F-19 | Firewall configuration | Remote Desktop to the file server is reachable from the internet through a port forward that a previous administrator set up "temporarily" in 2023. Firewall rules have not been reviewed since 2022. |
| F-20 | Interview, Operations Director | The company has no documented recovery time or recovery point objectives. Operations can run manually for about 4 hours before shipments are delayed. |

## Notes 
- Some findings support more than one risk, and some risks rest on more than one finding. That is normal.
- Do not invent facts. If you need something this evidence does not say, record it as an assumption in your report.
- A finding is not a risk until you connect it to a threat and a business impact.
