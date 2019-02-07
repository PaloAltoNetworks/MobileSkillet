# Mobile-Skillet for PANOS 8.0

###  Best Practice templates for Palo Alto Networks NGFW for Mobile Networks.
The purpose of these templates is to provide Day 1 best-practice configuration templates for Mobile Networks that can be loaded into a Palo Alto Networks NGFW.
These templates are in addition to the [Iron-Skillet](https://github.com/PaloAltoNetworks/iron-skillet) NGFW best-practices templates

The mobile template details and usage are documented here: <br/>
[Mobile Skillet Documentation](http://github.com/PaloAltoNetworks/mobileskillet)


## Getting Started
Mobile-Skillet is best used from within [Panhandler](https://github.com/PaloAltoNetworks/panhandler).  The easiest way to use Panhandler is to do 
so through Docker.  

To start Panhandler: `docker run -p 9999:80 paloaltonetworks/panhandler:latest`

Then point your browser to localhost:9999.

From Panhandler use the drop down menu to import MobileSkillet:
* <b>Repository Name:</b> MobileSkillet
* <b>Git Repository HTTPS URL:</b> https://github.com/PaloAltoNetworks/MobileSkillet.git
* <b>Branch:</b> panos_v8.0

After a successful import you should see 5 configuration snippets in your Template library under Pan-OS.
* Mobile SIGTRAN Configuration
* Mobile RAN Configuration
* Mobile Roaming Configuration
* Activation of GTP and SCTP capabilities
* Mobile Basline Configuration

Always run "Activation of GTP and SCTP capabilities" first, then "Mobile Baseline Configuration".  From there you can run 
RAN/Roaming/SIGTRAN as needed.

## Contributing
Please read [CONTRIBUTING.md](https://github.com/PaloAltoNetworks/MobileSkillet/CONTRIBUTING.md) for details on how you can help contribute to this project.

## Support
This is a Palo Alto Networks community project.

## Authors
* Mitch Rappard - [(@mitch-pan)](https://github.com/mitch-pan)
* Scott Shoaf - [(@scotchoaf)](https://github.com/scotchoaf)
* Edward Arcuri - [(@punisherVX)](https://github.com/punisherVX)
* Nathan Embery - [(@nembery)](https://github.com/nembery)

See also the list of [contributors](https://github.com/PaloAltoNetworks/mobile-templates/contributors) who have participated in this project.


## Support Policy
The code and templates in the repo are released under an as-is, best effort, support policy. These scripts should be seen as community supported and Palo Alto Networks will contribute our expertise as and when possible. We do not provide technical support or help in using or troubleshooting the components of the project through our normal support options such as Palo Alto Networks support teams, or ASC (Authorized Support Centers) partners and backline support options. The underlying product used (the VM-Series firewall) by the scripts or templates are still supported, but the support is only for the product functionality and not for help in deploying or using the template or script itself. Unless explicitly tagged, all projects or work posted in our GitHub repository (at https://github.com/PaloAltoNetworks) or sites other than our official Downloads page on https://support.paloaltonetworks.com are provided under the best effort policy.
