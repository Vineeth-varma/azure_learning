Your company currently the following resources deployed to their Azure subscription



You now have to ensure that webapp has the ability to access the resources in app-network. The implementation needs to ensure that costs are minimized. Which of the following would you implement for this requirement?





Explanation
You can use a private link to ensure that the web app can access the resources in the virtual network

Question 2: Incorrect
Your team has a virtual machine deployed onto Azure. Below are the network security groups that are attached to the network interface for the virtual machine. The subnet hosting the virtual machine does not have any network security groups assigned to it.


An application hosted on the virtual machine needs to access an Azure storage account. You have to add an outbound rule to the Network Security Group. Which of the following would you include in the rule?





Explanation
Here since we need to allow Outbound access to the Azure storage service, we can mention the destination as a service tag and we can choose the Service Tag as the storage service.


Question 3: Correct
Your company has a set of virtual machines hosted in their on-premises data center. And they also have Azure virtual machines in an Azure virtual network. They have created a Site-to-Site VPN between the on-premises network and the Azure virtual network. They want to periodically monitor the latency between the Azure virtual machines and the virtual machines hosted in their on-premises network. Which of the following can be used for this requirement?




Explanation
You can use the Connection Monitor tool to continuously monitor the connections between two endpoints.

Question 4: Correct
Your team is planning on using Azure Traffic Analytics to analyze the traffic flowing through various Azure virtual machines that are deployed as part of their subscription. Which of the following is required in Azure to support Azure Traffic Analytics? Choose 2 answers from the options given below.





Explanation
You need to have the Azure Storage account to store the NSG flow logs. And then to support the Traffic Analytics solution, you need to have a Log Analytics workspace in place.

Question 5: Correct
Your team has deployed a web application onto the Azure Web App service. The Azure Web App has been configured as a backend to an Azure Front Door instance. You have to configure a custom domain URL onto the Azure Front Door instance. You need to ensure to use a certificate for implementing HTTPS. Which of the following can be used for this requirement?




Explanation
You can have certificates deployed in Azure Key vault. The certificates can then be used for implementing HTTPS.

Question 6: Incorrect
Your company currently has the following Azure virtual networks in place


app-network1 has a virtual network gateway attached to it.

Currently the following on-premises Windows 10 clients have established Point-to-Site VPN connections with app-network1 via the virtual network gateway.

1) app-client1

2) app-client2

You then implement virtual network peering between app-network1 and app-network2. In the peering connection you ensure that “Allow gateway transit” and “Use remote gateway” are enabled accordingly.

Which of the following needs to be done to ensure that app-client1 can connect to app-network1 via the Point-to-Site VPN connection?





Explanation
If a change is made to the network topology, then you have to download the VPN client package again. And then install the VPN client again.

One can use the below URL for further reference to this.

https://docs.microsoft.com/en-us/azure/vpn-gateway/vpn-gateway-peering-gateway-transit

Question 7: Correct
Your company currently has two on-premises networks. One is located in Greater London and the other in the New York location. They are going to establish ExpressRoute circuits to connect the on-premises networks to individual Azure virtual networks. The office in Greater London will connect to an Azure virtual network in the UK South location. And the New York location will connect to an Azure virtual network in the East US location. You have to ensure that the on-premises servers in the Greater London location can connect to the on-premises servers in the New York location. Which of the following would you use as an ExpressRoute option for this requirement?




Explanation
This can be accomplished with the ExpressRoute Global Reach option.

One can use the below URL for further reference to this.

https://docs.microsoft.com/en-ca/azure/expressroute/expressroute-global-reach

Question 8: Incorrect
Your company currently has an on-premises data center in New York. They want to establish an ExpressRoute circuit with an Azure virtual network located in the East US location. The ExpressRoute connection needs to only make use of the Unlimited data plans. You have to ensure that the solution minimizes costs.

Which of the following would you use as the SKU for the ExpressRoute circuit?




Explanation
Here since we just need to connect to one Azure region and to save on costs, we can choose to go for the Local SKU of Azure ExpressRoute.

For more information on the pricing for Azure ExpressRoute , one can visit the below URL

https://azure.microsoft.com/en-us/pricing/details/expressroute/

Question 9: Correct
Your company has a set of Azure virtual machines located in an Azure virtual network. One of the machines named appvm is hosting a web-based application. There is a Network Security Group assigned to the subnet hosting appvm. The Network Security Group has around 50 rules. A third-party application needs to connect to the application hosted on appvm. But the third-party application is not able to connect to the virtual machine. You suspect it could be because of the Network Security Group rules. You have to resolve the issue and understand which rule is blocking the connection. Which of the following in Network Watcher can you use for this requirement?





Explanation
You can use NSG Diagnostics for this requirement. Here you can see the effect of the various rules in the Network Security Group.

Question 10: Correct
Your company has an Azure virtual network named app-network. The network contains the following subnets


The following virtual machines are defined in the virtual network


A Network security group is assigned to SubnetA that has the following rules in place

Inbound Rules


Outbound Rules


A Network security group is assigned to SubnetB that has the following rules in place

Inbound Rules


Outbound Rules


Would appvm1 be able to connect to port 80 on appvm2?





Explanation
Here we have to look at rules that would affect the incoming requests on appvm2.

appvm2 is part of SubnetB.

The NSG applied to SubnetB allows all Inbound virtual network traffic, hence the request would be allowed.

Question 11: Correct
Your company has an Azure virtual network named app-network. The network contains the following subnets


The following virtual machines are defined in the virtual network


A Network security group is assigned to SubnetA that has the following rules in place

Inbound Rules


Outbound Rules


A Network security group is assigned to SubnetB that has the following rules in place

Inbound Rules


Outbound Rules


Would appvm2 be able to connect to port 8080 on appvm1?



Explanation
Here we have to look at rules that would affect the incoming requests on appvm1.

appvm1 is part of SubnetA.

The NSG applied to SubnetA denies all traffic from within the virtual network apart from connections on port 80 and 443.

Question 12: Incorrect
Your company has an Azure virtual network named app-network1. An Azure Firewall resources has been deployed to the virtual network. The virtual network has the following subnets


All traffic from SubnetA is routed through the Firewall. You have to ensure that virtual machines deployed in SubnetA can connect to an external site http://cloudportalhub.com

Which of the following would you configure?




Explanation
You can add an application rule in the firewall to allow traffic to the external site.

Question 13: Correct
Your company has the following Azure virtual networks


You are planning on deploying an Azure Firewall resource to the East US location as part of the app-grp1 resource group.

Can you link the new Azure Firewall resource to app-network1 during deployment?



Explanation
When deploying the Firewall resource , the Azure Firewall resource needs to be in the same location and resource group as the Azure virtual network.

Question 14: Correct
Your company has the following Azure virtual networks


You are planning on deploying an Azure Firewall resource to the East US location as part of the app-grp1 resource group.

Can you link the new Azure Firewall resource to app-network2 during deployment?



Explanation
When deploying the Firewall resource , the Azure Firewall resource needs to be in the same location and resource group as the Azure virtual network. Here the resource group is different.

Question 15: Correct
Your company has the following Azure virtual networks


Can you link the new Azure Firewall resource to app-network3 during deployment?



Explanation
When deploying the Firewall resource , the Azure Firewall resource needs to be in the same location and resource group as the Azure virtual network. Here the location of the virtual network is different from the deployment location of the Azure Firewall resource.

Question 16: Correct
Your company currently has an on-premises network and an Azure virtual network. They are planning on deploying an ExpressRoute circuit to connect the on-premises network and the Azure virtual network. At the same time, they also want to deploy a Site-to-Site VPN as a backup connection incase the ExpressRoute connection fails.

Which of the following must be used as the routing type when it comes to the VPN gateway?



Explanation
When you have an ExpressRoute connection as the primary connection and Site-to-Site VPN as the backup, we need to use a Route-based VPN.

For more information on configuring these connections, one can visit the below link

https://docs.microsoft.com/en-ca/azure/expressroute/expressroute-howto-coexist-resource-manager

Question 17: Incorrect
Your company currently has an on-premises network and an Azure virtual network. They are planning on deploying an ExpressRoute circuit to connect the on-premises network and the Azure virtual network. At the same time, they also want to deploy a Site-to-Site VPN as a backup connection incase the ExpressRoute connection fails.

What is the minimum number of virtual network gateways that need to be configured?




Explanation
We need one virtual network gateway for the Site-to-Site VPN and the other for Azure Express Route.

Question 18: Incorrect
Your company currently has an Azure virtual network in place. They want to configure Point-to-Site VPN connections. Here the connections need to be authenticated via Azure Active Directory.

Which of the following needs to be configured in Azure Active Directory for this requirement?





Explanation
Here we need to ensure that we configure the use of an enterprise application. We need to make use of the Azure VPN enterprise application when it comes to Azure AD authentication.


Question 19: Incorrect
Your company currently has an Azure virtual network in place. They want to configure Point-to-Site VPN connections. Here the connections need to be authenticated via Azure Active Directory.

Which of the following must be select as the VPN tunnel type?




Explanation
Only OpenVPN is available when it comes to Azure AD authentication.

Question 20: Incorrect
Your company has just setup a Site-to-Site VPN connection . They want to be able to diagnose the different issues in the connection via the use of diagnostic logs.

Which of the following can be used to troubleshoot past events about unexpected VPN disconnections?






Explanation
You can get this information from TunnelDiagnosticLog

For more information on VPN diagnostics, one can visit the below link

https://docs.microsoft.com/en-us/azure/vpn-gateway/troubleshoot-vpn-with-azure-diagnostics

Question 21: Incorrect
Your company has just setup a Site-to-Site VPN connection . They want to be able to diagnose the different issues in the connection via the use of diagnostic logs.

Which of the following can be used to dig deeper into IPsec issues when it comes to VPN connections?






Explanation
You can get this information from IKEDiagnosticLog

For more information on VPN diagnostics, one can visit the below link

https://docs.microsoft.com/en-us/azure/vpn-gateway/troubleshoot-vpn-with-azure-diagnostics

Question 22: Correct
Your company has an on-premises network and an Azure virtual network. They want to establish a Sire-to-Site VPN connection between the on-premises network and the Azure virtual network. Which of the following needs to be created in Azure to setup the connection? Choose 2 answers from the options given below






Explanation
You need to create a Virtual network gateway and a Local network gateway resource.

For more information on Site-to-Site VPN connection, one can visit the below link

https://docs.microsoft.com/en-us/azure/vpn-gateway/tutorial-site-to-site-portal

Question 23: Correct
Your team has an Azure virtual network that is hosting a set of Azure virtual machines. You have to ensure that no connections can be made from the virtual machines to storage accounts in the East US location. The virtual machines should be able to connect to storage accounts in other regions.

Which of the following can be implemented for this requirement?





Explanation
Here since the connections are being made from the virtual machines to Azure storage accounts, we need to create an Outbound Rule. We only want to deny traffic to storage accounts in the East US location.

Question 24: Correct
Your company has an Azure subscription and an Azure AD tenant. The company has the following resources in Azure


A private endpoint is created for newapp. Which of the following is the record that gets created for the Azure Web App in Azure DNS?




Explanation
The Azure Web App will be registered in a separate Azure DNS private zone.

For more information on using private endpoints with Azure Web Apps, one can visit the below link

https://docs.microsoft.com/en-us/azure/app-service/networking/private-endpoint

Question 25: Incorrect
Your company has the following Public IP addresses deployed in their subscription


A NAT gateway named new-nat is going to be deployed to the subscription . The IP address and the NAT gateway resource are in the same region.

Can you use nat-ip1 as the public IP address for new-nat?



Explanation
The Azure Network NAT is only compatible with a Standard SKU public IP address

For more information on Virtual Network NAT, one can visit the below link

https://docs.microsoft.com/en-us/azure/virtual-network/nat-gateway/nat-overview

Question 26: Correct
Your company has the following Public IP addresses deployed in their subscription


A NAT gateway named new-nat is going to be deployed to the subscription . The IP address and the NAT gateway resource are in the same region.

Can you use nat-ip2 as the public IP address for new-nat?



Explanation
The Azure Network NAT is only compatible with a Standard SKU public IP address

For more information on Virtual Network NAT, one can visit the below link

https://docs.microsoft.com/en-us/azure/virtual-network/nat-gateway/nat-overview

Question 27: Correct
Your company has the following Public IP addresses deployed in their subscription


A NAT gateway named new-nat is going to be deployed to the subscription . The IP address and the NAT gateway resource are in the same region.

Can you use nat-ip3 as the public IP address for new-nat?



Explanation
The Azure Network NAT is only compatible with a Standard SKU public IP address

For more information on Virtual Network NAT, one can visit the below link

https://docs.microsoft.com/en-us/azure/virtual-network/nat-gateway/nat-overview

Question 28: Incorrect
Your company has the following Public IP addresses deployed in their subscription


You will be creating a Public Standard Load balancer in the North Europe location named app-load.

Can app-load use load-ip1 as the public IPv4 address?



Explanation
A Standard Load Balancer needs a Standard SKU Static Public IP address.

When you try to create a Public IP address as the Front End IP address for a Standard Load Balancer as shown below, you can see this as the requirement.


Question 29: Correct
Your company has the following Public IP addresses deployed in their subscription


You will be creating a Public Standard Load balancer in the North Europe location named app-load.

Can app-load use load-ip2 as the public IPv4 address?



Explanation
A Standard Load Balancer needs a Standard SKU Static Public IP address.

When you try to create a Public IP address as the Front End IP address for a Standard Load Balancer as shown below, you can see this as the requirement.


Question 30: Correct
Your company has the following Public IP addresses deployed in their subscription


You will be creating a Public Standard Load balancer in the North Europe location named app-load.

Can app-load use load-ip3 as the public IPv4 address?



Explanation
A Standard Load Balancer needs a Standard SKU Static Public IP address.

Question 31: Correct
Your company has the following Public IP addresses deployed in their subscription


You will be creating a Public Standard Load balancer in the North Europe location named app-load.

Can app-load use load-ip4 as the public IPv4 address?



Explanation
The Public IP address and the Load Balancer need to be in the same region.

Question 32: Incorrect
Your company has the following Azure Web Apps in place. All of them are part of the company’s Azure subscription


The Azure Web Apps are hosting the same instance of a web application. You have to deploy an Azure Traffic Manager profile. You have to ensure that clients get a list of Azure Web App endpoints and connect to the first available endpoint.

Which of the following would you choose as the routing method?





Explanation
Here since you want the clients to get a list of endpoints, you need to use the Multivalue routing method.

For more information on configuring the multi-value routing method, one can refer to the below URL

https://docs.microsoft.com/en-us/azure/traffic-manager/traffic-manager-configure-multivalue-routing-method

Question 33: Correct
Your company has the following Azure Web Apps in place. All of them are part of the company’s Azure subscription


The Azure Web Apps are hosting the same instance of a web application. You have to deploy an Azure Traffic Manager profile. You have to ensure that clients get a list of Azure Web App endpoints and connect to the first available endpoint.

Which of the following would you choose as the endpoint type in the Traffic Manager profile?




Explanation
Since here we need to have the Azure Web Apps as endpoints, we can make use of Azure endpoints.

Question 34: Incorrect
Your company has the following Azure Web Apps in place. All of them are part of the company’s Azure subscription


You have to deploy an instance of the Azure Application Gateway. You have to ensure that requests are routed as follows


Which of the following do you need to configure in Azure Application gateway for this requirement?




Explanation
Here you need to add rules based on URL-path based routing

For more information on request routing rules in Azure Application Gateway, one can refer to the below URL

https://docs.microsoft.com/en-us/azure/application-gateway/configuration-request-routing-rules

Question 35: Incorrect
Your company is planning on implementing the following infrastructure that looks at connecting their on-premises data center to an Azure virtual network.


They want to implement high availability for their NVA’s. Which of the following can be used for this requirement?





Explanation
Here you can use the Azure Standard Load Balancer to distribute traffic across the Network Virtual Appliances.

For more information on high availability for your NVA’s, one can refer to the below URL

https://docs.microsoft.com/en-us/azure/architecture/reference-architectures/dmz/nva-ha?tabs=cli

Question 36: Correct
Your company has the following infrastructure in place


Virtual network peering connections have been created between app-network1 and app-network2. And between app-network1 and app-network3.

Below the peering connection settings


Here the remote virtual network ID is

/subscriptions/6912d7a0-bc28-459a-9407-33bbba641c07/resourceGroups/architecture-grp1/providers/Microsoft.Network/virtualNetworks/app-network2


Here the remote virtual network ID is

/subscriptions/6912d7a0-bc28-459a-9407-33bbba641c07/resourceGroups/architecture-grp1/providers/Microsoft.Network/virtualNetworks/app-network3



Can virtual machines defined in app-network3 communicate with app-network1?



Explanation
Yes, since there is a peering connection between these networks , communication is possible.

Question 37: Incorrect
Your company has the following infrastructure in place


Virtual network peering connections have been created between app-network1 and app-network2. And between app-network1 and app-network3.

Below the peering connection settings


Here the remote virtual network ID is

/subscriptions/6912d7a0-bc28-459a-9407-33bbba641c07/resourceGroups/architecture-grp1/providers/Microsoft.Network/virtualNetworks/app-network2


Here the remote virtual network ID is

/subscriptions/6912d7a0-bc28-459a-9407-33bbba641c07/resourceGroups/architecture-grp1/providers/Microsoft.Network/virtualNetworks/app-network3

Can virtual machines defined in app-network2 communicate with app-network3?



Explanation
Here there is no peering connection between the networks.

Question 38: Incorrect
Your company has the following infrastructure in place


Virtual network peering connections have been created between app-network1 and app-network2. And between app-network1 and app-network3.

Below the peering connection settings


Here the remote virtual network ID is

/subscriptions/6912d7a0-bc28-459a-9407-33bbba641c07/resourceGroups/architecture-grp1/providers/Microsoft.Network/virtualNetworks/app-network2


Here the remote virtual network ID is

/subscriptions/6912d7a0-bc28-459a-9407-33bbba641c07/resourceGroups/architecture-grp1/providers/Microsoft.Network/virtualNetworks/app-network3

Can virtual machines defined in app-network2 communicate with machines defined in the on-premises network?



Explanation
Here the peering connection between app-network1 and app-network2 is configured to not use the remote virtual network gateway.

Question 39: Correct
Your company has an Azure virtual network named app-network with an IP address space of 10.0.0.0/16.

An Azure virtual named app-vm is deployed to the Azure virtual network.

An Azure DNS zone named cloudportalhub.com has been defined that has the following records


An Azure private DNS zone named cloudportalhub.com has been defined that has the following records.

The Azure private DNS zone has a virtual network link to app-network that has the setting of Auto-registration set to false.


Would requests from the Internet to www.cloudportalhub.com get resolved to 10.0.0.4?



Explanation
This is a private IP address that is part of the Azure Private DNS zone. Hence requests from the Internet would not get resolved to this IP address.

Question 40: Incorrect
Your company has an Azure virtual network named app-network with an IP address space of 10.0.0.0/16.

An Azure virtual named app-vm is deployed to the Azure virtual network.

An Azure DNS zone named cloudportalhub.com has been defined that has the following records


An Azure private DNS zone named cloudportalhub.com has been defined that has the following records.

The Azure private DNS zone has a virtual network link to app-network that has the setting of Auto-registration set to false.


Would requests from the Internet to www.cloudportalhub.com get resolved to 20.107.198.65?



Explanation
Yes, the requests would go to the Public defined Azure DNS zone. And IP address of 20.107.198.65 would be returned for www.cloudportalhub.com.

Question 41: Incorrect
Your company has an Azure virtual network named app-network with an IP address space of 10.0.0.0/16.

An Azure virtual named app-vm is deployed to the Azure virtual network.

An Azure DNS zone named cloudportalhub.com has been defined that has the following records


An Azure private DNS zone named cloudportalhub.com has been defined that has the following records.

The Azure private DNS zone has a virtual network link to app-network that has the setting of Auto-registration set to false.


Would requests from app-vm to www.cloudportalhub.com get resolved to 20.107.198.65?



Explanation
Here the requests would be resolved to the record in the private DNS zone.

Question 42: Correct
Your company has the following resources defined as part of their Azure subscription


app-network has an IP address space of 10.0.0.0/16. The network contains a subnet named SubnetA that has an IP address space of 10.0.0.0/24.

You have to ensure that appvm can only access appstore1. Which of the following would you include in the implementation for this requirement?





Explanation
Here you can create a private endpoint to app-network just for appstore1 , so that the virtual machine can just access this storage account. Just ensure that the Network Security Groups are managed for the virtual machine to not allow access onto the Azure Storage service.

Question 43: Incorrect
Your company has the following Azure virtual networks


There is a virtual network peering connection between app-network1 and app-network2

The following Azure virtual machines are defined in the virtual network


An Azure private DNS zone is defined named cloud2hub.com. Virtual Network links have been added to both virtual networks with Auto-registration enabled.

You then manually add an entry for appvm1 with an IP address of 10.1.0.5

Would appvm2 resolved appvm1 to the IP address 10.1.0.4?



Explanation
Since the IP address is now changed manually , this will override the registered DNS entry.

Question 44: Incorrect
Your company has the following Azure virtual networks


There is a virtual network peering connection between app-network1 and app-network2

The following Azure virtual machines are defined in the virtual network


When you delete appvm1, would the DNS zone automatically delete the record linked to appvm1?



Explanation
Here since we have manually added an entry, it will not manage the record anymore.

Question 45: Correct
Your team has deployed an Azure Application Gateway. An Azure Web App has been placed behind the Azure Application Gateway. Currently the Gateway has been configured to route requests to http://cloudportalhub.com to the Azure Web App sitting behind the Application Gateway instance.

You now have to configure another Azure Web App to site behind the Application Gateway instance. You have to ensure that requests made to http://cloud2hub.com are routed via the Gateway instance onto the new Azure Web App. Which of the following steps need to be implemented for this requirement? Choose 3 answers from the options given below.






Explanation
First add a backend pool for the new Azure Web App

Then add a listener to listen to requests on http://cloud2hub.com

Then add the routing rule to route requests from the new listener to the new backend pool.

Question 46: Correct
Your team has deployed an Azure Application Gateway. An Azure Web App has been placed behind the Azure Application Gateway. The following path-based routing rules have been defined


Which of the following rule will be applied for a request http://cloudportalhub.com/images/data/img1.jpg?





Explanation
When there are multiple rules, the first rule that matches the request will be applied.

For more information on the request routing rules, one can visit the below URL

https://docs.microsoft.com/en-us/azure/application-gateway/configuration-request-routing-rules

Question 47: Correct
Your team has deployed an Azure Application Gateway. An Azure Web App has been placed behind the Azure Application Gateway. The following path-based routing rules have been defined


Which of the following rule will be applied for a request http://cloudportalhub.com/data.txt?





Explanation
When there are multiple rules, the first rule that matches the request will be applied.

For more information on the request routing rules, one can visit the below URL

https://docs.microsoft.com/en-us/azure/application-gateway/configuration-request-routing-rules

Question 48: Correct
Your company has an Azure virtual network named app-network defined as part of their subscription. The virtual network has an IP address range of 10.0.0.0/16. The virtual network has a subnet named SubnetA.

Your team has deployed a set of virtual machines to the virtual network as shown below. The virtual machines are both deployed to SubnetA.


You have deployed a NAT gateway which has a public IP address of 51.143.218.12 to SubnetA.

Would both appvm1 and appvm2 use the same public IP address of 51.143.218.12 when making outbound calls to the Internet?



Explanation
Since the NAT gateway is assigned to the subnet, it would be used by both virtual machines.

Question 49: Correct
Your company has an Azure virtual network named app-network defined as part of their subscription. The virtual network has an IP address range of 10.0.0.0/16. The virtual network has a subnet named SubnetA.

Your team has deployed a set of virtual machines to the virtual network as shown below. The virtual machines are both deployed to SubnetA.


You have deployed a NAT gateway which has a public IP address of 51.143.218.12 to SubnetA.

You then go ahead and assign a public IP address of 51.143.218.1 to appvm2. Which IP address would be used by appvm2 when making outbound calls?




Explanation
appvm2 would continue to use the Public IP address assigned to the NAT gateway. This supersedes any Public IP resources assigned to the virtual machine.

Question 50: Incorrect
Your company has deployed two Azure Web Apps. The details are given below


Your team then create a Traffic Manager profile based on the performance routing method. Both of the Azure Web Apps have been added as endpoints to the Traffic Manager profile.

The DNS name for the traffic manager profile is http://app-traffic.trafficmanager.net

The DNS name for the Azure web apps are https://traffic-app1000.azurewebsites.net and https://traffic-app2000.azurewebsites.net respectively.

You have to ensure that requests for http://www.cloud2hub.com is routed via the Azure Traffic Manager. Which of the following would you implement for this requirement?




Explanation
First you need to add a CNAME record in your domain registrar that maps your domain name to the DNS name assigned to the Traffic Manager profile.

For Azure Web Apps, also ensure to set the custom domain names accordingly.
