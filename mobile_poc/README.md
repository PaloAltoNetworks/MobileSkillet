# TAPModePoC
Skillet to set up a Firewall for PoC in TAP mode

#### Installation and usage
1. Get [Panhandler](https://panhandler.readthedocs.io/en/latest/overview.html) running on your local [docker](https://docs.docker.com/)
2. You need to import the skillet via a Panhandler repo. Add the skillet files either as-is or together with other skillets to a repo. If you have access to the original repo you can also import directly from [github](https://github.com/pennersm/TAPModePoC)
add or If you can not access it create your own repo and push the archive that came along this readme. 
3. The original repo has only one YAML file and self-explaining input parameters


#### Need to know
In the current status this skillet is only a defined starting point and mot likely not what you need at the end of the PoC.
Your contribution to improvement should go the usual yet undefined way of using github and internal channels!

Let us know what needs to be adapted.
Do not forget to fill the "Sheets for all" on the Speedboat page, please.

## Current functions

* Enable SCTP and GTP functionality in system settings
* Set the disk quotas for logs
* Create a TAPZONE and put the selected interface into it
* Assign a Zone Protection Profile IPOnly that blocks non-IPv4, non-IPv6 and non-VLAN ethertypes
* Creata an SCTP Protection Profile with filtering functions for DIAMETER and SIGTRAN
* Create a GTP Protection Profile with GTP-U inspection and allowed logging settings for watermarking GTP
* Create a Vulnerability Profile with suitable exceptions for Flood- and Bruteforce protection
* Configure Forwarding of Threat and GTP logs to the SFN35 server you specify
* Create an Address Object for the Mobile Subscribers UE (default is CGNAT)
* Create a basic Security Policy that sorts the traffic by App-ID based rules

##### Purpose of that Policy
As much of the protection is provided by the Vulnerability and Protection Profiles, it would also possible but inconvenient to handle all traffic in one single rule. The purpose of separating by App-ID is, to learn quickly which IP addresses trigger on which rule, so that the traffic and role of NFs/NEs can be understood.    
 
##### PanOS Version
This has been tested with PanOS version 9.0.1. Specifics like e.g. enabling Packet Capture Feature in the GTP Profile or havni UUIDs in the XML for the FW rules have been avoided. We would love to hear someone tested it with 8.1


