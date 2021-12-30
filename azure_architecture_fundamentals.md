## Virtual Machines

**Choosing the size for the virtual machine** - Remember that the size of the virtual machine plays an important role in both the cost and performance you get for your virtual machine.
If you are looking at the Free services provided by Azure - https://azure.microsoft.com/en-us/free/

**Costing for a virtual machine** - Remember that costing for a virtual virtual machine depends on several factors, such as time as it runs for, the region used for hosting the virtual machine, the underlying operating system.
* If you don't need the virtual machine running for a certain duration of time, you can always go ahead and stop the virtual machine. This will ensure you don't get charged for the compute cost of the virtual machine.
* To ensure you don't get charged for the compute costs for the virtual machine, the virtual machine must be in the Stopped (deallocated) state.
* Also keep a note that you will still be charged for other aspects of the virtual machine ( such as the disks attached to the virtual machine) , even if the virtual machine is stopped.

### Availability Sets
* When you host your virtual machines in Azure, you sometimes need to cater to the following
* An unplanned event wherein the underlying infrastructure fails unexpectedly. The failures could be attributed to network failures , local disk failures or even rack failures.
* Planned maintenance events , wherein Microsoft needs to make planned updates to the underlying physical environment. In such cases , a reboot might be required on your virtual machine.
* You can increase the availability of your application by making use of availability sets. Each virtual machine that is assigned to the availability set is assigned a separate fault and update domain.

**Fault domains** are used to define the group of virtual machines that share a common source and network switch. You can have up to **3** fault domains.

**Update domains** are used to group virtual machines and physical hardware that can be rebooted at the same time. You can have up to **20** update domains.

* If you deploy two or more virtual machines in an Availability set, you will get a guarantee of virtual machine connectivity to at least one virtual machine 99.95% of the time.

### Availability Zones
1. This features help provides better availability for your application by protecting them from datacenter failures.

2. Each Availability zone is a unique physical location in an Azure region.

3. Each zone comprises of one or more data centers that has independent power, cooling, and networking

4. Hence the physical separation of the Availability Zones helps protect applications against data center failures

5. Using Availability Zones, you can be guaranteed an availability of 99.99% for your virtual machines. You need to ensure that you have 2 or more virtual machines running across multiple availability zones

**An interesting fact** - Does it cost more to use an Availability Zone. Well no, you don't get charged separately for the use of Availability Zones.

Below is an excerpt from the Microsoft documentation

Reference - https://docs.microsoft.com/en-us/azure/availability-zones/az-overview
