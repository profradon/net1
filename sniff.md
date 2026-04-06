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
    