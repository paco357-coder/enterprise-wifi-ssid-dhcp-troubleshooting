# enterprise-wifi-ssid-dhcp-troubleshooting

Overview

This project documents troubleshooting and resolution of a wireless SSID connectivity issue on an Aruba Virtual Controller where clients were unable to obtain an IP address and received a 169.x.x.x APIPA address.

The issue was caused by incorrect VLAN assignment and DHCP communication failure.

Environment

Aruba Virtual Controller

WPA2 Enterprise SSID

VLAN based network segmentation

DHCP provided by internal network

Problem:
Clients connecting to the SSID experienced:

"No Internet, secured"

169.254.x.x IP address

Unable to reach network resources

Root Cause

The SSID was assigned to a VLAN that did not have DHCP connectivity.

Troubleshooting Steps

Connected client to SSID

Checked client IP address

Observed 169.x.x.x APIPA address

Verified VLAN assignment on Aruba Virtual Controller

Checked DHCP scope availability

Corrected VLAN assignment to the proper network

Resolution:

Updated SSID VLAN assignment within the Aruba Virtual Controller to the correct VLAN with DHCP access.

Clients successfully received valid IP addresses.

Lessons Learned

APIPA addresses usually indicate DHCP failure

Always verify VLAN mapping for wireless SSIDs

Confirm DHCP availability on the assigned VLAN
