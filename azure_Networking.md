## Azure Virtual Network
* The Azure Virtual Network service is used to define an isolated network in Azure. The virtual network can then be used to host your resources such as Azure virtual machines.
* The Azure virtual network gets assigned an address space which you specify when you create an Azure virtual network
* You can then add subnets to your Azure virtual network. This helps divide your network into more logical segments.
* An example is shown below of having multiple subnets.
  *  You could have one subnet named SubnetA in the virtual network to host your Web servers and another subnet to host the Database servers.

![image](https://user-images.githubusercontent.com/60296821/147773511-c4f76609-5048-403e-8a99-4e7a70ddb2ac.png)

* When you create a virtual machine in a virtual network, the virtual machine gets a Private IP address from the address space of the subnet is it launched in.

## Network Security Groups
* These are used to filter network traffic to and from Azure resources in an Azure virtual network.
* A network security group is attached to the network interface attached to the virtual machine.
* A network security group consists of Inbound rules that are used to control the traffic inbound into a virtual machine
![image](https://user-images.githubusercontent.com/60296821/147773633-dff3e853-3ebb-4b25-94cd-01b7f4949175.png)
* By default all traffic into a virtual machine is DENIED.
* You have explicitly add rules to allow traffic into a virtual machine
* There are also outbound rules to control the traffic flowing out of the virtual machine. By default all traffic outbound onto the Internet is allowed.

## Virtual Network Peering
* Virtual Network Peering is used to connect two Azure virtual networks together via the backbone network.
* Azure supports connecting two virtual networks located in the same region or networks located across regions.
* Once you enable virtual network peering between two virtual networks, the virtual machines can then communicate via their private IP addresses across the peering connection.
* You can also peer virtual networks that are located across different subscriptions.
* The virtual networks can't have overlapping CIDR blocks.

## Point-to-Site VPN Connection
* A Point-to-Site VPN connection is used to establish a secure connection between multiple client machines and an Azure virtual network via the Internet.
* Below is a diagram from the Microsoft documentation on a sample scenario
![image](https://user-images.githubusercontent.com/60296821/147773851-28dcd83f-f0af-4710-a119-22ee24eb4234.png)

* Image reference -https://docs.microsoft.com/en-us/azure/vpn-gateway/vpn-gateway-howto-point-to-site-resource-manager-portal
* To implement a Point to Site VPN connection, you need to create a VPN Gateway in Azure.

## Site-to-Site VPN Connection
* A Site-to-Site VPN connection is used to establish a secure connection between an on-premise network and an Azure network via the Internet.
* Below is a diagram from the Microsoft documentation on a sample scenario
![image](https://user-images.githubusercontent.com/60296821/147773921-b2ea047c-ec77-4c77-8e32-5a60e8304d98.png)
* Image reference - https://docs.microsoft.com/en-us/azure/vpn-gateway/vpn-gateway-howto-site-to-site-resource-manager-portal
* On the on-premise side, you need to have a VPN device that can route traffic via the Internet onto the VPN gateway in Azure. The VPN device can be a hardware device like a Cisco router or a software device ( e.g Windows Server 2016 running Routing and Remote services). The VPN device needs to have a publically routable IP address.
* The subnets in your on-premise network must not overlap with the subnets in your Azure virtual network
* The Site-to-Site VPN connection uses an IPSec tunnel to encrypt the traffic.
* The VPN gateway resource you create in Azure is used to route encrypted traffic between your on-premise data center and your Azure virtual network.
