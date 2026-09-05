Indicators of Compromise(IOC)-
Observable evidence that suggests signs of a potential  security incident.

# Command and Control(C2C):

1. malicious actors can use protocols and ports that are not commonly associated to maintain communications between the compromised system and their own machine. These communications are what’s known as command and control (C2), which are the techniques used by malicious actors to maintain communications with compromised systems.

2. For example, malicious actors can use HTTPS protocol over port 8088 as opposed to its commonly associated port 443 to communicate with compromised systems. Organizations must know which ports should be open and approved for connections, and watch out for any mismatches between ports and their associated protocols.

# Packet payload information:
1. Network packets contain components related to the transmission of the packet.
2. This includes details like source and destination IP address, which is the actual data that's transmitted.
3. Often, this data is encrypted and requires decryption for it to be readable.
4. Organizations can monitor the payload information of packets to uncover unsual activity, such as sensitive data transmitting outside of the network, which could indicate a possible exfiltration attack.

# Temporal patterns:
1. Network patterns contain information relating to time. This information is useful in understanding time patterns.
2. For example, a company operating in North America experiences bulk traffic flows between 9 a.m. to 5 p.m., which is the baseline of normal network activity. 
3. If large volumes of traffic are suddenly outside of the normal hours of network activity, then this is considered off baseline and should be investigated.

# SOC AND NOC:
1.  security operations centers (SOC) and their role in monitoring systems against security threats and attacks.
2. Organizations may deploy a network operations center(NOC), which is an organizational unit that monitors the performance of a network and responds to any network disruption, such as a network outage.
3. While a SOC is focused on maintaining the security of an organization through detection and response, a NOC is responsible for maintaining network performance,availability and uptime.
4. Security analysts monitor networks to identify any signs of potential security incidents known as indicators of compromise (IoC) and  protect networks from threats or attacks. 

# Network monitoring tools:
1. **Intrusion detection systems(IDS)**-
monitor system activity and alert on possible intrusions. An IDS will detect and alert on the deviations you’ve configured it to detect. Most commonly, IDS tools will monitor the content of packet payload to detect patterns associated with threats such as malware or phishing attempts.

2. **Network protocol analyzers**-
also known as packet sniffers, are tools designed to capture and analyze data traffic within a network.
They can be used to analyze network communications manually in detail.
Examples include tools such as tcpdump and Wireshark, which can be used by security professionals to record network communications through packet captures. Packet captures can then be investigated to identify potentially malicious activity.

# Defensive measures of data exfiltration attacks:
1. Prevent attacker access.
2. Monitor network activity.
3. Protect assets.
4. Detect and stop the exfiltration.
