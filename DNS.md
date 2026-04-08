DNS is a goldmineee

DNS is often the first thing a pentester attacks: (pentest first)

DNS Reconnaissance: By querying a company's DNS, you can find hidden subdomains like dev.company.com or vpn.company.com, which might be less secure.

DNS Spoofing / Cache Poisoning: This is where you "lie" to a DNS server. You tell it that google.com is actually your Kali IP address. If the server believes you, anyone using that DNS will be sent to your malicious site instead of the real Google.

DNS Exfiltration: Since DNS traffic is rarely blocked by firewalls, hackers can "hide" stolen data inside DNS queries to sneak it out of a network. This is something you could technically write a Rust tool to do!

