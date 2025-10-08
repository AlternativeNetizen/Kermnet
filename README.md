# Kermnet
Alternative to the internet


the modern internet mainly consists of centralized servers allowing users to connect to other users
Main issues with centralized servers:

1.ISPS hold a great deal of power over citizens and they abuse it, making customers pay enormous amounts compared to the costs of the real cost of connecting that user to the internet

2.those central servers exist within countries therefor governments impose regulations over any services over the internet

3.Bad actors/authorities try to restrict your actions on the internet, disallowing any form of free speech or rights you have


**What is Kermnet exactly?**

at core, its a large mesh network utilizing cryptographic hashes and proof of work to verify anything done on Kermnet

nodes broadcast connections to other nodes/clients

every client holds a ledger of all/parts of every requests ever made, similar to bitcoins (full and lightweight nodes), they themselves need to mine in order to make requests
clients need to mine a very small amount to produce a request

why mining? why crypto based? why even verify requests on kermnet?

In-short, to give incentive for nodes to share connections with more clients
As a client mines it produces a very small amount of whatever digital unit currency(kerms), a small percentage of kerms mined by a client go to the node which gave it access to the larger mesh, this makes nodes care about reaching clients, this requires defining what a larger mesh is so every node isn't stealing a percentage of every other nodes kerms 

Larger Mesh: a mesh consisting of at least 50 nodes meshed together


**Distribution of kerms upon request:**

every request has a client,host, and nodes in between

a client mines till it reaches the nessasary amount of kerms to pay each node on the way to the host, and the host themselves as the host needs to pay nodes on the way to the client in order to reply. obviously it routes by the least node amounts and varies how many node routes are used in parallel depending on how what data rate(bytes/kilobytes/megabytes/etc) its trying to send at. also pays exponentially more for higher data rates on nodes its already sending on

-this makes it more computationally expensive on a client to send requests to a very far or virtually unreachable host
-this makes it more computationally expensive on a client to ask a host to send replies at high data rates

this also makes sure clients can't flood nodes with extremely high data rates as they'd need to mine much more to do that



**Hosts' side of things:**
they also have to mine to send data to clients but are paid back in kerms by the clients at their own custom rate












**Important Notes:**

1.a client shouldn't waste more than a few ms of mining to produce a request at a reasonable distance and reasonable data rate to host

2.this will most likely be based on the tried and tested CJDNS networking stack

3.amount of (unit currency)kerms will be uncapped, to discourage real life trading with it

4.nodes can set their own custom kerm price

5.nodes can use wireless connections to reach clients as its just cheaper than wiring Ethernet or fiber to them

6.every client can be a node, every host can be a node. already mentioned incentives are given to both for being so

7.every node is technically also a client and host



Host and Client talking over nodes:
<img width="1080" height="1080" alt="Node bigger example" src="https://github.com/user-attachments/assets/1d3b579d-48da-4a0e-ac11-2696f47d6f1a" />






**Benefits**

1.Decentralized

2.Client is anonymous to host, vice versa; although you'd think every request's "connectionnumber,host public id,client public id,extradata" being exposed on ledgers would make it extremely public, due to both being able to change their (ipv6 address + public id) freely and nodes being in between most clients and hosts it causes no node to truly know if a request came from any other specific node, but only the general direction of it

3.It addresses a need of the people so has a slightly better chance of actually being adopted


**Issues to be aware of:**

1.Higher Energy Consumption

2.If the first node you directly connect to is compromised then you can be tracked

3.its so anonymous hosts have to implement their own system for identifying and verifying users if permanence is required

4.My expertise is in radio and micro-controllers. I require more skill for this project

5.I don't have the resources to do this alone
