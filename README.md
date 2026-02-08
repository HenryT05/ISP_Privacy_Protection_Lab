# ISP Privacy Protection Lab

## Objective
The Objective of this project is to demonstrate how to protect network traffic from an Internet Service Provider (ISP). This is valuable because an ISP is able to collect data on a person. meaning they can use this data and sell to corporations that create targeted profiles for advertising and tracking purposes. I believe that each person has a right to privacy and that their data should be protected. This lab provides the learning and understanding of network privacy, encryption protocols, and defensive strategies.

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

### Step 2 : Choosing VPN
There are many VPN services that one can choose. Most VPN's claim that they dont keep logs about your internet usage. However only few VPN's have undergone a full third-party audit. So picking a VPN is a important idea when it comes to keeping your data safe. I believe that most private and safe VPN is Mullvad VPN since it requires no email, username, or password and only an account number is generated. It also can recieve payments from various ranges from crypto currency to mailing in cash. this makes it so that mullvad has very to little no information about their users. Since using a VPN leaves your internet logs in the power of the VPN company its very important to choose the right one.

For the project however I will be using nordvpn since I already paid for a 2 year subscription. this VPN service also keeps no user logs. But requires an email to sign up.

### Step 3: Configuring WireGuard VPN on Router
Ok now to actually use a VPN to protect ourselves. I would recommend to use a router that is not provided by the ISP. There are many routers that can be used. For this project I will be using the Flint 2 by GL.inet. Im going to head to my routers admin panel and find VPN client. Im going to then select WireGuard Client. WireGuard provides state-of-the-art encryption that's faster and more secure than older protocols like OpenVPN. 
<img width="800" height="819" alt="image" src="https://github.com/user-attachments/assets/c3e466f9-a3fb-4a5a-93db-7e0faf383f6f" />

Its then going to ask for an access token if your on NordVPN. If its on Mullvad it will ask for the account number. For other VPN services you can click on the setup guide provided on the admin page also. After entering in the VPN details it will lead to a page with servers across the world that the VPN has. Many people select Switzerland or Sweden servers for better data protection laws. Im going to choose San Francisco and hit apply.
<img width="595" height="624" alt="image" src="https://github.com/user-attachments/assets/465bded4-3233-4330-bd31-75a51f7bef4e" />

Then I will head over to the VPN Dashboard section and turn on kill switch. This makes it so that all traffic will be forced through the VPN tunnel and makes sure no traffic is leaked. Now 
<img width="1280" height="583" alt="image" src="https://github.com/user-attachments/assets/031a69fe-8132-47b1-b6ab-975899032b02" />

### Step 4: Setting Up NextDNS for Encrypted DNS Queries
Now its time to Encrypt our DNS queries. For different routers its a different process but for the flint 2 im going to head over to network > DNS/ Then im going to turn on encrypted DNS for the mode and select DNS over transport layer security (TLS). For the DNS provider im going to select NextDNS. From there i will head over to the NextDNS website and create an free account. I will then copy my NextDNS id and paste it back in the router. Make sure to also switch on Override DNS Settings of All Clients and the other 2 options.

<img width="1308" height="749" alt="image" src="https://github.com/user-attachments/assets/292bd9e6-ddb2-4bdd-bafd-1651141997f5" />

<img width="1169" height="604" alt="image" src="https://github.com/user-attachments/assets/a76ec159-c848-479e-ab41-d9b8974aaeac" />

With this configured our DNS queries are now encrypted using  DNS-over-TLS/DoH. this combined with the VPN acts as a two-layer privacy system. Making sure our data is safe and private. Also in NextDNS you can add some blocklists to block ads and trackers if you wanted. You also have the ablitiy to read your own logs and set a retention time for the logs to expire. Im going to keep the logs for 1 day and change the storage location of my logs to Switzerland. You can do this in the settings tab of NextDNS.
<img width="1234" height="743" alt="image" src="https://github.com/user-attachments/assets/039e58ff-6c2d-4441-a784-96ee0c47bb6d" />


