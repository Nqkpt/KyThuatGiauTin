Project: Secure Message Transmission via VPN
Objectives:
Establish secure VPN connections for reliable message transmission.
Implement and configure OpenVPN for secure communication.
Ensure safe data transmission using steganography.
Role: VPN Settings, Packet Creation, Data Transmission
Description:
VPN Configuration:
OpenVPN Server on AWS: Configured as the main access point (IP: 172.31.20.199), set up routing for network range 172.31.0.0/24, and added users with VPN Gateway enabled.
Ubuntu Client: Configured as an OpenVPN client (IP: 42.118.123.150), enabled IP forwarding, and rebooted to apply settings.
Packet Creation and Transmission:
Preparing Data: Converted user input message into binary format for hiding in packets.
Creating Packets: Embedded secret data into the MSS field of TCP/IP packet options, generated packets, and sent them to the VPN IP of the Client Machine.
Packet Reception and Data Extraction:
Reading Packets: Used Wireshark to capture packets, read them with Scapy, and checked for the presence of IP and TCP layers from the Server.
Extracting Data: Retrieved the MSS field from TCP options, extracted bits, and reassembled them into the original message.
Displaying Message: Converted extracted bits to a readable message and displayed it for the user.
