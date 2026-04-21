# 1. SOC L1 Alert Triage
## a. Introduction
- An alerts is a core concept for any SOC team
- Understanding the concepts and lifecycle of alerts, from event generation to collect resolution
## b. Events and Alerts 
* Imagining yourself as a SOC intern, looking at the monitor of your mentor, a SOC L1 or L2 analyst, and seeing hundreds of alerts appear.
 
* Alert Management Platforms
<img width="1224" height="547" alt="image" src="https://github.com/user-attachments/assets/e4a233b5-df29-4179-b1bc-19c6f187e34d" />

* L1 Role in Alert Triage
- SOC L1 analyst: Review the alerts, distinguish bad from good, and notify L2 analyst in case of a real threat
- SOC L2 analyst: Receive the alerts escalated by L1 analysts and perform deeper analysis and remediation
- SOC engineer: Ensure the alerts contain enough information required for efficient alert triage
- SOC manager: Track speed and quality of alert triage to ensure that real attacks won't be missed

## c. Alert Properties
- While the details differ for every SIEM or security solution, the alerts have generally have a few main properties you must understand before taking them.
<img width="1494" height="484" alt="image" src="https://github.com/user-attachments/assets/e2f084dd-fcc3-4b83-8331-353adfab7bdf" />

- Alert Properties
<img width="1108" height="1154" alt="image" src="https://github.com/user-attachments/assets/8eb56be5-236c-42fd-b910-9055bbaaef76" />

## d. Picking Right Alert
- Every SOC team decides on its own prioritisation rules and usually automates them by setting the appropriate alert sorting logic in SIEM or EDR.
  1. Filter the alerts
     --> Make sure you don't take the alert that other analysts have already reviewed, or that is already being investigated by one of your teammates. You should only take news, yet unseen and unresolved alerts.
  3. Sort by severity
     --> **Start with critical alerts, then high, medium, and finally low.** This is because detection engineers design rules so that critical alerts are much more likely to be real, major threats and cause much more impact than medium or low ones.
  5. Sort by time
     --> Start with the oldest alerts and end with the newest ones. The idea is that if both alerts are about two breaches, the hacker from the older breach is likely already dumping your data, while the "newcomer" has just started the discovery.
