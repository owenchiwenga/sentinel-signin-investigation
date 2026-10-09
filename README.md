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
