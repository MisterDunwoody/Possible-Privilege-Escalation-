# Possible-Privilege-Escalation

Work the incidents being generated within Azure Sentinel, in accordance with the
NIST 800-61 Incident Management Lifecycle. Make use of the provided Pl

Step 1: Preparation
(We initiated this already by ingesting all of the logs into Log Analytics Workspace and Sentinel and configuring alert rules)

Step 2: Detection & Analysis (You may have different alerts/incidents)
Set Severity, Status, Owner

![image](https://github.com/user-attachments/assets/4ae6eb22-dc07-45b7-822a-4d7725f94d4d)

View Full Details 
Observe the Activity Log (for history of incident)
Observe Entities and Incident Timelines (are they doing anything else?)
“Investigate” the incident and continue trying to determine the scope

![image](https://github.com/user-attachments/assets/da291bcc-fb97-4424-90dc-494ca35ed1c5)

Inspect the entities and see if there are any related events.
In this case the only entity is I.P address 70.125.56.206 (Which is our User I.P for testing the  enviornment)

![image](https://github.com/user-attachments/assets/299968b8-3458-45bb-b1ad-b7d8dc0a3bde)


Determine legitimacy of the incident (True Positive, False Positive, etc.)
This would be a False Positive or Benign Positive given this is an expected alarm generation.

If True Positive, continue, if False/Benign positive, close it out.

Step 3: Containment, Eradication, and Recovery

Step 4: Document Findings/Info and Clouse out the Incident in Sentinel

![image](https://github.com/user-attachments/assets/8cbd2e8b-2467-418c-b75a-17fce35a042a)


Ticket Note: Possible Privilege Escalation (Azure Key Vault Critical Credential Retrieval
or Update)
Incident ID: 11
Same user viewed critical credentials several times:
Name Christopher Dunwoody
User I.P 70.125.56.206
User Christopher Dunwoody
itsonly01_gmail.com#EXT#@itsonly01gmail.onmicrosoft.com

This user not only accessed critical credentials multiple times but was also involved in several other incidents, such as excessive password resets and global admin role assignments.

Hypothetically, after contacting the user, they woul have explained that these actions were part of their regular duties, which was confirmed by management. The case would be closed as a false positive or benign positive. 
