# Briefing Other Suppliers

You may have to inform other suppliers of your requirements

There are very few projects where you will be the sole supplier of everything. Some very large companies may have this capability, but even in these cases, they must coordinate across multiple teams and business units. The requirement here is the same, you must be capable of briefing other suppliers as to what the requirements are for the components you are providing.

In this scenario, let us imagine that we are providing host servers, virtual machines, and their configuration and integration, a typical scope of supply in a private cloud exercise. We might need to brief a range of other suppliers on what we need from them, and what we will be providing to them. For example, the network supplier would need to know our physical connectivity requirements.

- Which cabinet will servers be located in? 
- How many connections do your servers need, with what properties? 
- Speed 
- Media type 
- Connectors 
- Will there be redundancy and if so, how will it work? 
- Are these connections access ports or trunks/tagged and are there implications? Many students miss this. A network supplier might block ports which behave like switches. 
- Any there any other port characteristics like QoS? 
- What port security settings should be provided?

On a real project, I would provide a network supplier with a physical diagram showing the interfaces of my server and what I require them to connect to.

Regarding logical connectivity:

- What VLANs should connections be in? 
- For tagged connections, what VLANs should be allowed and what should be pruned? 
- If you are using redundant connections, is there any sort of load balancing? 
- What network services exist, where, who supplies them? 
- DNS, DHCP, Time/NTP/PtP 
- Logging 
- AAA

The contents of a briefing document from one supplier to another, will depend on who is supplying what to whom. The example given here is one possible scenario only.