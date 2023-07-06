# ActiveDirectory-1K_Users
Active directory lab using Virtual box, Windows server 2019 and Windows 10.

## Introduction
<b>Welcome to the Active Directory lab!</b>
<br>In this lab, I have created a simulated environment using Windows Server 2019 and VirtualBox to explore Active Directory. The main objective of this lab is to enhance my understanding of Active Directory and provide me with hands-on experience in creating and managing environments. By configuring the client PC and Domain Controller I can route the clients' internet traffic through the Domain Controller, doing this I can establish a more improved security framework and exercise greater control over the clients connected to our domain. </br>
 
This lab will contain:
* Oracle VirtualBox
* Windows 10
* Windows Server 2019
* Powershell


## Architecture
![Untitled](https://github.com/taco2442/ActiveDirectory-1K_Users/assets/58244861/8ffa86a1-b636-4b5d-bbdb-6ca950a30169)

<b>Configuration</b>
<br>NIC 1: Uses DHCP from home router to access internet</br>
<br>NIC 2:
* IP: 172.16.0.1
* MASK: 255.255.255.0
* DNS: 127.0.0.1 </br>

<br>NIC 3: Uses DHCP from Domain Controller</br>

<b>Services</b>
<br>
* Active Directory Domain Service
* Remote Access Service
* Dynamic Host Configuration Protocol Service</br>

<b>Explanation</b>
<br>Powershell was used to generate first and last names for 1,000 users. The names were then used to create usernames for the account with all passwords sharing Password1. The users were then added with the information about first name, last name, username, password and enabling the account. The powershell script then created a new OU in Active Directory called USERS_PS and added each new user into the newly created OU. </br>
<br>![image](https://github.com/taco2442/ActiveDirectory-1K_Users/assets/58244861/4a3536dd-7858-448b-9749-064b5031f062)</br>
## Conclusion
<b>Lessons learned</b>
<br>During the creation of this lab I had to troubleshoot with networking, watch more tutorials and redo the creation of the lab, this allowed me to fully wrap my head around the end goal I was trying to achieve. It also made me able to complete the creation of this lab with only following key stages I needed to hit. Starting again on this lab I would take more time to keep a note of key events to make the creation flow smoother. I would </br>

<b>Closing thoughts</b>
<br>Having my client set up to route through my Domain Controller to access the internet has given me a better understanding of how to have a more enhanced security framework. I also had more control over clients accessing my domain in Active Directory by centralizing where I can apply security controls. </br>

