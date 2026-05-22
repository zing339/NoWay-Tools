<img width="180" height="180" alt="WOW" src="https://github.com/user-attachments/assets/8875e905-1cd6-4cf8-8214-60e49b1125a3" />

Skuld StealerGo-written Malware targeting Windows systems, extracting User Data from Discord, Browsers, Crypto Wallets and more, from every user on every disk. (PoC. For Educational Purposes only)
Table of Contents

About the project

This proof of concept project demonstrates a "Discord-oriented" stealer implemented in Go. The malware operates on Windows systems and use fodhelper.exe technique for privileges elevation. By elevating privileges, the malware gains access to all user sessions on every disk
Features:

    antidebug: Terminates debugging tools.
    antivirus: Disables Windows Defender and blocks access to antivirus websites.
    antivm: Detects and exits when running in virtual machines (VMs).
    browsers:
        Steals logins, cookies, credit cards, history, and download lists from 37 Chromium-based browsers.
        Steals logins, cookies, history, and download lists from 10 Gecko browsers.
    clipper: Replaces the user's clipboard content with a specified crypto address when copying another address.
    commonfiles: Steals sensitive files from common locations.
    discodes: Captures Discord Two-Factor Authentication (2FA) backup codes.
    discordinjection:
        Intercepts login, register, and 2FA login requests.
        Captures backup codes requests.
        Monitors email/password change requests.
        Intercepts credit card/PayPal addition requests.
        Blocks the use of QR codes for login.
        Prevents requests to view devices.
    fakerror: Trick user into believing the program closed due to an error.
    games: Extracts Epic Games, Uplay, Minecraft (14 launchers) and Riot Games sessions.
    hideconsole: Module to hide the console.
    startup: Ensures the program runs at system startup.
    system: Gathers CPU, GPU, RAM, IP, location, saved Wi-Fi networks, and more.
    tokens: Extracts tokens from 4 Discord applications, Chromium-based browsers, and Gecko browsers.
    uacbypass: Grants privileges to steal user data from others users.
    wallets: Steals data from 10 local wallets and 55 wallet extensions.
    walletsinjection: Captures mnemonic phrases and passwords from 2 crypto wallets.


Disclaimer
Important Notice: This tool is intended for educational purposes only.

This software, referred to as skuld, is provided strictly for educational and research purposes. Under no circumstances should this tool be used for any malicious activities, including but not limited to unauthorized access, data theft, or any other harmful actions.
Usage Responsibility:

By accessing and using this tool, you acknowledge that you are solely responsible for your actions. Any misuse of this software is strictly prohibited, and the creator (hackirby) disclaims any responsibility for how this tool is utilized. You are fully accountable for ensuring that your usage complies with all applicable laws and regulations in your jurisdiction.
No Liability:

The creator (hackirby) of this tool shall not be held responsible for any damages or legal consequences resulting from the use or misuse of this software. This includes, but is not limited to, direct, indirect, incidental, consequential, or punitive damages arising out of your access, use, or inability to use the tool.
No Support:

The creator (hackirby) will not provide any support, guidance, or assistance related to the misuse of this tool. Any inquiries regarding malicious activities will be ignored.
Acceptance of Terms:

By using this tool, you signify your acceptance of this disclaimer. If you do not agree with the terms stated in this disclaimer, do not use the software.

