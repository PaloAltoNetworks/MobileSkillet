# Mobile Skillet

###  Best Practice templates for Palo Alto Networks NGFW for Mobile Networks.
Templates and documentation are based on PAN-OS sofware release version.

The mobile template details and usage are documented here: <br/>
[Mobile Skillet Documentation](http://github.com/PaloAltoNetworks/mobileskillet)

Currently supported versions are:

<b>8.1</b>
[Templates](https://github.com/PaloAltoNetworks/MobileSkillet/tree/panos_v8.1)

<b>9.0</b>
[Templates](https://github.com/PaloAltoNetworks/MobileSkillet/tree/panos_v9.0)

## Getting Started
Mobile-Skillet is best used from within [Panhandler](https://github.com/PaloAltoNetworks/panhandler).  The easiest way to use Panhandler is to do 
so through Docker.  

To start Panhandler: `docker run -p 9999:80 paloaltonetworks/panhandler:latest`

Then point your browser to localhost:9999.

From Panhandler use the drop down menu to import MobileSkillet:
* <b>Repository Name:</b> MobileSkillet
* <b>Git Repository HTTPS URL:</b> https://github.com/PaloAltoNetworks/MobileSkillet.git
* <b>Branch:</b> panos_v9.0

After a successful import you should a MobileSkillet collection.  If you navigate to that collection you
should see a "9.0 Mobile TAP Mode PoC" skillet.  This template will 

* Enable SCTP and GTP functionality in system settings
* Set the disk quotas for logs
* Create a TAPZONE and put the selected interface into it
* Assign a Zone Protection Profile IPOnly that blocks non-IPv4, non-IPv6 and non-VLAN ethertypes
* Creata an SCTP Protection Profile with filtering functions for DIAMETER and SIGTRAN
* Create a GTP Protection Profile with GTP-U inspection and allowed logging settings for watermarking GTP
* Create a Vulnerability Profile with suitable exceptions for Flood and Bruteforce protection
* Configure Forwarding of Threat and GTP logs to the [Safe Networking](https://github.com/PaloAltoNetworks/safe-networking) 
server you specify
* Create an Address Object for the Mobile Subscribers UE (default is CGNAT)
* Create a basic Security Policy that sorts the traffic by App-ID based rules

## Contributing
Please read [CONTRIBUTING.md](https://github.com/PaloAltoNetworks/MobileSkillet/CONTRIBUTING.md) for details on how you can help contribute to this project.

See also [Iron Skillet](https://github.com/PaloAltoNetworks/iron-skillet) for non Mobile templates

## Support
This is a Palo Alto Networks community project.

## Authors
* Mitch Rappard - [(@mitch-pan)](https://github.com/mitch-pan)
* Mario Penners - [(@pennersm)](https://github.com/pennersm)
* Scott Shoaf - [(@scotchoaf)](https://github.com/scotchoaf)
* Edward Arcuri - [(@punisherVX)](https://github.com/punisherVX)
* Nathan Embery - [(@nembery)](https://github.com/nembery)


See also the list of [contributors](https://github.com/PaloAltoNetworks/mobile-templates/contributors) who have participated in this project.


## Support Policy
The code and templates in the repo are released under an as-is, best effort, support policy. These scripts should be seen as community supported and Palo Alto Networks will contribute our expertise as and when possible. We do not provide technical support or help in using or troubleshooting the components of the project through our normal support options such as Palo Alto Networks support teams, or ASC (Authorized Support Centers) partners and backline support options. The underlying product used (the VM-Series firewall) by the scripts or templates are still supported, but the support is only for the product functionality and not for help in deploying or using the template or script itself. Unless explicitly tagged, all projects or work posted in our GitHub repository (at https://github.com/PaloAltoNetworks) or sites other than our official Downloads page on https://support.paloaltonetworks.com are provided under the best effort policy.
