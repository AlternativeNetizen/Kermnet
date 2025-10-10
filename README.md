# Kermnet
Alternative to the internet

Framework to replace layer 2-4(OSI) of the internet

## **Why replace the internet?**

the modern internet mainly consists of centralized servers allowing users to connect to other users
Main issues with centralized servers:

1.ISPS hold a great deal of power over citizens and they abuse it, making customers pay enormous amounts compared to real cost of connecting that user to the internet

2.those central servers exist within countries therefor governments impose regulations over any services over the internet

3.Bad actors/authorities try to restrict your actions on the internet, disallowing any form of free speech or rights you have


## **What is Kermnet exactly?**

at core, its a large mesh network utilizing hard "tasks"(verifying other requests) to create basic rules in requests and incentive for nodes to work

nodes broadcast connections to other nodes/clients

every client holds a ledger of all/parts of every requests ever made, similar to any cryptographic system's (full and lightweight nodes), they themselves need to verify requests in order to make requests
clients need to verify a very small amount of requests to produce a request
Example:
client would need to cryptographically validate #z requests to send 1 request at x data rate with y data amount

why mining? why have a built in currency? why even verify requests on kermnet?

In-short, to give incentive for nodes to share connections with more clients
As a client validates it produces a very small amount of whatever digital unit currency(kerms), a small percentage of kerms mined by a client go to the node which gave it access to the larger mesh, this makes nodes care about reaching clients, this requires defining what a larger mesh is so every node isn't stealing a percentage of every other nodes kerms 

Larger Mesh: a mesh consisting of at least 50 nodes meshed together


### **Distribution of kerms upon request:**

every request has a client,host, and nodes in between

a client validates till it reaches the nessasary amount of kerms to pay each node on the way to the host, and the host themselves as the host needs to pay nodes on the way to the client in order to reply. obviously it routes by the least node amounts and varies how many node routes are used in parallel depending on how what data rate(bytes/kilobytes/megabytes/etc) its trying to send at. also pays exponentially more for higher data rates on nodes its already sending on

-this makes it more computationally expensive on a client to send requests to a very far or virtually unreachable host

-this makes it more computationally expensive on a client to ask a host to send replies at high data rates

this also makes sure clients can't flood nodes with extremely high data rates as they'd need to mine much more to do that



**Hosts'(Reciever) side of things:**
depending on what they want they could make the client(Sender) pay kerms for both send and reply or just send

in the case of the client paying for send and reply the host doesn't need to validate requests to interact with clients and the kerm cost burden is put on the clients

in the case of the client paying for send only the host does need to validate requests to interact with clients and the kerm cost burden is shared by the client and host



### **Addressing Crypto concerns:**

**multiple aspects of Kermnet are in place to ensure no one tries to actually trade with or invest in the built in kerms(currency)**

**1.its extremely inflationary,** due to kerms relying on validation of other kerms, as the computation power of computers increases they thus will produce exponentially more kerms, devaluing all other kerms

**2.its uncapped,** adding to the previous point, having no cap or limiting system to the kerms currency makes sure its price can never go up therefor would never be treated as an investment

**3.Kermnet will always be in the hands of the people,** as its an alternative that can be freely switched to and isn't forced, no system can be put in place against the people(the ones actually making it work since its peer-to-peer)

**4.I am open to any and all feedback,** any alert of issue or suggestion you can give me is my priority and will be made sure it assists in the development of Kermnet and its ensurance to staying open source, and for the good of the people.












### **Important Notes:**

1.a client shouldn't waste more than a few ms of mining to produce a request at a reasonable distance and reasonable data rate to host

2.this will most likely be based on the tried and tested CJDNS(networking stack)

3.amount of (unit currency)kerms will be uncapped, to discourage real life trading with it

4.nodes can set their own custom kerm price/rate

5.nodes can use wireless connections to reach clients as its just cheaper than wiring Ethernet or fiber to them

6.every client can be a node, every host can be a node. already mentioned incentives are given to both for being so

7.every node is technically also a client and host



Host and Client talking over nodes:
<img width="1080" height="1080" alt="Node bigger example" src="https://github.com/user-attachments/assets/1d3b579d-48da-4a0e-ac11-2696f47d6f1a" />






**Benefits**

1.Decentralized

2.Client is anonymous to host, vice versa; although you'd think every request's "connectionnumber,host public id,client public id,extradata" being exposed on ledgers would make it extremely public, due to both being able to change their (ipv6 address + public id) freely and nodes being in between most clients and hosts it causes no node to truly know if a request came from any other specific node, but only the general direction of it

3.It addresses a need of the people so has a slightly better chance of actually being adopted

4.Self regulated by nodes custom kerm rates

**5.due to the inflating nature of kerms due to interactions producing more kerms, its given reason to be spent immediately instead of hoarded.** 
6.its extremely difficult for any whales/corps/giants to buy up the system in any way to induce profits to themselves, as they'd need impossible amounts of money or impossible amounts of computation power


**Issues to be aware of:**

1.Higher Energy Consumption

2.If the first node you directly connect to is compromised then you can be tracked easier

3.its so anonymous hosts have to implement their own system for identifying and verifying users if permanence is required

4.My expertise is in radio and micro-controllers. I require more skill for this project

5.I don't have the resources to do this alone




YT video:
[![Kermnet](https://img.youtube.com/vi/2H-zGdBOiBY/maxresdefault.jpg)](https://www.youtube.com/watch?v=2H-zGdBOiBY)
