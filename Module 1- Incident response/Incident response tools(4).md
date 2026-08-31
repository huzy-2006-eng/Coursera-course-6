Tool types-
1. Detection and management tools.
2. Documentation tools.
3. Investigative tools.

Types of documentation-
1. Playbooks
2. Incident handler's journals
3. Policies
4. Plans
5. Final reports

Playbook-
A manual that provides details about any operational action.

Word processor tools-
1. Google Docs
2. Notepad++

Jira

Other tools-
1. Google Sheets
2. Audio recorders
3. Cameras

#  Intrusion detection system(IDS)-
An application that monitors system and network activity and produces alerts on possible intrusions. An IDS does not stop or prevent the activity. Instead, security professionals will investigate the alert and act to stop it, if necessary. 

4 types of detection categories:
1. **A true positive** is an alert that correctly detects the presence of an attack.
2. **A true negative** is a state where there is no detection of malicious activity. This is when no malicious activity exists and no alert is triggered.
3. **A false positive** is an alert that incorrectly detects the presence of a threat. This is when an IDS identifies an activity as malicious, but it isn't. False positives are an inconvenience for security teams because they spend time and resources investigating an illegitimate alert.
4. **A false negative** is a state where the presence of a threat is not detected. False negatives are dangerous because security teams are left unaware because security teams are left unaware of legitimate attacks that they can be vulnerable to.


# Intrusion Prevention System(IPS)-
An application that monitors system activity for intrusions and take action to stop the activity.

# EDR (Endpoint detection and response)-
1. Endpoint detection and response (EDR) is an application that monitors an endpoint for malicious activity. EDR tools are installed on endpoints. Remember that an endpoint is any device connected on a network. Examples include end-user devices, like computers, phones, tablets, and more.

2. EDR tools monitor, record, and analyze endpoint system activity to identify, alert, and respond to suspicious activity. Unlike IDS or IPS tools, EDRs collect endpoint activity data and perform behavioral analysis to identify threat patterns happening on an endpoint. Behavioral analysis uses the power of machine learning and artificial intelligence to analyze system behavior to identify malicious or unusual activity. EDR tools also use automation to stop attacks without the manual intervention of security professionals. For example, if an EDR detects an unusual process starting up on a user’s workstation that normally is not used, it can automatically block the process from running.

Tools-
1. Open EDR
2. Bitedefender
3. FortiEDR


IDS and IPS tools-
1. Snort
2. Zeek
3. Kismet
4. Sagan
5. Suricata

# SIEM process:
1. #### Collect and aggregate data-
SIEM tools require data for them to be effectively used. During the first step, the SIEM collects event data from various sources like firewalls, servers, routers, and more. This data, also known as logs, contains event details like timestamps, IP addresses, and more.

 Logs are a record of events that occur within an organization’s systems. After all of this log data is collected, it gets aggregated in one location. Aggregation refers to the process of consolidating log data into a centralized place. 

 Through collection and aggregation, SIEM tools eliminate the need for manually reviewing and analyzing event data by accessing individual data sources. Instead, all event data is accessible in one location—the SIEM. 

Parsing can occur during the first step of the SIEM process when data is collected and aggregated. Parsing maps data according to their fields and their corresponding values. For example, the following log example contains fields with values. At first, it might be difficult to interpret information from this log based on its format:

April 3 11:01:21 server sshd[1088]: Failed password for user nuhara from 218.124.14.105 port 5023

In a parsed format, the fields and values are extracted and paired making them easier to read and interpret:

host = server

process = sshd

source_user = nuhara

source ip = 218.124.14.105

source port = 5023

2. #### Normalize data-
SIEM tools collect data from many different sources. This data must be transformed into a single format so that it can be easily processed by the SIEM. However, each data source is different and data can be formatted in many different ways. For example, a firewall log can be formatted differently than a server log.

A SIEM solution ingests raw data and normalizes it into structured data.
Collected event data should go through the process of normalization. Normalization converts data into a standard, structured format that is easily searchable. 


3. #### Analyze data-
After log data has been collected, aggregated, and normalized, the SIEM must do something useful with all of the data to enable security teams to investigate threats. During this final step in the process, SIEM tools analyze the data. Analysis can be done with some type of detection logic such as a set of rules and conditions. SIEM tools then apply these rules to the data, and if any of the log activity matches a rule, alerts are sent out to cybersecurity teams.

#### SIEM TOOLS-
AlienVault® OSSIM™

Chronicle

Elastic

Exabeam

IBM QRadar® Security Intelligence Platform

LogRhythm

Splunk


#### Security Orchestration, automation, and response(SOAR):
A collection of applications, tools and workflows that uses automation to respond to security events.

# Advantages of SIEM tools:
1. **Access to event data:** SIEM tools provide access to the event and activity data that happens on a network, including real-time activity. Networks can be connected to hundreds of different systems and devices. SIEM tools have the ability to ingest all of this data so that it can be accessed.

2. **Monitoring,detecting and alerting:** SIEM tools continuously monitor systems and networks in real-time. They then analyze the collected data using detection rules to detect malicious activity. If an activity matches the rule, an alert is generated and sent out for security teams to assess.

3. **Log storage:** SIEM tools can act as a system for data retention, which can provide access to historical data. Data can be kept or deleted after a period depending on an organization's requirements.
