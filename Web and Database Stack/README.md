# Web and Database CAM Deployment Using ARM
ARM Templates that deploys the following:

1. An NSG for each subnet in a VNet virtual network, as described below:
  * NSG-FrontEnd. The front end NSG will be applied to the FrontEnd subnet, and contain two rules:
    * rdp-rule. This rule will allow RDP traffic to the FrontEnd subnet.
    * web-rule. This rule will allow HTTP traffic to the FrontEnd subnet.
  * NSG-BackEnd. The back end NSG will be applied to the BackEnd subnet, and contain two rules:
    * sql-rule. This rule allows SQL traffic only from the FrontEnd subnet.
    * web-rule. This rule denies all internet bound traffic from the BackEnd subnet.

    The combination of these rules create a DMZ-like scenario, where the back end subnet can only receive incoming traffic for SQL from the front end subnet, and has no access to the Internet, while the front end subnet can communicate with the Internet, and receive incoming HTTP requests only.

2. One (1) Windows 2012 R2 Web Server with a public IP
3. One (1) Windows 2012 R2 MS SQL Web Edition Server
4. Appropriate storage accounts for virtual servers
