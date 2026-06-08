# servicenow-developer-portfolio
A complete ServiceNow Developer portfolio showcasing ITSM projects, automation workflows, CMDB configurations, and real-world enterprise scenarios. Includes incident, change, and service catalog implementations with documentation and screenshots.

📖 Project Overview
This project simulates a real-world ServiceNow Major Incident Management solution for critical infrastructure environments such as Etihad Rail operations and Abu Dhabi Airport systems.

The solution focuses on handling P1 incidents affecting train control systems, baggage handling systems, and operational IT services using ITIL-based processes and ServiceNow ITSM modules.
🎯 Objective

The main objective of this project is to:

- Detect and manage critical P1/P2 incidents in real time
- Ensure fast escalation to NOC and control room teams
- Automate Major Incident workflows using Flow Designer
- Improve communication between technical and business teams
- Reduce downtime in critical transport operations
- 🏗️ Real-Life Scenario
- 
- ### Etihad Rail Scenario
A failure occurs in the train signaling system between stations causing service disruption.

### Airport Scenario
A baggage handling system failure occurs during peak passenger hours, impacting flight operations.

Both incidents are classified as Major Incidents (P1) requiring immediate escalation and coordination.

⚙️ Features Implemented

- Major Incident auto-identification (P1 trigger logic)
- Automatic assignment to NOC / Control Room group
- Stakeholder notification (Email & Alerts)
- War room / bridge communication setup
- SLA tracking and escalation rules
- Incident linking (child incidents under major incident)
- Post-incident review (PIR) process
- 
- 🧰 Technologies Used
- 
- - ServiceNow ITSM Module
- Major Incident Management Plugin
- Flow Designer
- Business Rules
- Assignment Rules
- Notifications
- SLA Engine
- Client Scripts
- 
🔄 Workflow Process
1. Incident is created in ServiceNow
2. System checks priority conditions
3. If P1 → Major Incident is triggered automatically
4. Incident assigned to NOC / Control Room team
5. War room communication initiated
6. Stakeholders are notified immediately
7. Resolution team investigates and fixes issue
8. Incident closed with PIR documentation

🏢 Assignment Groups Used
- Airport NOC Team
- Rail Control Room Team
- IT Infrastructure Support
- Application Support Team

  🧠 Business Rule Example
  // Auto-trigger Major Incident for P1 cases

if (current.priority == 1) {
    current.major_incident_state = "Accepted";
    current.assignment_group = "NOC Team";
    gs.addInfoMessage("Major Incident triggered automatically");
}
🔔 Flow Designer Automation
Flow triggers when:
- Incident priority = 1

Actions:
- Create Major Incident record
- Assign to Control Room group
- Send email notifications to stakeholders
- Start SLA timer

  📊 Benefits Achieved
  - Faster response to critical system failures
- Reduced manual escalation steps
- Improved coordination between IT teams
- Better SLA compliance for critical operations
- Structured Major Incident handling process
  
  🖼️ Screenshots
  ### Incident Creation
![Incident](images/incident.png)

### Major Incident Dashboard
![Dashboard](images/dashboard.png)

### Flow Designer Workflow
![Flow](images/flow.png)

📌 Real Business Impact
This solution is designed for high-impact environments such as:

- ✈️ Airports (baggage systems, flight operations)
- 🚆 Railways (train control, signaling systems)
- 🏢 Government infrastructure services

It ensures minimal downtime and faster recovery for mission-critical services.

🚀 How to Use
1. Activate ITSM and Major Incident plugins
2. Configure assignment groups (NOC, Control Room)
3. Import Flow Designer workflows
4. Set priority rules for P1 incidents
5. Test using sample incident records

👨‍💻 Author
Name: Chinchu S Pillai 
Role: ServiceNow Developer  
Location: Abu Dhabi, UAE  
Focus: ITSM, Flow Designer, Automation, Major Incident Management  
LinkedIn: www.linkedin.com/in/chinchu-s-pillai-engineer

📜 License
This project is created for portfolio and learning purposes only.
