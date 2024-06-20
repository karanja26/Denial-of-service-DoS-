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
Step 7.	In the [sudo] password for attacker field, type your root password and press Enter. 
Note: The password that you type will not be visible. 
Step 8.	Now, type cd and press Enter to jump to the root directory. 
 
 <br/>
  <img src="https://github.com/karanja26/Denial-of-service-DoS-/assets/55892563/f2bbaa7e-0d7f-4c40-a61b-231231e41c8c" alt="image" style="width: 50%; height: auto; display: block; margin: 0 auto;"/>
  <br/>
</p>

<p align="center">
  step 9.	A Parrot Terminal window appears; type hping3 -S (Target IP Address) -a (Spoofable IP Address) -p 22 --flood and press Enter. 
Note: Here, the target IP address is 10.10.1.11 [Windows 11], and the spoofable IP address is 10.10.1.19 [Windows Server 2019] 
Note: -S: sets the SYN flag; -a: spoofs the IP address; -p: specifies the destination port; and -flood: sends a huge number of packets. 

 <br/>
  <img src="https://github.com/karanja26/Denial-of-service-DoS-/assets/55892563/86463945-1719-402c-a86c-f0e7f8359233"
alt="image" style="width: 50%; height: auto; display: block; margin: 0 auto;"/>
  <br/>
</p>

<p align="center">
  step 10.	This command initiates the SYN flooding attack on the Windows 11 machine. After a few seconds, press Ctrl+C to stop the SYN flooding of the target machine. 
Note: If you send the SYN packets for a long period, then the target system may crash. 
11.	Observe how, in very little time, the huge number of packets are sent to the target machine. 
 
 <br/>
  <img src="https://github.com/karanja26/Denial-of-service-DoS-/assets/55892563/9069f012-4034-40e3-ac5f-a84bc96cd6ac"
alt="image" style="width: 50%; height: auto; display: block; margin: 0 auto;"/>
  <br/>
</p>

<p align="center">
  step 12.	hping3 floods the victim machine by sending bulk SYN packets and overloading the victim’s resources. 
Click CEHv12 Windows 11 to switch to the Windows 11 machine and observe the TCP-SYN packets captured by Wireshark. 
 
 <br/>
  <img src="https://github.com/karanja26/Denial-of-service-DoS-/assets/55892563/b3dd27c9-7c91-422d-8ee4-abf93894ff91"
alt="image" style="width: 50%; height: auto; display: block; margin: 0 auto;"/>
  <br/>
</p>

<p align="center">
  step 13.	Now, observe the graphical view of the captured packets. To do so, click Statistics from the menu bar, and then click the I/O Graph option from the drop-down list. 
 <br/>
  <img src="https://github.com/karanja26/Denial-of-service-DoS-/assets/55892563/c32993aa-fa5f-4ad1-bbd6-39bd05c21536"
alt="image" style="width: 50%; height: auto; display: block; margin: 0 auto;"/>
  <br/>
</p>

<p align="center">
  step 14.	The Wireshark . IO Graphs . Ethernet window appears, displaying the graphical view of the captured packets. Observe the huge number of TCP packets captured by Wireshark, as shown in the screenshot. 
 <br/>
  <img src="https://github.com/karanja26/Denial-of-service-DoS-/assets/55892563/2bac71c0-041d-49c3-b00c-b8880ff0de3c"
alt="image" style="width: 50%; height: auto; display: block; margin: 0 auto;"/>
  <br/>
</p>

<p align="center">
  step 15.	After analyzing the I/O Graph, click Close to close the Wireshark . IO Graphs . Ethernet window. 
Close the Wireshark main window. If an Unsaved packets… pop-up appears, click Stop and Quit without Saving. 
 
 <br/>
  <img src="https://github.com/karanja26/Denial-of-service-DoS-/assets/55892563/977d80e9-8a54-4bfc-8a3d-455885363c23"
alt="image" style="width: 50%; height: auto; display: block; margin: 0 auto;"/>
  <br/>
</p>

<p align="center">
  step 16.	Now, we shall perform a PoD attack on the target system. 
	Now, click  Parrot Security to switch to the Parrot Security machine. In the Terminal window, type hping3 -d 65538 -S -p 21 --flood (Target IP 
Address) (here, the target IP address is 10.10.1.11 [Windows 11]) and press Enter. 
Note: -d: specifies data size; -S: sets the SYN flag; -p: specifies the destination port; and --flood: sends a huge number of packets. 

 <br/>
  <img src="https://github.com/karanja26/Denial-of-service-DoS-/assets/55892563/bdeda188-eb43-45b1-b629-e3aa95046b70"
alt="image" style="width: 50%; height: auto; display: block; margin: 0 auto;"/>
  <br/>
</p>

<p align="center">
 	This command initiates the PoD attack on the Windows 11 machine.
Note: In a PoD attack, the attacker tries to crash, freeze, or destabilize the targeted system or service by sending malformed or oversized packets using a simple ping command.
Note:For example, the attacker sends a packet that has a size of 65,538 bytes to the target web server. This packet size exceeds the size limit prescribed by RFC 791 IP, which is 65,535 bytes. The receiving system’s reassembly process might cause the system to crash..	hping3 floods the victim machine by sending bulk packets, and thereby overloading the victim’s resources.Click Windows 11 to switch to the Windows 11 machine.
	step 17.Click Search icon ( ) on the Desktop. Type wireshark in the search field, the Wireshark appears in the results, click Open to launch it.
 
 <br/>
  <img src="https://github.com/karanja26/Denial-of-service-DoS-/assets/55892563/6f23b2a2-9c0f-42af-b40b-c4f4e92af624"
alt="image" style="width: 50%; height: auto; display: block; margin: 0 auto;"/>
  <br/>
</p>

<p align="center">
  step 18.The Wireshark Network Analyzer window appears. Double-click on the primary network interface (here, Ethernet) to start capturing the network traffic.
 <br/>
  <img src="https://github.com/karanja26/Denial-of-service-DoS-/assets/55892563/65642579-5ca0-4e31-a76f-084dc1eaf54f"
alt="image" style="width: 50%; height: auto; display: block; margin: 0 auto;"/>
  <br/>
</p>

<p align="center">
  step 19.Observe the large number of packets captured by Wireshark. 
 <br/>
  <img src="https://github.com/karanja26/Denial-of-service-DoS-/assets/55892563/f5e16508-4116-43e4-85cd-798eff26c0c2"
alt="image" style="width: 50%; height: auto; display: block; margin: 0 auto;"/>
  <br/>
</p>

<p align="center">
  step 20.You can observe the degradation in the performance of the system.
Note: The results might differ when you perform the task.
Click  Parrot Security to switch to the Parrot Security machine. In the Terminal window, press Ctrl+C to terminate the PoD attack using hping3.
 
 <br/>
  <img src="https://github.com/karanja26/Denial-of-service-DoS-/assets/55892563/19e63784-2c03-47b3-9501-5f4f15195dc2"
alt="image" style="width: 50%; height: auto; display: block; margin: 0 auto;"/>
  <br/>
</p>

<p align="center">
  step 21.	Now, we shall perform a UDP application layer flood attack on the Windows Server 2019 machine using NetBIOS port 139. To do so, first, determine whether NetBIOS port 139 is open or not.
	In the terminal window, type nmap -p 139 (Target IP Address) (here, the target IP address is 10.10.1.19 [Windows Server 2019]) and press Enter.
Note:Here, we will use NetBIOS port 139 to perform a UDP application layer flood attack.

 <br/>
  <img src="https://github.com/karanja26/Denial-of-service-DoS-/assets/55892563/b1067673-1eb8-4a4e-9275-bd40cf689190"
alt="image" style="width: 50%; height: auto; display: block; margin: 0 auto;"/>
  <br/>
</p>

<p align="center">
  step 21 Now, type hping3 -2 -p 139 --flood (Target IP Address) (here, the target IP address is 10.10.1.19 [Windows Server 2019]) and press Enter.
Note:-2: specifies the UDP mode; -p: specifies the destination port; and --flood: sends a huge number of packets.

 <br/>
  <img src="https://github.com/karanja26/Denial-of-service-DoS-/assets/55892563/8472eb87-2473-4aad-9425-113ef1ffebb6"
alt="image" style="width: 50%; height: auto; display: block; margin: 0 auto;"/>
  <br/>
</p>

<p align="center">
  step 22.	Click  Windows Server 2019 to switch to the Windows Server 2019 machine, click Ctrl+Alt+Del to activate the machine. By default, Administrator account is selected, type your pass in the Password field and press Enter to log in.
 <br/>
  <img src="https://github.com/karanja26/Denial-of-service-DoS-/assets/55892563/c0824dbb-fa8d-43c2-b959-0e07d229dee0"
alt="image" style="width: 50%; height: auto; display: block; margin: 0 auto;"/>
  <br/>
</p>

<p align="center">
  step 23.	In the Type here to search field on the Desktop, type wireshark in the search field, the Wireshark appears in the results, click Wireshark to launch it.
Note: You might experience degradation in the Window Server 2019 machine’s performance.

 <br/>
  <img src="https://github.com/karanja26/Denial-of-service-DoS-/assets/55892563/d4a7481f-fcaa-45c9-abde-c5dfa8938454"
alt="image" style="width: 50%; height: auto; display: block; margin: 0 auto;"/>
  <br/>
</p>

<p align="center">
  step 24.	The Wireshark Network Analyzer window appears. Double-click on the primary network interface (here, Ethernet) to start capturing the network traffic.
Note: The network interface might differ when you perform the task.
Note: If a Software Update pop-up appears click on Remind me later.

 <br/>
  <img src="https://github.com/karanja26/Denial-of-service-DoS-/assets/55892563/3d2e65d3-141a-4a8f-8848-2462734875bc"
alt="image" style="width: 50%; height: auto; display: block; margin: 0 auto;"/>
  <br/>
</p>

<p align="center">
Wireshark displays the network’s flow of traffic. Here, observe the huge number of UDP packets coming from the Source IP address 10.10.1.13 via port 139.
 <br/>
  <img src="https://github.com/karanja26/Denial-of-service-DoS-/assets/55892563/feb748fd-f54c-4403-8f27-55758d1b0ce9"
alt="image" style="width: 50%; height: auto; display: block; margin: 0 auto;"/>
  <br/>
</p>

<p align="center">
  step 25.	Click CEHv12 Parrot Security to switch to the Parrot Security machine. In the Terminal window, press Ctrl+C to terminate the DoS attack.
Note: Here, we have used NetBIOS port 139 to perform a UDP application layer flood attack. Similarly, you can employ other application layer protocols to perform a UDP application layer flood attack on a target network.
Note: Some of the UDP based application layer protocols that attackers can employ to flood target networks include:
Note: - **CharGEN **(Port 19)
	<p align="center">
<ul>
        <li>SNMPv2 (Port 161)</li>
        <li>QOTD (Port 17)</li>
        <li>RPC (Port 135)</li>
        <li>SSDP (Port 1900)</li>
        <li>CLDAP (Port 389)</li>
        <li>TFTP (Port 69)</li>
        <li>NetBIOS (Port 137, 138, 139)</li>
        <li>NTP (Port 123)</li>
        <li>Quake Network Protocol (Port 26000)</li>
	<li>VoIP (Port 5060)</li>
    </ul>
    </p>
	  <br/>
	  <img src="https://github.com/karanja26/Denial-of-service-DoS-/assets/55892563/4fe85cd2-bffa-4b5b-9d58-988d431befe6"
	alt="image" style="width: 50%; height: auto; display: block; margin: 0 auto;"/>
	  <br/>
	</p>

<p align="center">
This concludes the demonstration of how to perform DoS attacks (SYN flooding, PoD attacks, and UDP Application Layer Flood Attacks) on a target host using hping3.
 </p>


