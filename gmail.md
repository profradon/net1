1. --The "Reverse Proxy" (The Modern Phish)
         Evilginx2 on your Kali VM.

        How it works: You send a link to your test phone. The link points to your Kali machine, which acts as a "middleman" between the phone and the real Google login page.

        The Magic: The phone logs in to the real Google. Your Kali machine "sniffs" the Session Cookie (the digital "VIP pass" that keeps you logged in).

        The Result: You don't even need the password. You just paste that cookie into your own browser, and you are inside the Gmail account, bypassing MFA completely.

2. --Infostealers (The Malware Path)
        Since you were asking about APKs earlier, this is the "payload" method.

        The Mechanism: You trick the test phone into installing a malicious app.

        The Goal: The app doesn't wait for the user to type a password. It goes straight to the browser's database on the phone and "steals" all the saved passwords and active session tokens.

        Rust Connection: Many modern "Stealers" are actually being rewritten in Rust because it's harder for Antivirus software to detect than older C++ malware.