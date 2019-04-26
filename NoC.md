###NoC###

1 . A network-on-chip (NoC) is a packet-switching network embedded on a chip, typically interconnecting intellectual property cores in systems-on-chip.

2 . A NoC typically consists of routers, network interfaces (NIs) and links.

![NoC](/home/rishu/Pictures/pic1.jpg  "NoC")

The figure shows how the routers, NI, coherency nodes and links are organized. This is a toplogy of 4 * 4 mesh, composed of 16 tiles. A tile houses one router, one network interface and one core. 


3 . A router directs traffic between nodes according to a specified switching method,flow control policy, routing algorithm and buffering policy.

4 . A network interface (NI) serves to convert messages between the different protocols used by routers and cores.

5 . Another imporant purpose of the NI is to decouple computation from communication, allowing use of both infrastructures independent of each other.

6 . A link is composed of a set of wires and interconnects two routers in the network. A link may consist of one or more logical or physical channels, each of which is composed of a set of wires.

7 . The switching method defines how data is sent from a source to a destination node. . Packet switching is the most common technique in NoCs. In packet switching, routers communicate through packets or flits. Flits (flow control units) are the atomic units that form packets and streams.

8 . A flow control policy determines how packets move along the NoC and how resources such as buffers and channel bandwidth are allocated.

9 . Virtual channels (VCs) are often used in flow control, to improve
performance by avoiding deadlocks and reducing network congestion. VCs multiplex a single physical channel over several logically separate channels with individual and independent buffer queues.

10 . A dead-lock is caused by a cyclic dependency between packets in the network, where nodes are waiting to access each other’s resources.

11 . In livelock, packets do continue to move through the network, but they do not advance to their destination.

12 . The routing algorithm determines for a packet arriving at a router’s input port which output port to forward it to. The output port is selected according to the routing information embodied in the header of a
packet.

13 .  The buffering policy defines the number, location and size of buffers, which are used to enqueue packets or flits in the router in case of congestion.
