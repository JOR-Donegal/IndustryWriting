# Listings
Whenever a project has code or configuration, you may be required to provide listings and these may be industry or project specific. Whenever you provide Infrastructure as Code (IaC), this is the main deliverable!

In assignments, I will typically ask for “A copy of the listings tidied up as much as possible”.

On server configuration, this might be PowerShell, Shell script, Ansible/YAML, etc. 

Networking Example
On a networking project, if I look at the physical and logical diagrams, I know what the listings should look like for each device.

Switches should show best security practice as demonstrated in the associated practical exercises. I should be able to recreate your configuration based on the listings. If you added notes, better!

Whatever you submit must work, make sure it’s a tested configuration, and it must match your other documentation, logical, physical diagrams, etc.

For network equipment, your listings should have some or all:

- Port descriptions. 
- Trunking, native VLAN, pruning. 
- Password security, passwords encrypted/obfuscated in listings. 
- Loop avoidance, typically spanning tree (portfast, root guard, etc.) 
- Port security 
- Unused ports mapped to discard VLAN and switched off. 
- NTP/SNTP/PtP 
- VTP (optional, only if CISCO used), 
- Native VLAN, discard. 
- VRRP/HSRP 
- Custom banners/warnings 
- Make sure each switch has a management IP address in the correct VLAN.

Provide either a

- A usable script 
- If its Cisco equipment, you may also need a __sh vlan__
- If there is a router, maybe also include a __sh ip route__.

Some students log the output of a Putty session, this is useful, but the text file must be cleaned up and documented before you submit.

As we move to networks provisioned as IaC, you may have files in specific formats, YANG models etc. If so, include them in your report.

In assignments, you are providing an example configuration to the customer. If you plan to use a stack or chassis, do not worry about configuring the entire stack. If you show a working configuration with an 8 port switch, that will be fine. Just note that the final configuration will be adapted for the hardware supplied for the project.