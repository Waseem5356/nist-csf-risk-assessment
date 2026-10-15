# Methodology

This assessment follows a simple qualitative approach. It is a learning exercise, so scores come from analyst judgement and the evidence provided, not from statistics.

## Framework
NIST Cybersecurity Framework (CSF) 2.0 has six Functions: **Govern, Identify, Protect, Detect, Respond, Recover**. Each Function has Categories (22 in total). I scored the organization against all 22 categories, then recorded risks and mapped each risk to the category that best fits.

## Steps
1. Read the company profile and the assessment evidence.
2. List the assets and rate how critical each one is to the business (1 to 5).
3. Score current and target maturity (0 to 4) for each of the 22 CSF categories, citing evidence IDs.
4. Write risks as a statement of cause, event and impact, and link each to evidence, assets and a CSF category.
5. Score each risk by likelihood (1 to 5) and impact (1 to 5). Score = likelihood x impact.
6. Choose a treatment (mitigate, accept, transfer or avoid), a recommended action and an owner role.
7. Re-score the risk as it would be after the action (residual risk).
8. Summarize results and build a 30/60/90-day action plan.

## Key terms
- **Asset:** anything of value to the business, such as a system, data or a person's access.
- **Threat:** something that could cause harm, such as a phishing attacker or a failed server.
- **Vulnerability:** a weakness that a threat could use, such as no MFA.
- **Risk:** the chance that a threat uses a vulnerability and harms the business. Written as cause, event and impact.
- **Likelihood and impact:** how probable the event is and how bad the worst realistic result would be.
- **Inherent risk:** the risk as it stands today, with existing controls.
- **Residual risk:** the risk expected after the recommended action is done.
- **Treatment:** mitigate (reduce), accept (live with it), transfer (insure or outsource) or avoid (stop the activity).

## Scales and thresholds
Likelihood, impact, rating thresholds and the maturity scale are defined on the `Scoring Method` sheet of `risk-register.xlsx`. The thresholds are common choices for a 5x5 matrix and are not a NIST requirement. The maturity scale (0 to 4) is a simple scale I used for this exercise, because CSF 2.0 does not prescribe scores for each category.

## Limits
- Scores are qualitative and could differ between analysts.
- The company, its systems and the findings are fictional, so no real organization was assessed.
- Dollar ranges in the impact scale are assumptions for this scenario.
