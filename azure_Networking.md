## Azure Virtual Network
* The Azure Virtual Network service is used to define an isolated network in Azure. The virtual network can then be used to host your resources such as Azure virtual machines.
* The Azure virtual network gets assigned an address space which you specify when you create an Azure virtual network
* You can then add subnets to your Azure virtual network. This helps divide your network into more logical segments.
* An example is shown below of having multiple subnets.
  *  You could have one subnet named SubnetA in the virtual network to host your Web servers and another subnet to host the Database servers.

![image](https://user-images.githubusercontent.com/60296821/147773511-c4f76609-5048-403e-8a99-4e7a70ddb2ac.png)

* When you create a virtual machine in a virtual network, the virtual machine gets a Private IP address from the address space of the subnet is it launched in.
* **Network Interface:** - This is the interconnection between the virtual Machine and Virtual Network.

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

## Azure DNS
* **DNS Zone:-** This is used to host the dns regards for a particular domain. Here azure DNS can resolve host names in your public domain.
* **Private DNS Zone:-** Here domain names can be resolved within the virtual network.
* **Virtual Network Link:-** To ensure that the virtual network can use the private DNS zone, You need to link the virtual network to the zone.
* **AutoRegistration:-** Here DNS records for your virtual machines automatically created in the zone.

## Azure Load Balancer
* **Azure Availability Sets**
  * **Failure -** This feature helps to protect againist infrastructure failures.
  * **Unplanned Events -** This is when the underlying infrastucture fails Unexpectedly. the failure could be attributed to network, rack, local disk failures etc.,
  * **Planned Maintainance Activities -** Microsoft needs to do planned updates to the underlying physical infrastructure, which needs reboot on your virtual machine.
  * **Availibility Sets -** Here when a machine is assigned to am availability set it is assigned with a fault and Update domain.
* **Azure Availibility Zones**
  * **Failure -** This feature helps to provide better availability for your application by protecting them  from data center failure.
  * **Zones -** Each availibility zone is a unique physical location in a azure region. Zone consists of one or more data centers that has seperate power, cooling and network.
  * **Protection -** Hence physical seperation of the Availibility zones helps protect applications againist the data center failures.
  * **Availibilty -** Using Availibility zones you can be gaurenteed an availibility of 99.9% for your virtual Machines.
* **Azure LoadBalancer**
  * This is a service that is used to distribute incoming traffic across a group of backend resources or servers.
  * The service opereates at the layer 4 of the OSI model.
  * **Public Load Balancer -** This provides outbound connections for virtual machines inside the virtual network.
  * **Performance -** Load Balancer provides low latency and high throughput.
  * **Internal LaodBalancer -** This is used to loadbalance traffic inside a virtual network.
  * **Scaling -** The loadBalancer can scale up to millions of flows for a TCP and UDP applications.
  ## Basic SKU
  * This is a free version of the load Balancer.
  * The backend virtual Machines needs to be part of an availability set or a scale set.
  * Supports helath probes of TCP and HTTP.
  * Does not have an SLA.
  ## Standard SKU
  * Here there is an hourly charge.
  * The backend virtual Machines can also be independent machinesthat are part of a virtual network.
  * Supports helath probes of TCP, HTTP and HTTPS.
  * Has an SLA of 99.99%.
* **Azure LoadBalancer Components**
  * **Load-Balancing Rules -** This defines how incoming traffic is distributed to the instances in the backend pool. A rule maps a frontend IP and port to the backend IP adresses and ports.
  * **Health Probe -** This is used to determine the health status of the instances in the backend pool.
  * **Inbound NAT Rules -** This forwards incoming traffic sent to frontend IP and port to a specific virtual machine in the backend pool.
  * **Outbound Rules -** This enables instances in the backend to communicate with the internet.


## Azure Virtual Machine Scale Sets
* This service helps to create and manage group of load Balancer VM's.
* Here VM's can be created on demand.
* **Integration -** This service can be used with the Load-Balancer.
* **Virtual Machines -** Here VM's can be created based on the base image for the machine.
* **Rules -** You can use rules and conditions to scale out or scale in the number of virtual machines.
* **Availibility -** This service can automatically distribute the VM's across availability sets and Availability Zones.


## Azure Application Gateway
* **LoadBalancer -** This is a web traffic LoadBalancer. This makes routing decisions based on the attributes of the http requests.
* **AutoScaling -** The standard_v2 SKU supports autoscaling that can scale up and down based on traffic load patterns.
* **High Availibility -** For the standard_v2 SKU, the gateway can span multiple availability zones.
* **Layer 7 -** This loadbalancer operates at layer7.
### Azure Application Gateway Features
* **URL-based routing -** Here requests can be routed to the backend server pools based on the URL paths of the request.
* **Multiple-site Hosting -** Here you can configure routing based on the host name or domain name.
* **Rewrite HTTP headers or URl -** Here you can create rules to rewrite the headers and URL's.
* **Web application Firewall -** This feature helps to protect your web applications.
### Azure application Gateway Components
* **Frontend IP-Adress -** IP adress that is associated with the application gateway.
* **Listeners -** This is a logical entity that checks for incoming requests.
* **Requests Routing Rule -** The rule binds the listener, the backed server pool and the backend http settings.
* **HTTP Settings -** The settings determine how requests are routed to the backend servers.
* **Backend Pools -** This contains the backend servers.
* **Health Probes -** Here you can define your own custom health probes.


## Azure Traffic Manager
**Priority -** Here you can direct users to a secondary endpoint if the primary one fails.
**Weighted -** Here you can assign weights to each endpoint.
**Performance -** Here users can be directed to the closest endpoints with the lowest network latency.
**Geographic -** Here users are directed endpoints based on their geographic location.
**Multi-Value -** Here multiple endpoints are sent to the User.
**Subnet -** Here the endpoint is decided based on the subnet the user is located in.
**Endpoint Types**
* **Azure Endpoints -** This can PaaS cloud services, Web Apps, Web App Slots, Public IP Adresses that are assigned to virtual machines. Here the VM's ned to also have a DNS name assigned.
* **External Endpoints -** This can be Ip Adresses or FQDN's that are loacted outside of azure.
* **Nested Endpoints -** This can be another Azure traffic Manger Profile.

## Azure Front Door 
* It will provide the combined benefits of both Azure Traffic Manager & Azure Application Gateway. or more info follow the microsoft docs.

## Azure Virtual Network NAT
* NAT gateway helps to provide a common public IP for group of VM's

## Azure WAF Policy
* There are to kinds of modes Prevention and Detection.
* In Prevention mode the rule we apply will be executed.
* In detection mode it will print the logs to one storage account we create.

## Azure User defined Routes using Route Table
* Refer documentation for this.

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
