1. Packet List 
    The top pane displays a table containing all packets in th current capture file. It has columns containining the packet number, the relative time the packet was captured, the source and destination of thepacket, the packet’s protocol, and some general information found in the packet.

all DNS traffic is blue, and all HTTP traffic is green

-- this  expression will capture only traffic with a source IP address of 192.168.0.10 and a source or destination port of 80:
src 192.168.0.10 && port 80


tcp[13] & 32 ==                 32TCP packets with the URG flag set
tcp[13] & 16 ==                 16TCP packets with the ACK flag set
tcp[13] & 8 ==                  8TCP packets with the PSH flag set
tcp[13] & 4 ==                  4TCP packets with the RST flag set
tcp[13] & 2 ==                  2TCP packets with the SYN flag set
tcp[13] & 1 ==                  1TCP packets with the FIN flag set
tcp[13] == 18                   TCP SYN-ACK packets
ether host 00:00:00:00:00:00   Traffic to or from your MAC address
(replace with your MAC)         
!ether host 00:00:00:00:00:00  Traffic not to or from your MAC address
(replace with your MAC)
broadcast                       Broadcast traffic only
icmp                            ICMP traffic
icmp[0:2] == 0x0301             ICMP destination unreachable, host unreachable
ip                              IPv4 traffic only
ip6                             IPv6 traffic only
udp                             UDP traffic only