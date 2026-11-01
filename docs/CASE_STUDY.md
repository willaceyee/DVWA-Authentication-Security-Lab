# Authentication assessment case study

## Objective

Evaluate whether the DVWA Brute Force module in the assignment lab restricted repeated login attempts, and document how responses distinguished an unsuccessful attempt from a successful one.

## Environment and scope

The supplied group report records an Ubuntu virtual machine, Docker, DVWA, a browser, and Burp Suite Intruder. Its local DVWA target used port 8080 and the reviewed brute-force screenshots show the Low security level. The Docker version evidence shows 28.2.2. These are historical observations, not a currently deployed public service.

The portfolio covers Willace Yee's full Part 1 environment setup and brute-force login assessment. Based on his clarification of the work performed, the setup includes Ubuntu, Docker, DVWA, the web server, networking, Burp/proxy configuration, and system verification. Other members' vulnerability assessments remain distinguished from this work.

## Recorded method

1. Prepare the Ubuntu/Docker operating environment and confirm that the training application is available locally.
2. Open the DVWA Brute Force module using a lab account and the intended training security level.
3. Observe a failed login response and establish what the application displays when authentication fails.
4. In the recorded Burp Intruder assessment, vary the password parameter using a small training payload list while keeping the other request conditions consistent.
5. Compare responses, then inspect the candidate successful result to confirm that protected-area content was returned.
6. Document the observed controls, account-takeover implications, and recommended remediation.

This describes the reported workflow. It is not a script for targeting an arbitrary host and no new password-guessing run was performed for this repository.

## Observations and interpretation

| Evidence | Observation | What it supports |
| --- | --- | --- |
| Report Figure 60 | The module displays an unsuccessful login message | Baseline failure behavior in the training module |
| Report Figures 64–68 | The gallery shows password-parameter variation and response comparison in Burp | The recorded assessment method; visible cookie headers are redacted and raw session exports are excluded |
| Report Figure 69 | The module displays its protected-area welcome message | A successful lab credential match |
| Report narrative | Successive attempts were processed without observed delay or lockout | No effective throttling or lockout was demonstrated during the sampled sequence |

Response-length variation by itself does not establish successful authentication. The protected response provides the stronger confirmation. Likewise, a finite sequence without a lockout does not prove that no threshold exists under any circumstances.

## Impact

In a real application, weak or reused credentials combined with inadequate login throttling can make account compromise more likely. This lab demonstrates the authentication failure mode; it does not show compromise of a real organization, exposure of production credentials, or a measured attack success rate.

## Recommendations and limits

Apply server-side throttling and progressive delays, detect repeated failures, consider MFA, and use carefully designed temporary lockout. Generic failure messages help reduce account enumeration, but do not substitute for throttling. See [remediation verification](REMEDIATION.md).

The original report includes a broader risk-scoring discussion. No numerical severity score is independently recalculated or certified in this portfolio. Recommendations have not been implemented in a patched application, so no remediation-success claim is made.

## Evidence provenance

The [evidence register](EVIDENCE.md) maps each included image to its figure in the supplied report. No new screenshots, scanner outputs, or test results have been invented.
