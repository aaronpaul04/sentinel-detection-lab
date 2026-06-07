Sentinel Detection Lab



A hands-on Microsoft Sentinel project where I build, test, and document custom threat detections from scratch.



What is this?



Microsoft Sentinel is a cloud-based SIEM (Security Information and Event Management) tool. It collects logs from across an organization (Windows machines, cloud services, firewalls, etc) and lets security teams write rules to spot attacks in real time.



This repo is a personal lab where I:



\- Write custom detection rules in \*\*KQL\*\* (Kusto Query Language, the language Sentinel uses to search logs)

\- Map each detection to the \*\*MITRE ATT\&CK framework\*\*, which is the industry-standard catalog of how real attackers operate

\- Simulate attacks in a safe environment and prove the detections actually catch them

\- Document everything with screenshots and walkthroughs so anyone can reproduce it



Repo structure:



`detections/`        -     Scheduled analytics rules that run automatically in Sentinel

`credential-access/` -     Detections for stolen passwords, token theft, etc

`execution/`         -     Detections for malicious code being run

`persistence/`       -     Detections for attackers maintaining access

`defense-evasion/`   -     Detections for attackers hiding their tracks

`lateral-movement/`  -     Detections for attackers moving between machines

`exfiltration/`      -     Detections for data being stolen

`hunting-queries/`   -     Queries for proactively searching for threats

`playbooks/`         -     Automated response actions (e.g. auto-disable a compromised user)

`deployment/`        -     Infrastructure-as-code to deploy this whole lab in one click

`docs/`              -     Walkthroughs, screenshots, and writeups



The folder names under `detections/` come straight from MITRE ATT\&CK tactics, which is the standard way SOC teams organize their detections.



How to read this repo:



Each detection lives in its own `.kql` file with a header explaining:



\- What attack it catches

\- Which ATT\&CK technique it maps to

\- What data sources it needs

\- How I tested it



If you want a tour, start in `docs/` for the full walkthroughs with screenshots.



Tech used:



\- Microsoft Sentinel (SIEM)

\- KQL (query language)

\- Azure Log Analytics

\- Atomic Red Team (for simulating attacks safely)

\- ARM / Bicep templates (for one-click deployment)



Status:



Active build. New detections added regularly.

