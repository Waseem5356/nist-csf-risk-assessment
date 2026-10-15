# NIST CSF Risk Assessment and Risk Register

- This is my second cybersecurity project. In this project I checked the security risks of a made-up company using the NIST Cybersecurity System (CSF) 2. 0. I wrote the risks in a risk register, gave each one a score, and made a report with a plan for what to fix in the first 30, 60 and 90 days.

- I was inspired to do this project to find out what a GRC (governance, risk, and compliance) analyst has to do for their work. The main part of the role is discovering risks, assigning scores and then justifying why one should be fixed before others.

# About the data

- This company is Northbank Freight Services and it isn't a real company. I used a fictitious company profile and a list of 20 fictitious findings (F-01 to F-20) for this exercise. There is no real company or individual involved in this project.

# Results

- I scored all 22 categories of NIST CSF 2. 0. For each one I gave a current score and a target score from 0 to 4, research says.

- I identified 14 risks. 1 was Critical, 6 were High and 7 were Medium.

- If all fixes are applied, no risk remains Critical or High. 6 would be Medium and 8 would be Low.

- The lowest scoring areas were Detect and Recover. They did not monitor their alarms, and they never tried testing their backups.

- The biggest potential risk is a Remote Desktop connection that's exposed to the internet on the file server. A hacker could use this to install ransomware or exfiltrate data.

-My key suggestion is that you break that link and immediately enable multi-factor authentication (MFA) for all users within the first 30 days.

# What I learned to do

- Rank assets based on their business contribution

- Review NIST CSF 2. 0 categories and score. Identify the gaps.

- Describe a risk as: 'write in three parts a) an event b) will be caused c) by at the effect of this will be:'

- Score the risk as likelihood x impact (1-5 for each) and explain why I chose each score.

- Choose a treatment, an action and an owner for each risk.

- Compare risk (inherent) today to risk (residual) after fix.

- Translate findings into a 30/60/90 day plan and written report.

## Files in this repository
```
scenario/                   company-profile.md and assessment-evidence.md (made-up)
methodology.md              the steps, terms and scoring scales I used
risk-register.xlsx          assets, CSF gap assessment, risk register and summary
risk-assessment-report.md   my final report and action plan
```
Start by opening `risk-assessment-report`. Md first if you're short on time. You can then open `risk-register. Xlsx`. The final column in the register tab clarifies why I scored each item as I did


## Words I learned



- NIST CSF 2. 0: 6 Functions (Govern Identify Protect Detect Respond, Recover). What are the Funtions? The six primary Functions are broken down into a total of 22 categories.

- Risk: something unfortunate that might happen to a company due to a vulnerability.

- Probability and consequence: the risk's probability and severity. Both of these are given a score of between 1 and 5.

- Inherent risk and residual risk: the risk now, and the risk after the fix.

- What you do about a risk: lessen it, accept it, transfer it (for example with insurance), or avoid it.

- A risk register: a table that contains each risk, each rating, each owner and what you are doing about fixing it.


## Tools I used
- Microsoft Excel
- Visual Studio Code

## Limits of this project
- The company and the findings are made up, so I did not talk to anyone or look at a real company.
- The scores are my personal opinion. Perhaps someone else would score some of the risks differently.
- The dollar values used on the impact scale are a hypothetical estimate on my part.
- The 0 to 4 maturity scale is a simple one that I used. NIST CSF 2. 0 does not give scores for each category.

## Author
Waseem Akram Shaik | MS in Management Information Systems, University of Memphis
