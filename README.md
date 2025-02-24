
<!DOCTYPE html  PUBLIC '-//W3C//DTD XHTML 1.0 Transitional//EN'  'http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd'><html xmlns="http://www.w3.org/1999/xhtml">
<head>
<meta content="text/html; charset=utf-8" http-equiv="Content-Type"/>
</head><body><b><u>VERIFYING MAC ADDRESSES OF CISCO IOS SWITCHES</u></b><br/>
<br/>
<b>Objective</b>: This lab is to explore the MAC address table on Cisco IOS switches and routing table on cisco IOS routers.<br/>
Below is the topology for my lab demonstration.<br/>
<img src="1.png"/><br/>
From this topology I had to login and check which interface has been configured on 10.10.10.10/24 by using the &quot;show ip interface brief&quot; command.<br/>
These are the results of my ip configurration check below.The ranges for this check was from Router1 (R1) to Router4(R4).<br/>
<img src="2.png"/><br/>
<img src="3.png"/><br/>
<img src="4.png"/><br/>
<img src="5.png"/><br/>
<br/>
Now I know the NIC running the protocol, I can find the MAC Addresses of each routers.<br/>
Using the command &quot;show interface gigabitethernet 0/0&quot;<br/>
<img src="6.png"/><br/>
<br/>
The MAC address is also known as the physical address. From the screenshot the Hardware is CN Gigabit Ethernet, and the address is<i><b>0090.2b82.ab01</b></i><b><br/>
</b>Physical/Hardware address = MAC address.<br/>
<br/>
Below are the screenshots for the MAC addresses for R2, and R4.<br/>
<img src="7.png"/><br/>
R2 MAC address is 0060.2fb3.9152 looking at the output of our command.<br/>
<br/>
<img src="8.png"/><br/>
Above is the screenshot for router R4. The MAC address of R4 = 00d0.9701.02a9<br/>
<br/>
R3 approach is quite different from the rest due to the NIC. In R3's case it's using the gigaethernet0/1 which is different from the others<br/>
<img src="9.png"/><br/>
From the screenshot above, the command was runned against a different NIC in order to find the MAC address which is gigabitetherne0/1.<br/>
So looking at the screenshot the MAC address = 0001.9626.8970<br/>
<br/>
<b><u>VIEWING DYNAMICALLY LEARNED MAC ADDRESS ON SWITCHES<br/>
</u></b><br/>
<b>Objective</b>: We will be verifying the router's MAC addresses are reachable via the expected ports in the topology below.<br/>
<img src="1 2.png"/><br/>
To begin with we will test for SW1 but first of all let me explain dynamically learned MAC address. A dynamically learned MAC address is an address that a switch learns when a device connects to the network for the first time.<br/>
The command to view this is &quot; show mac address-table dynamic&quot;. Below is the use of this command to display the dynamic mac address-table.<br/>
<img src="10.png"/><br/>
So looking at the table above we can tell the MAC addresses of the routers connected to SW1 and the ports in which they are connected to, which are Fa0/24 and Fa0/1 respectively.<br/>
If you wish to clear this table you can use the command &quot;clear mac address-table dynamic&quot;<br/>
<br/>
Let us repeat for SW2 as well.<br/>
<img src="11.png"/><br/>
<br/>
<b>NOTE</b>: Devices ina real world network tend to be more chatty and send traffic more frequently, which causes the MAC address table to stay updated. The Switch will periodically flush old entries.</body></html>
