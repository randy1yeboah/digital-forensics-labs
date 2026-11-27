# Digital forensics labs

Lab work from my Digital Forensics, Investigation, and Response course at CSU Global. Each lab ran in a virtual environment with a case scenario and evidence files, and I worked through them with standard forensic tools.

Tools used: FTK Imager, E3 (Paraben), Autopsy, StegExpose, OpenPuff, Wireshark, Windows registry tools, and Cisco router commands.

## Lab 1: Applying the Daubert Standard to forensic evidence

I filled out chain of custody paperwork for seized evidence, then used FTK Imager to extract evidence files from a drive image and generate MD5 and SHA-1 hashes for each one. I re-hashed the same files in E3 and compared the results.

The hashes from both tools matched exactly. That shows the evidence wasn't changed between examinations, which is one of the things a court looks for under the Daubert Standard when deciding whether forensic evidence is reliable enough to admit.

## Lab 2: Recognizing steganography

I searched a drive image for signs that steganography software had been installed, then ran StegExpose across a set of images to flag the ones likely hiding data. Using a passphrase found on the drive, I pulled the hidden file out of a suspicious image with OpenPuff.

## Lab 3: Recovering deleted files

I used E3 to recover deleted files and folders from an NTFS drive image, including a deleted patent document that was relevant to the case.

## Lab 5: Windows system forensics

I collected live system information from a Windows workstation: running processes, listening ports, drive details and the NTFS USN change journal. In the registry I pulled the Windows install timestamp, network interface settings, Winlogon values, ShellBags and RecentDocs, which together show what a user opened and where they browsed in File Explorer.

I then analyzed a suspect's Windows drive image in a new case file. I traced an image file through its .lnk shortcut, found installers for suspicious apps in Downloads, spotted a VPN app (Speedify) in the uninstall records, reviewed the user list and startup Run entries, and pulled suspicious browser history and search keywords.

## Lab 7: Email and chat forensics

I read email headers to get timestamps and the sender's IP address, searched an Outlook database for evidence, and went through a Slack workspace database to identify its members and channels and read a relevant conversation.

## Lab 9: Network infrastructure forensics

I captured and analyzed network traffic, filtering it by timestamp, IP address, port, TCP push flag and HTTP. On a router I pulled the version info, interface details, ARP table, routing table and running configuration, which is the information an investigator needs to trace how traffic moved through a network.
