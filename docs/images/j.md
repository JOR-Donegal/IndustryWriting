# Switch Configuration Sheet
In the documentation described so far, we've seen many aspects of what is required to plan and coordinate a heterogeneous project. We have to tie together the physical installation, power, server installation, and information on physically wiring it up.

So much of the project comes together at the network switch. On the smallest project, we are always going to have 2 switches for redundancy.
On a data centre type project, our configuration may be much more complex, per rack. Giving an example;

## Top of Rack switches (ToR) x 2
At the top of the rack, I'm going to have two switches which we refer to as the Top of Rack switches (ToR). When we cover Ethernet topologies, these will be the leaves in a leaf spine topology. In a virtualized data centre, most of our workloads will be tagged/trunked traffic. I may also connect the management interfaces of each server here. The client-side ports will be 10Gb/s or greater and for ease of wiring and cost, I use CAT6. The uplink ports will be higher speed, typically 50-100Gb/s.

## Back End (BE) switches x 2
Storage is a specialist application, and we will normally separate out the storage network devices and refer to them as back end (BE) switches. For redundancy, there will always be two back-end switches. Storage is demanding, and typically we specify for much higher throughput, 25-1000Gb/s. As you will see when we specify data centre servers, our server clusters must have shared storage. Every design is different, but this covers the basics.

## Management Switch x 1
Finally, we keep certain aspects of network management, separate. Most servers will have a baseboard management controller (BMC). In Dell equipment, this is an integrated Dell remote access controller (iDRAC). For Hewlett Packard, this is integrated lights out (ILO). And for IBM and others, it may be based on red fish. In any case, this is a critical interface for server management. This is where I would connect power management equipment (UPS, PDU), support equipment (KVM switches) etc.

The way we capture all this information so that is commonly held with the server team, the network team, the storage team, and everybody else, is to use a switch configuration sheet. Some vendors and contractors have complex spreadsheets back-end code that tend to be called in anti malware filters. Let's not go there!
In my opinion the best design sheets look like very simple relational databases.

I'll create a sheet for every type of option.
-	Switch devices
-	Connector Types
-	VLANs
-	Hosts
-	Ports
-	Loop avoidance
-	Link aggregation
-	Etc.

For Each unique switch device, I'll give it a unique identifier, and its own sheet. For every interface, every property I want to define is a drop-down box.
If I get this right, what would there be to stop me from building a network configuration using a Python script based on this sheet? One of the most effective and flexible ways to automate configuration, is to do it based on a specification or a database.

<figure>
<img src = "https://jor-donegal.github.io/IndustryWriting/images/fig3.png">
<figcaption>Fig 3. A simple switch configuration sheet.</figcaption>
</figure>




