# Sentinel Sign-in Investigation

## Project Overview
This project demonstrates how Kusto Query Language (KQL) can be used to investigate failed sign-in activity in Microsoft Sentinel.

## Objective
Identify patterns of repeated failed sign-ins that may indicate password guessing or password spraying.

## Tools and Technologies
- Microsoft Sentinel
- Microsoft Entra ID sign-in logs
- Kusto Query Language (KQL)
- GitHub

## Investigation Approach
1. Review sign-in events from the last 24 hours.
2. Filter unsuccessful sign-in attempts.
3. Group failures by source IP address and user account.
4. Flag IP addresses with repeated failures for further investigation.
5. Review related activity before deciding whether an incident is suspicious.

## Important Note
A high number of failed sign-ins does not automatically prove an attack. Findings must be validated using available logs and organizational context.

## Project Status
This repository contains example investigation queries and documentation. Live execution and results will be documented only after testing in an appropriate environment.

## Skills Demonstrated
- KQL query development
- Authentication log analysis
- Suspicious sign-in investigation
- Security incident documentation

## Disclaimer
This project is for educational purposes. No real security incident or attack is claimed.
## Screenshots

### 1. Failed Sign-in Query
![Failed sign-in query](screenshots/01-failed-signin-query.png)

### 2. Repeated Failures by IP
![Repeated failures by IP](screenshots/02-repeated-failures-by-ip.png)

### 3. Successful Sign-in Investigation
![Successful sign-in investigation](screenshots/03-successful-signin-investigation.png)

### 4. Investigation Report
![Investigation report](screenshots/04-investigation-report.png)

### 5. GitHub Project Overview
![GitHub project overview](screenshots/05-github-project-overview.png)
