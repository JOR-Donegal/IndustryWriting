# Network Services
A technical description explaining how the infrastructure will integrate with the core services and what services can be provided from the infrastructure for the virtualization servers”

We may be working in VMWare or Hyper-V; I change this around from module to module and in different assignments. 

In all my modules, the network services are provided from Windows Servers using Active Directory. I could also use Linux to provide these services, this is general guidance only!

Avoid generalities, a technical description does not need to explain what AD, DHCP and DNS are, but rather how they are applied and implemented in this project. You are writing for a peer.

As an example, it is expected that there will be two AD servers on any local site. If there is a central data center, these will synch with one (?) at the data center. Some description of the services which run on the servers would be expected; where is the DNS, DHCP, AAA, WDS, WSUS and how do they work from the perspective of high availability. How does time work?

Discuss the directory. Trees of multiple domains? Groups? Policies?

Do we mention file servers synching with the data center, BranchCache/DFS/Storage Spaces? Or do we use volume copy techniques?

I would include:

- A brief introduction. 
- A definition of scope. 
- A description of the existing domain, DCs and details of any change to be made. 
- The services which will be provided (AAA, DHCP, DNS, NTP, etc.) to the hosts and VMs.

I would then describe some of:

- Any testing or remediation to be done before the project commences. 
- The final desired result and replication topology. I would have a diagram illustrating this. 
- The improvements to availability, BC, DR, and any other emergent technical benefit. 
- Security. 
- Any rollback or contingency plans.