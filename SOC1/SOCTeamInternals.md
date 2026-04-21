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
  2. Sort by severity
     --> **Start with critical alerts, then high, medium, and finally low.** This is because detection engineers design rules so that critical alerts are much more likely to be real, major threats and cause much more impact than medium or low ones.
  3. Sort by time
     --> Start with the oldest alerts and end with the newest ones. The idea is that if both alerts are about two breaches, the hacker from the older breach is likely already dumping your data, while the "newcomer" has just started the discovery.

## e. Alert Triage
- Alert review by SOC analysts can also be called alert triage, alert processing, alert investigation, or alert analysis.
* Sticking to the **Alert Triage** 
<img width="1231" height="428" alt="image" src="https://github.com/user-attachments/assets/1c168900-390d-4461-8e46-3c9ec26c270d" />

* **Initail Actions**
  - initial strps are designed to ensure taking ownership of the assigned alert and avoid interfacing with alerts being handled by other analysts, and confirm being fully prepared to proceed with the detailed investigation.
  - Achieving it by first assigning the alert to yourself, moving it to **IN PROGRESS**, and then familliarising yourself with the alert details like its name, description, and key indicators.

* **Investigation**
  - The most complex step, requiring to apply technical knowledge and experience to understand the activity and analyse its legitimacy in SIEM or EDR logs.
    1. Understand who is under threat, like the affected user, hostname, cloud, network, or website
    2. Note the action described in the alert, like whether it was a suspicious login, malware, or phishing
    3. Review surrounding events, looking for suspicious actions shortly after or before the alert
    4. Use threat intelligence platforms or other available resources to verify your thoughts
   
* **Final Actions**
  -  Decide whether the alert is a True Positive (malicious) or False Positive (benign).
  -  Write a detailed comment explaining your analysis and reasoning. Then return to the dashboard and set the alert status to Closed.
 SOC Dashboard notes --> If you don’t get a flag, your selections are incorrect. You can reset the dashboard using the Restart button.
 
* **NOTE**:
  - Virustotal, Whois Lookup --> Look up, scan, investigate file, host, url, domain, etc..
