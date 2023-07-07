# ActiveDirectory-1K_Users
Active directory lab using Virtual box, Windows server 2019 and Windows 10.

## Introduction
<b>Welcome to the Active Directory lab!</b>
<br>In this lab, I have created a simulated environment using Windows Server 2019 and VirtualBox to explore Active Directory. The main objective of this lab is to enhance my understanding of Active Directory and provide me with hands-on experience in creating and managing environments. By configuring the client and Domain Controller I can route the clients' internet traffic through the Domain Controller, doing this I can establish an improved security framework and exercise greater control over the clients connected to the domain. </br>
 
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
## Thoughts
<b>Explanation</b>
<br>Powershell was used to generate first and last names for 1,000 users. The names were then used to create usernames for the account with all passwords sharing Password1. The users were then added with the information about first name, last name, username, password and enabling the account. The powershell script then created a new OU in Active Directory called USERS_PS and added each new user into the newly created OU. </br>
<br>![image](https://github.com/taco2442/ActiveDirectory-1K_Users/assets/58244861/84a608a7-1ebe-4d4e-9d17-4c9bd87c7bbb)</br>


<br><b>Finished set up</b></br>
<br>I was able to successfully ping google.com and Testdomain.com. On my Client I could visit Github.com/taco2442 verify that my DHCP had worked giving me an address of 172.16.0.100 which will be leased for 8 Days.</br>
<br>![image](https://github.com/taco2442/ActiveDirectory-1K_Users/assets/58244861/85e63ea5-1517-4cfc-bd53-9eb4f67e8ff9)</br>

<b>Lessons learned</b>
<br>During the creation of this lab I had to troubleshoot with networking, watch more tutorials and redo the lab. This allowed me to fully wrap my head around the end goal I was trying to achieve. It also made me able to complete the creation of this lab with only following key stages I needed to accomplish. Starting again on this lab I would take more time to keep a note of key events to make the creation flow smoother.</br>

## Conclusion

<b>Closing details</b>
<br>Having my client set up to route through my Domain Controller to access the internet has given me a better understanding of how to have a more enhanced security framework. I also had more control over clients accessing my domain in Active Directory by centralizing where I can apply security controls. This set up could be applied to a real scenario like where many different people would access the internet inside the network like cafes, restaurants or librarys. By controlling DHCP from the Domain Controller we can assign rules such as only allowing 100 IP addresses and leasing them for an appropriate amount of time before they need to be redone. </br>

