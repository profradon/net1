--Sniffing
    There are four primary ways to capture traffic from a target device on a switched network: port mirroring, hubbing out, using a tap, and ARP cache poisoning.

 -port mirroring
    have access to the command-line or web-management interface of the switch on which the target computer is located. Also, the switch must support port mirroring and have an empty port into which you can plug your sniffer. you issue a command that forces the switch to copy all traffic on one port to another port

    Ciscoset span : <source port> <destination port>
    Enterasysset  : port mirroring create <source port> <destination port>
    Nortel        : port-mirroring mode mirror-port <source port> monitor-port <destination port>

 -hubbing out
    o hub out, all thats needed is a hub and a few network cables. Once you have your hardware, connect it as follows:
        1.Go to the switch the target device resides on and unplug the target from
        the network.
        2.Plug the target’s network cable into your hub.
        3.Plug in another cable that connects your analyzer to the hub.
        4.Plug in a network cable from your hub to the network switch to connect
        the hub to the network.

 -using a tap
    A network tap is a hardware device that you can place between two points on your cabling system in order to capture the packets between those two points. As with hubbing out, you place a piece of hardware on the network that allows you to capture the packets you need. The difference is that rather than using a hub, you use a specialized piece of hardware designed for net-work analysis.

 -ARP process
    when one computer wants to interract witht the other The
    transmitting computer first checks its ARP cache to see if it already has the Chapter 2MAC address associated with the IP address of the destination computer. If it does not, it sends an ARP request to the data link layer broadcast address FF:FF:FF:FF:FF:FF. Devices without the destination computer’s IP address simply discard this ARP request. The destination machine replies to the packet with its MAC address via an ARP reply

   ** ARP cache poisoning, sometimes called ARP spoofing, is the process of sending ARP messages to an Ethernet or router with fake MAC (layer 2) addresses in order to intercept the traffic of another computer
   -Using Cain & Abel(old anf for windows) ARP Poisoning	bettercap or arpspoof are better kali tools
   When attempting to poison the ARP cache you’ll need to collect certain information, including the IP address of your analyzer system, the remote system from which you wish to capture the traffic, and the router from which the remote system is downstream


Tapping into the wire
↓
Do your switches support mirroring?
├─ (Yes) → Use port mirroring
└─ (No)  ↓
Can a client be taken offline temporarily?
├─ (No)  → Use ARP cache poisoning
└─ (Yes) ↓
Do you have access to a tap?
├─ (Yes) → Use a tap
└─ (No)  → Hub out