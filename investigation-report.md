# Failed Sign-in Investigation Report

## 1. Objective
Investigate failed Microsoft Entra ID sign-in events and identify patterns that may warrant further security review.

## 2. Data Source
The example queries use the Microsoft Sentinel SigninLogs table.

## 3. Query 1: Failed Sign-ins by User and IP
The first query reviews the last 24 hours of sign-in logs, filters unsuccessful attempts, and groups failures by user account and source IP address.

Purpose:
- Identify accounts with repeated authentication failures.
- Identify source IP addresses associated with those failures.
- Prioritize combinations with the highest failure counts.

## 4. Query 2: Repeated Failures by IP
The second query summarizes failed sign-ins by IP address and estimates the number of distinct accounts involved. It flags IP addresses with at least 10 failures.

Purpose:
- Identify sources generating repeated failures.
- Look for patterns that may be consistent with password guessing or password spraying.
- Prioritize results for further investigation.

## 5. Analyst Validation Steps
For any suspicious results:
1. Review timestamps and sign-in status details.
2. Examine targeted accounts and source IP reputation where approved tools are available.
3. Check locations, device details, authentication methods, and Conditional Access results.
4. Correlate with other relevant alerts and sign-in activity.
5. Escalate according to the organization's incident response process if evidence supports it.

## 6. Important Limitations
A high failure count does not prove malicious activity. Legitimate users, misconfigured applications, and expired credentials can also cause failures. The threshold of 10 is an illustrative starting point and should be tuned to the environment.

## 7. Results and Status
These queries and steps are documented as a portfolio exercise. They have not been validated against live Microsoft Sentinel data, and no real incident or attack is claimed.

## 8. Skills Demonstrated
- KQL query writing
- Authentication log analysis
- Detection triage and investigation
- Security documentation and incident response reasoning
