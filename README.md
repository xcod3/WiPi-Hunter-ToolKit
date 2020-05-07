```
		__        ___ ____  _       _   _             _            
		\ \      / (_)  _ \(_)     | | | |_   _ _ __ | |_ ___ _ __ 
		 \ \ /\ / /| | |_) | |_____| |_| | | | | '_ \| __/ _ \ '__|
		  \ V  V / | |  __/| |_____|  _  | |_| | | | | ||  __/ |   
		   \_/\_/  |_|_|   |_|     |_| |_|\__,_|_| |_|\__\___|_|   
                                                           
				 _____           _ _  ___ _   
				|_   _|__   ___ | | |/ (_) |_ 
				  | |/ _ \ / _ \| | ' /| | __|
				  | | (_) | (_) | | . \| | |_ 
				  |_|\___/ \___/|_|_|\_\_|\__|
            

			                By XC0D3
			       	https://cs-academy.org/
                  
	    WiPi-Hunter-ToolKit integrates all WiPi-Hunter tools in one place.
In this way it is easy to monitor illegal wireless network activities with a single tool.
```

#Modules

##PiDense
#### Purpose

Monitor  **illegal wireless network activities.**

+ Similar SSID broadcasts
+ Detects SSID brute
+ Detects beacon flood
+ Monitor deauthentication attack
+ Same SSID broadcasts
+ Calculates unencrypted wireless networks density
+ Watches SSID broadcasts at the blacklist.
+ KARMA Attacks
+ WiFi Pineapple Activities

#### Capabilities (Now)

+ Calculates Unencrypted wireless network density
+ Finds same ssid, different encryption
+ Watches SSID broadcasts at the blacklist.
+ KARMA Attacks
+ WiFi Pineapple Activities
+ Blacklist SSID analysis

##PiFinger
#### Purpose

The purpose of this module is to determine whether the network we are connected for is opened by Wifi- Pineapple. In addition, the tool analyzes the wireless networks you have previously connected and gives you a security score.

#### Features

* Is this network opened by pineapple?
* Have you been connected to insecure networks before?
* Logging  (
![#f03c15](https://placehold.it/15/f03c15/000000?text=+) `Wireless Security Score`)
(time, mac, ssid, score, is_pineapple)

#### Used Techinuques

**WiFi-Pineapple Network Detection Techniques**

```
A Chinese proverb says:
"If attackers are accessing systems using default settings, 
we too can catch them with the default settings in their software and hardware."
```

* Manufacturer's MAC address information
* Default HTTP Port (1471)
* Default hostname information for wifi-pineapple

**Previous networks**

* Analyzes the wireless networks you have previously connected

##PiKarma
#### Working Principle for PiKarma

+ Collects all the packets from Wireless Network. (Probe Response) 
+ Analyses all the packets in real time.
+ If PiKarma finds more than one SSID info from unique mac address in Probe Response;
+ Logs the activity with some extra information within defined template and sends deauthentication packets 


#### How works KARMA Attack?

+ Sends Probe Response for all Probe Requests

**Example:**

<img src="https://github.com/besimaltnok/pikarma/blob/master/karma.gif">


#### Softwares and hardwares that uses KARMA module

+ FruityWifi
+ WiFi Pineapple
+ Mana (improvements to KARMA attacks)
+ ..

##PiNokyo
#### Purpose
+ 🍓🤥🍍If threats like wifi pineapple attacks or karma attacks are active around, users will be informed about these threats. 
+ Fills the SSID pool of WiFi Pineapple device with the SSID informations in pinokyo.txt
+ Generates fake probe requests against KARMA attacks.


#### Working Principles

+ Collects probe requests
+ Seperates MAC Addresses from probe requests
+ Creates new probe packets with collected MAC addresses
+ Sends probe requests with pinokyo.txt

#### Tested

+ Wifi Pineapple Mark V
+ KARMA Attack
+ MANA (mana-toolkit) Attack

##PiSavar
#### Purpose

The goal of this module is to find out the fake access points opened by the WiFi pineapple device using the PineAP module and to prevent clients from being affected by initiating a deauthentication attack to the attacking device.


### How PineAP Module Works

* Collects SSID information
* Creates SSID pool with collected SSID information
* Creates fake access points using information in the SSID pool

### Where is the problem?

- ![#f03c15](https://placehold.it/15/f03c15/000000?text=+) `One MAC address, more than one SSID information .... ..- -. - . .-. `


### Features of PiSavar

* Detects PineAP activities. 
* Detects networks opened by PineAP.
* Starts deauthentication attack for PineAP.

##PiUser
#### Purpose

📡 Examine probe requests in the environment to determine if they have previously connected to the malicious network
📡 Thus, the number of people who are likely to fall into the potentially fake access point in the environment is determined

For corporation environment

+ Monitors company name in probe requests
+ Monitors blacklist ssids in probe requests

For clients

+ Analyzes behavior the clients of the corporation with probe requests

# Usage (for Linux)

# Requirements