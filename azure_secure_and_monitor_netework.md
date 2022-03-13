## Network Security Groups
* **Filter traffic -** Filter traffic to and from azure resources in an Azure Virtual Network.
* **Rules -** Here you can create Inbound and Outbound Network Group Security  rules.
* **Attachment -** NSG can be attached to a Network Interface or to a subnet.
* **Default -** Each NSG has default rules that can't be edited or deleted.
* **Priority -** Here the rules with lower numbers are processed first. Once a matching rule found the processing is stopped.
* **Source/Destination -** Can be an IP address, a service tag(internet), or an Application Security Group.
* **Protocol -** TCP, UDP, ICMP etc...,
* **Dircetion -** Whether it is an inbound or outbound rule.
* **Acion -** Allow or Deny

## Azure FireWall
* **Protection -** Helps to protect your Azure virtual network resources. It has built-in high Availability.
* **Application Rules -** You can restrict outbound traffic to fully qualified domain names.
* **Netwrok Rules -** You can also limit traffic at the network layer.
* **Threat Intelligence -** Can alert and deny traffic based on known malicious IP adresses and domains.
* **NAT Rules -** Define NAT rules for resources in the virtual Network.
* **Forced Tunneling -** Can route all internet bound traffic to a designated next hop instead of directly being routed to the internet.

## Network Watcher
* **Connection Monitor -** Check the network connectivity between machines. These can be in Azure or on your on-premises environments.
* **IP Flow Verify -** This can be used to check if a packet is allowed or denied to or from a virtual machine. If a packet is being denied by a security group, you can see which rule is denying the packet.
* **Next Hop -** Here you can see the next route for a packet of data. This helps you understand whether the packet is being routed to the correct destination.
* **Connection troubleshoot -** Check the connection from  virtual machine to a virtual machine, FQDN, URL or IPv4 address.
* **NSG diagnostic -** Provides detailed information that helps to understand and debug the security configuration of the network.
* **NSG Flow Logs -** This helps to log information about the IP traffic that is flowing through an NSG.
* **Traffic Analytics -** Helps to provide visibility into user and application activity in cloud networks. 
