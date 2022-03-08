## Azure Virtual Private Network
### Point-to-Site VPN Connection
* **Secure Connection -** A Point-to-Site VPN connection is used to establish a secure connection between multiple client machines and an Azure virtual network via the Internet.
* **Few Clients -** This is ideal when you have a few clients that need to connect to the Azure virtual network.
* **VPN Connection -** The VPN Connection is created over SSTP(Secure Socket Tunneling Protocol) or IKEv2
* **Authentication -** You have different authentication methods that can be used - Certificates, Azure AD.
* **Gateway Subnet -** Your virtual Network needs to have a Gateway Subnet in place. Here the VM's that will manage the VPN will be deployed here.
* **Virtual Network Gateway -** This allows you to configure the Virtual Network Gateway Connection.
* **Certificates -** You can use self-signed certificates. The public key  of the root certificate is uploaded to the Azure Virtual network gateway.
* **Client -** Eacch client needs to hav the client certificate installed.
* **Point-to-site VPN Protocols**
  * **SSTP -** Developed by Microsoft. Here the encrypted tunnel is created over TCP port 443. Uses SSL/TLS protocol.
  * **OpenVPN -** This is an open standard createed to implement secure connections. Used the OpenSSL library.
  * **IKEv2 -** Internet Key Exchange uses the IPsec protocol suite to establish a secure connection.
* Below is a diagram from the Microsoft documentation on a sample scenario
![image](https://user-images.githubusercontent.com/60296821/147773851-28dcd83f-f0af-4710-a119-22ee24eb4234.png)

* Image reference -https://docs.microsoft.com/en-us/azure/vpn-gateway/vpn-gateway-howto-point-to-site-resource-manager-portal
* To implement a Point to Site VPN connection, you need to create a VPN Gateway in Azure.

## Site-to-Site VPN Connection
* A Site-to-Site VPN connection is used to establish a secure connection between an on-premise network and an Azure network via the Internet.
* **Secure Connection -** Here the connection is established over IPsec/IKE VPN tunnel.
* **Public IP Adress -** The On-premises network needs to have a software or hardware device that has a public routable IP address.
* **Gateway Subnet -** Your virtual network needs to have a Gateway subnet in place. Here the VM's that will manage the VPN will be deployed here.
* **Virtual Network Gateway -** This allows you to configure the Virtual Network Gateway Connection.
* **Local Network gateway -** This will be a representation of the On-premise network Configuration.
* 
* Below is a diagram from the Microsoft documentation on a sample scenario
![image](https://user-images.githubusercontent.com/60296821/147773921-b2ea047c-ec77-4c77-8e32-5a60e8304d98.png)
* Image reference - https://docs.microsoft.co **
**/en-us/azure/vpn-gateway/vpn-gateway-howto-site-to-site-resource-manager-portal
* On the on-premise side, you need to have a VPN device that can route traffic via the Internet onto the VPN gateway in Azure. The VPN device can be a hardware device like a Cisco router or a software device ( e.g Windows Server 2016 running Routing and Remote services). The VPN device needs to have a publically routable IP address.
* The subnets in your on-premise network must not overlap with the subnets in your Azure virtual network
* The Site-to-Site VPN connection uses an IPSec tunnel to encrypt the traffic.
* The VPN gateway resource you create in Azure is used to route encrypted traffic between your on-premise data center and your Azure virtual network.

## Virtual Network Gateway - Extra notes
### IKE Policy
* You can change the IKE policy configuration when it comes the Azure VPN gateway
* In your virtual network gateway, you can click on Connections to see your Site-to-Site connections
* Then click on the actual Site-to-Site connection
![image](https://user-images.githubusercontent.com/60296821/157166866-3f0bb3ca-b32a-4d3f-b328-e856fac9a8cc.png)
* This will actually open up the connection resource. Here go to the Configuration section
![image](https://user-images.githubusercontent.com/60296821/157166917-6bf76d82-86b1-4c11-b102-cce2d862cfcf.png)
* And then you can set IKE settings. For example, you can choose the encryption algorithm being used.
![image](https://user-images.githubusercontent.com/60296821/157167005-48505731-ba79-4003-86d1-470ef88c87e0.png)
* For further reference on configuring the IKE policy, one can refer to the below URL
* https://docs.microsoft.com/en-us/azure/vpn-gateway/ipsec-ike-policy-howto

### Policy vs Route-based VPN gateways
* When you create a Virtual network gateway , you can choose from either Route-based or Policy-based VPN’s. Normally you will choose Route-based VPN’s because these VPN’s have a lot of features over Policy-based VPN’s.
![image](https://user-images.githubusercontent.com/60296821/157167132-c3e9d265-6df0-4f23-8569-21d6336a231f.png)
* With Policy-based VPN’s , you can make use of traffic selectors to direct the traffic to different on-premises networks depending on the IP address ranges.
* For further reference on Policy-based VPN’s, one can refer to the below URL
* https://docs.microsoft.com/en-us/azure/vpn-gateway/vpn-gateway-connect-multiple-policybased-rm-ps

## Azure Virtual WAN
* https://docs.microsoft.com/en-us/azure/virtual-wan/virtual-wan-about

## Azure ExpressRoute
* **Connection -** Allows you to connect to your on-premises networks to microsoft cloud over a private connection.
* **Redundancy -** Each ExpressRoute circuit has two connection for Redundancy Purposes. Primary,Secondary - both in active active mode.
* **Peerings**
  * **Private Peering -** Azure Private peering allows you to connect to your azure virtual network resources.
  * **Microsoft Peering -** This allows you to connect to public services such as Microsoft 365 and Azure PaaS Services.
* **Gateway -** Your azure virtual network needs to have a virtual network gateway in place that is configured to use ExpressRoute.
* **FastPath -** This improves data path performance between on-premises network and the azure virtual network. Virtual Network Gateway - Ultra Performance, ErGw3AZ.
* **Global Reach -** This allows you to connect your on-premises networks together via their individual ExpressRoute circuits.
* **Bidirectional Forwarding Detection**
  * This is a feature available in Azure ExpressRoute. This helps to quickly detect a link failure between the Microsoft Enterprise Edge devices and the Azure ExpressRoute circuit.
  * For more information on Bidirectional Forwarding Detection , one can visit the below URL
  * https://docs.microsoft.com/en-us/azure/expressroute/expressroute-bfd

 
