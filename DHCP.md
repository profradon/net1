Since DNS is the "Phonebook," DHCP (Dynamic Host Configuration Protocol) is the "Receptionist."

When you connect your iPhone XR or your Kali VM to a network, it doesn't automatically know what its IP address should be. DHCP is the service that automatically hands out that info so you don't have to type it in manually

-----The 4-Step "DORA" Process

--When a device joins a network, it goes through these four stages:

D - Discover: Your phone "shouts" (broadcasts) to the whole network: "Is there a DHCP server here? I need an IP!"

O - Offer: The DHCP server (usually your router) hears the shout and replies: "I'm here! I have an opening at 192.168.1.50. Do you want it?"

R - Request: Your phone replies: "Yes, please! I'll take 192.168.1.50."

A - Acknowledge: The server says: "Got it. It's yours for the next 24 hours (the Lease Time). Here is your Subnet Mask and DNS info too."

                               **-how it works
The "Order of Operations"
Think of it like this:

DHCP First: You walk into school and connect to the Wi-Fi. Your iPhone XR asks, "Can I have a seat?" DHCP says, "Yes, you are 10.0.0.5."

DNS Second: You open Safari and type google.com. Your phone asks, "Where is google.com?" DNS says, "It's at 142.250.190.46."

The Connection: Your phone (at 10.0.0.5) sends a request directly to Google (at 142.250.190.46).