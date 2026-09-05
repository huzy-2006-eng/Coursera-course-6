Components of a network:
1. Header.
2. Payload.
3. Footer.

Network protocol analyzer(packet sniffer)-
A tool designed to capture and analyze data traffic within a network.

Packet capture(P-cap)-
A file containing data packets intercepted from an interface or network.

# Packets:
1. Previously in the program, you learned that a data packet is a basic unit of information that travels from one device to another within a network. Detecting network intrusions begins at the packet level. That's because packets form the basis of information exchange over a network. 
2. Each time you perform an activity on the internet—like visiting a website—packets are sent and received between your computer and the website’s server. These packets are what help transmit information through a network.
3. For example, when uploading an image to a website, the data gets broken up into multiple packets, which then get routed to the intended destination and reassembled upon delivery. 

## 1. Header:
Packets begin with the most essential component: the header. Packets can have several headers depending on the protocols used such as an Ethernet header, an IP header, a TCP header, and more. Headers provide information that’s used to route packets to their destination.
 This includes information about the source and destination IP addresses, packet length, protocol, packet identification numbers, and more. 

## 2. Payload:
The payload  component directly follows the header and contains the actual data being delivered. Think back to the example of uploading an image to a website; the payload of this packet would be the image itself.

## 3. Footer:
The footer, also known as the trailer, is located at the end of a packet. The Ethernet protocol uses footers to provide error-checking information to determine if data has been corrupted. In addition, Ethernet network packets that are analyzed might not display footer information due to network configurations.

# How network protocol analyzers work:
1. First, packets must be collected from the network via the Network Interface Card(NIC), which is hardware that connects computers to a network, like a router.
2. NICs receive and transmit network traffic, but by default they only listen to network traffic that's addressed to them.
3. T capture all the network traffic that is sent over the network, a NIC must be switched to a mode that has access to all visible network data packets. 
4. In wireless interfaces this is often referred to as monitoring mode, and in other systems it may be called promiscuous mode. 
5. This mode enables the NIC to have access to all visible data packets,  but it won’t help analysts access all packets across a network. A network protocol analyzer must be positioned in an appropriate network segment to access all traffic between different hosts. 
6. The network protocol analyzer collects the network traffic in raw binary format. Binary format consists of 0s and 1s and is not as easy for humans to interpret. The network protocol analyzer takes the binary and converts it so that it’s displayed in a human-readable format, so analysts can easily read and understand the information.  

# Capturing packets:
Packet sniffing is the practice of capturing and inspecting data packets across a network. A packet capture (p-cap) is a file containing data packet intercepted from an interface or network.

1. #### Libcap- 
It is a packet capture library designed to be used by Unix-like systems, like Linux and MacOS.
Tools like tcpdump use Libcap as the default packet capture file format.

2. #### WinPcap-
It is an open-source packet capture library designed for devices running windows operating systems.
It is considered an older file format and isn't predominantly used.

3. #### Npcap-
It is a library designed by the port scaning tool Nmap that is commonly used in Windows OS.

4. #### Pacapng-
It is a modern file format that can simultaneously capture packets and store data. Its ability to do both explains the "ng", which stands for "next generation".

# Internet Protocol(IP)-
# IPV4:
1. **Version:** This field indicates the IP version. For an IPv4 header, IPv4 is used. 

2. **Internet Header Length (IHL):** This field specifies the length of the IPv4 header including any Options.

3. **Type of Service (ToS):** This field provides information about packet priority for delivery.

4. **Total Length:** This field specifies the total length of the entire IP packet including the header and the data.

5. **Identification:** Packets that are too large to send are fragmented into smaller pieces. This field specifies a unique identifier for fragments of an original IP packet so that they can be reassembled once they reach their destination.

6. **Flags:** This field provides information about packet fragmentation including whether the original packet has been fragmented and if there are more fragments in transit.

7. **Fragment Offset:** This field is used to identify the correct sequence of fragments.

8. **Time to Live (TTL):** This field limits how long a packet can be circulated in a network, preventing packets from being forwarded by routers indefinitely.

9. **Protocol:** This field specifies the protocol used for the data portion of the packet.

10. **Header Checksum:** This field specifies a checksum value which is used for error-checking the header.

11. **Source Address:** This field specifies the source address of the sender.

12. **Destination Address:** This field specifies the destination address of the receiver.

13. **Options:** This field is optional and can be used to apply security options to a packet.

# IPV6:
1. **Version:** This field indicates the IP version. For an IPv6 header, IPv6 is used.

2. **Traffic Class:** This field is similar to the IPv4 Type of Service field. The Traffic Class field provides information about the packet's priority or class to help with packet delivery.

3. **Flow Label:** This field identifies the packets of a flow. A flow is the sequence of packets sent from a specific source. 

4. **Payload Length:** This field specifies the length of the data portion of the packet.

5. **Next Header:** This field indicates the type of header that follows the IPv6 header such as TCP.

6. **Hop Limit:** This field is similar to the IPv4 Time to Live field. The Hop Limit limits how long a packet can travel in a network before being discarded.

7. **Source Address:** This field specifies the source address of the sender.

8. **Destination Address:** This field specifies the destination address of the receiver.

# Wireshark:
1. Wireshark is an open-source network protocol analyzer. It uses a graphical user interface(GUI), which makes it easier to visualize network communications for packet analysis purposes.
2. Wireshark has many features to explore. 

Display filters
 

Comparsion factors:
1. Equal = eq
2. Not equal != ne
3. Greater than > gt
4. Less than < It
5. Greater than or equal >= ge
6. Less than or equal to <= le

**Contains operator-**
Contains operator is used to filter packets that contain an exact match of a string of text.
Eg - http contains "moved"

**Matches operator-**
Matches operator is used to filter packets based on the regular expression (regex) that's specified.
Regular expression is a sequence of characters that forms a pattern.

**Filter toolbar-**
You can apply filters to a packet capture using Wireshark's filter toolbar.

#### Filter for an IP address:
ip.addr == 172.21.224.2

ip.src == 10.10.10.10

#### Filter for a MAC address:
eth.addr == 00:70:f4:23:18:c4

#### Filter for ports:
udp.port == 53
tcp.port == 25

