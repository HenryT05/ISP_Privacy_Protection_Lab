# ISP Privacy Protection Lab

## Objective
The Objective of this project is to demonstrate how to protect network traffic from an Internet Service Provider (ISP). This is valuable because an ISP is able to collect data on a person. meaning they can use this data and sell to corporations that create targeted profiles for advertising and tracking purposes. I believe that each person has a right to privacy and that their data should be protected. This lab provides learning and understanding of network privacy, encryption protocols, and defensive strategies.

### Skills Learned
- Understanding of VPN technology and the differences between centralized vs. decentralized VPN architectures
- Application of WireGuard protocol
- deployment of DNS-over-TLS (DoT) and DNS-over-HTTPS (DoH) for DNS query encryption

### Tools Used
- Mullvad VPN -  VPN service with no email/password requirements
- Nord VPN - VPN alternative service
- NextDNS - DNS encryption service providing DoT/DoH
- GL.iNet Flint 2 Router - Router with VPN client and DNS encryption abilities
- WireGuard - Modern, fast, and lightweight VPN encryption method (preferred over older OpenVPN)


## Steps

### Step 1: Understanding the Privacy Threat
ISP's can view all unencrypted traffic passing through their networks. This allows them to collect and log user data based on browsing habits, search queries, website visits, timing patterns, and even infer mental health indicators. This data can also be sold to other Big Tech companies which then allows them to create detailed user profiles for targeted advertising and much more.

