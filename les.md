broadcast traffic
    
    bassicall yh like sending packets to all ports on a network segnment, regardless whether port is a hub (physival lvl of the OSI where packets are sent to all ports all the time but only used by the port defined in the header of the packet) or a switch (level 2 of the OSI model. it reads the layer 2 header information in the packet and, using the CAM table as reference, determines to which port(s) to send the packet).
    the highest possible IP addy in an IP network range is is usually reserved to act as the broadcast addy. for a network configured with 192.168.0.xxx IP range and a 255.255.255.0 subnet mask, the address 192.168.0.255 is the broadcast address.

    The extent to which broadcast packets travel is called the broadcast domain, which is the network segmentwhere any computer can directly transmit to another computer without going through a router

multicast raffic

    Multicast is a means of transmitting a packet from a single source to multiple destinations simultaneously. The primary method of implementing multicast is via an addressing scheme that joins the packet recipients to a multicast group If you see an IP address in the 224.0.0.0 to 239.255.255.255 range, it is most likely multicast traffic.

unicast

    A unicast packet is transmitted from one computer directly to another. The details of how unicast functions depend on the protocol using it. For example, consider a device that wishes to communicate with a web server. This is a one-to-one connection, so this communication process would begin with the client device transmitting a packet to only the web server.