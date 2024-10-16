# Active Directory Lab

## Objective

This Active Directy project aimed to establish a server and create users, aswell as imitate a brute force attack on a Kali machine & to view/read the code on Splunk. The primary focus is to create a virtual server with VMs and create an Active Directory on an admin server. This hands-on experience was designed to deepen understanding of creating & controlling a domain, network security, and basic attacks.

### Skills Learned

- Advanced understanding of domain concepts and practical application.
- Better understanding in analyzing and interpreting network logs.
- Ability to generate and recognize basic attack signatures and patterns.
- Enhanced knowledge of network protocols and security vulnerabilities.

### Tools Used

- **Oracle Virtual Box** to host all VMs and allocate memory.
- **Splunk** application and server for log ingestion and analysis aswell as capture and examine network traffic.
- **Powershell** to create telemetry from Atomic Red Team.
- **Kali Linux** to generate a brute force attack with "crowbar" application.

## Steps

*Ref 1: Network Diagram*

<img src="https://i.imgur.com/jqoWkdQ.png" width="80%"  height="80%" />

*Step 1: Download needed VMs and apply static IP & network configurations as shown in diagram*

<img src="https://i.imgur.com/P0DZg4z.png" width="80%"  height="80%" />

*Step 2: Download Sysmon and Splunk Enterprise on both windows server & target PC and congfigure IP and listening port. 
Once logged in on windows server, go to Splunk Enterprise to create new index and 
make sure both Target PC and Windows Server are listed as hosts*

<img src="https://i.imgur.com/Mhtcg7H.png" width="80%"  height="80%" />

*Step 3: In Windows Server, download & install the server, create domain, create new group and add Users to domain with logins.
Here it allows us to assign roles and create new profiles for instance, new hires. Assign roles with preconfigured settings
and access to each department.*

<img src="https://i.imgur.com/CvWn9Hu.png" width="80%"  height="80%" />

*Step 4: Login to Kali machine. Download crowbar application through Terminal. Enter code "crowbar -b rdp -u tsmith -C passwords.txt -s 192.168.10.100" and attack IP of the server. See success.*

<img src="https://i.imgur.com/F6tOgWZ.png" width="80%"  height="80%" />

*Step 5: Go to Splunk and view events through our created index. See event code 4625 indicating unsuccessful login attempts and event code 4624 showing
successful login and details of logged in machine which is the Kali Linux with the attacker IP of 192.168.10.250.*

<img src="https://i.imgur.com/9QgKmGC.png" width="80%"  height="80%" />

<img src="https://i.imgur.com/lSsZt2R.png" width="80%"  height="80%" />

<img src="https://i.imgur.com/lomdDZu.png" width="80%"  height="80%" />
