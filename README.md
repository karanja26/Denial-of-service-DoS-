<h1>Disclaimer</h1>
<br>The content of this project is intended solely for educational and ethical purposes. The skills and knowledge shared are to be used only for lawful activities, such as securing systems and networks with proper authorization. Unauthorized access, tampering, or exploitation of any computer systems or networks is illegal and punishable by law. By participating in this project, you agree to abide by all applicable laws and to use your skills responsibly.</br>
<h1>Denial of Service(DoS) Attacks<h1> 
<h2>Description</h2>
<br>Denial-of-Service (DoS) and Distributed Denial-of-Service (DDoS) attacks have become a major
threat to computer networks. These attacks attempt to make a machine or network resource
unavailable to its authorized users. Usually, DoS and DDoS attacks exploit vulnerabilities in the
implementation of TCP/IP model protocol or bugs in a specific OS.
In a DoS attack, attackers flood a victim’s system with nonlegitimate service requests or traffic
to overload its resources, bringing the system down and leading to the unavailability of the
victim’s website—or at least significantly slowing the victim’s system or network performance.
The goal of a DoS attack is not to gain unauthorized access to a system or corrupt data, but to
keep legitimate users from using the system.
Perpetrators of DoS attacks typically target sites or services hosted on high-profile web servers
such as banks, credit card payment gateways, and even root nameservers.
In general, DoS attacks target network bandwidth or connectivity. Bandwidth attacks overflow
the network with a high volume of traffic using existing network resources, thus depriving
legitimate users of these resources. Connectivity attacks overflow a computer with a flood of
connection requests, consuming all available OS resources, so that the computer cannot process
legitimate users’ requests.
As an expert ethical hacker or penetration tester (hereafter, pen tester), you must possess sound
knowledge of DoS and DDoS attacks to detect and neutralize attack handlers, and mitigate such
attacks.
The labs in this module give hands-on experience in auditing a network against DoS and DDoS
attacks.
<br/>
<h2>Tools and appplication used</h2>
<b>hping3 </b>
  hping3 is a command-line-oriented network scanning and packet crafting tool for the TCP/IP
protocol that sends ICMP echo requests and supports TCP, UDP, ICMP, and raw-IP protocols.
It performs network security auditing, firewall testing, manual path MTU discovery, advanced
traceroute, remote OS fingerprinting, remote uptime guessing, TCP/IP stacks auditing, and other
functions.
Here, we will use the hping3 tool to perform DoS attacks such as SYN flooding, Ping of Death
(PoD) attacks, and UDP application layer flood attacks on a target host.
<h2>Environment used</h2>
<b>Parrot Security Machine, Windows 11</b>
<h2>Program walkthrough:</h2>
  in this scenario I  am using a virtulised environment to run different operating systems.Assuming you have already set up your virtual machines it safe to procceed by attacking this machines in a controlled environments.
<p align="center">
  step 1. Click Windows 11 to switch to the Windows 11 machine. On the Windows
11 machine, Click Search icon ( ) on the Desktop. Type wireshark in the search
field, the Wireshark appears in the results, click Open to launch it.
 <br/>
  <img src="https://github.com/karanja26/Denial-of-service-DoS-/assets/55892563/1a7ec68b-4b15-4d55-9a54-4c9416bf9665" alt="image" style="width: 50%; height: auto; display: block; margin: 0 auto;"/>
  <br/>
</p>

<p align="center">
  step 2.	The Wireshark Network Analyzer window appears. Double-click on the primary network interface (here, Ethernet) to start capturing the network traffic. 
Note: If a Software Update pop-up appears click on Remind me later. 
 
 <br/>
  <img src="https://github.com/karanja26/Denial-of-service-DoS-/assets/55892563/197c2785-8cfb-40c3-9e71-f3cb3765943d" alt="image" style="width: 50%; height: auto; display: block; margin: 0 auto;"/>
  <br/>
</p>

<p align="center">
  step 3.	Wireshark starts capturing the packets; leave it running.  
 <br/>
  <img src="https://github.com/karanja26/Denial-of-service-DoS-/assets/55892563/2d6fc781-4e2b-4cd6-9acb-b6cfe4acb916"alt="image" style="width: 50%; height: auto; display: block; margin: 0 auto;"/>
  <br/>
</p>

<p align="center">
  step 4.switch to the Parrot Security machine. 
5.	Click the MATE Terminal icon at the top of the Desktop window to open a Terminal window. 
 
 <br/>
  <img src="https://github.com/karanja26/Denial-of-service-DoS-/assets/55892563/f752083d-ec79-4d6a-b762-c5e8bdb892bf"
alt="image" style="width: 50%; height: auto; display: block; margin: 0 auto;"/>
  <br/>
</p>

<p align="center">
  step 6.	The terminal window appears. In the terminal window, type sudo su and press Enter to run the programs as a root user. 
Step 7.	In the [sudo] password for attacker field, type toor as a password and press Enter. 
Note: The password that you type will not be visible. 
Step 8.	Now, type cd and press Enter to jump to the root directory. 
 
 <br/>
  <img src="https://github.com/karanja26/Denial-of-service-DoS-/assets/55892563/f2bbaa7e-0d7f-4c40-a61b-231231e41c8c" alt="image" style="width: 50%; height: auto; display: block; margin: 0 auto;"/>
  <br/>
</p>

<p align="center">
  step . 
 <br/>
  <img src=alt="image" style="width: 50%; height: auto; display: block; margin: 0 auto;"/>
  <br/>
</p>

<p align="center">
  step . 
 <br/>
  <img src=alt="image" style="width: 50%; height: auto; display: block; margin: 0 auto;"/>
  <br/>
</p>

<p align="center">
  step . 
 <br/>
  <img src=alt="image" style="width: 50%; height: auto; display: block; margin: 0 auto;"/>
  <br/>
</p>

<p align="center">
  step . 
 <br/>
  <img src=alt="image" style="width: 50%; height: auto; display: block; margin: 0 auto;"/>
  <br/>
</p>

<p align="center">
  step . 
 <br/>
  <img src=alt="image" style="width: 50%; height: auto; display: block; margin: 0 auto;"/>
  <br/>
</p>

<p align="center">
  step . 
 <br/>
  <img src=alt="image" style="width: 50%; height: auto; display: block; margin: 0 auto;"/>
  <br/>
</p>

<p align="center">
  step . 
 <br/>
  <img src=alt="image" style="width: 50%; height: auto; display: block; margin: 0 auto;"/>
  <br/>
</p>

<p align="center">
  step . 
 <br/>
  <img src=alt="image" style="width: 50%; height: auto; display: block; margin: 0 auto;"/>
  <br/>
</p>

<p align="center">
  step . 
 <br/>
  <img src=alt="image" style="width: 50%; height: auto; display: block; margin: 0 auto;"/>
  <br/>
</p>

<p align="center">
  step . 
 <br/>
  <img src=alt="image" style="width: 50%; height: auto; display: block; margin: 0 auto;"/>
  <br/>
</p>

<p align="center">
  step . 
 <br/>
  <img src=alt="image" style="width: 50%; height: auto; display: block; margin: 0 auto;"/>
  <br/>
</p>
