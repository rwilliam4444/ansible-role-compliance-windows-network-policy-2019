# Role Name:
- ansible-role-compliance-windows-network-policy-2019

# Description:
This Network Policy Role was based off the CIS specs for 2019 servers.   This role covers the "Network" CIS section only. The checks and remediation commands are for local settings only. Group Policy settings may override these settings. When the "remediate" variable is set to "YES", the role will try to remediate the server's setting(s) accoridng to the CIS standards.  The defaults/main.yml file can be used to disable specific CIS items (i.e. "execute_<cis task #>") from executing. The default value in the defaults/main.yml for these CIS item variables (i.e. "execute_<cis task #>") is set to "YES". The value "YES" means that the CIS item will execute at run time. Set the value to "NO" if you want to skip this CIS item in question from executing.

# Requirements:
Windows Ansible related pre-requisites 

# Defaults file for ansible-role-compliance-windows-network-policy-2019:
# Variables
Parameter | Choices/Defaults|Comments
----------|-----------------|--------
__remediate__ | "NO" | variable for whether or not to remediate the non-compliant settings.
__NodeType_cis__ | "2" | CIS value.
__EnableMulticast_cis__ |"0"| CIS value.
__EnableFontProviders_cis__ |"0"| CIS value.
__AllowInsecureGuestAuth_cis__ |"0"| CIS value.
__AllowLLTDIOOnDomain_cis__ |"0"| CIS value.
__AllowLLTDIOOnPublicNet_cis__ |"0"| CIS value.
__EnableLLTDIO_cis__ |"0"| CIS value.
__ProhibitLLTDIOOnPrivateNet_cis__ |"0"| CIS value.
__AllowRspndrOnDomain_cis__ |"0"| CIS value.
__AllowRspndrOnPublicNet_cis__ |"0"| CIS value.
__EnableRspndr_cis__ |"0"| CIS value.
__ProhibitRspndrOnPrivateNet_cis__ |"0"| CIS value.
__Disabled_cis__ |"1"| CIS value.
__NC_AllowNetBridge_NLA_cis__ |"0"| CIS value.
__NC_ShowSharedAccessUI_cis__ |"0"| CIS value.
__NC_StdDomainUserSetLocation_cis__ |"1"| CIS value.
__Netlogon_cis__ |"RequireMutualAuthentication=1, RequireIntegrity=1"| CIS value.
__SYSVOL_cis__ |"RequireMutualAuthentication=1, RequireIntegrity=1"| CIS value.
__DisabledComponents_cis__ |"255"| CIS value.
__EnableRegistrars_cis__ |"0"| CIS value.
__DisableUPnPRegistrar_cis__ |"0"| CIS value.
__DisableInBand802DOT11Registrar_cis__ |"0"| CIS value.
__DisableFlashConfigRegistrar_cis__ |"0"| CIS value.
__DisableWPDRegistrar_cis__ |"0"| CIS value.
__DisableWcnUi_cis__ |"1"| CIS value.
__fMinimizeConnections_cis__ |"1"| CIS value.
__fBlockNonDomain_cis__ |"1"| CIS value.



# Example Playbook:
---
 - hosts: [win]
   roles:
   - ansible-role-compliance-windows-network-policy-2019


# Author Information:
Richard M. Williams (williamsitv@yahoo.com)
