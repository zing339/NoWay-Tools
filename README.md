<img width="180" height="180" alt="WOW" src="https://github.com/user-attachments/assets/8875e905-1cd6-4cf8-8214-60e49b1125a3" />
# NoWay Malware - Windows Stealer

## Overview
This project demonstrates a Discord-oriented stealer written in Go. The malware targets Windows systems and leverages `fodhelper.exe` for privilege escalation. Upon gaining elevated privileges, it accesses all user sessions across every disk.

## Features
- **Anti-debugging**: Terminates debugging tools
- **Anti-antivirus**: Disables Windows Defender and blocks access to antivirus websites
- **Anti-VM**: Detects and exits in virtual machine environments
- **Browser Stealing**:
  - Logs, cookies, credit cards, history, downloads from 37 Chromium-based browsers
  - Logs, cookies, history, downloads from 10 Gecko browsers
- **Clipboard Cloner**: Replaces clipboard with crypto address when copying other addresses
- **Common Files Extraction**: Steals sensitive files from common directories
- **Discord 2FA Backup Codes**: Captures Discord 2FA backup codes
- **Discord Injection**:
  - Intercepts login/register/2FA requests
  - Captures backup code requests
  - Monitors email/password changes
  - Blocks QR code logins and device viewing
- **Fake Error Handler**: Tricks users into thinking program crashed
- **Game Data Extraction**: Epic Games, Uplay, Minecraft (14 launchers), Riot Games
- **Startup Persistence**: Ensures execution at system startup
- **System Information Gathering**: CPU/GPU/RAM/IP/location/Wi-Fi networks
- **Token Extraction**: From Discord apps, Chromium/Gecko browsers
- **UAC Bypass**: Privilege escalation for multi-user data collection
- **Wallet Extraction**: 10 local wallets + 55 wallet extensions
- **Wallet Injection**: Captures mnemonic phrases/passwords from 2 crypto wallets

## Disclaimer
**Educational Purpose Only**: This tool is strictly for research and educational purposes. Use responsibly and ensure compliance with applicable laws.

### Usage Responsibilities
- You alone are responsible for all actions taken with this tool
- Misuse is strictly prohibited
- Creator (hackirby) disclaims all responsibility for usage

### No Liability
- Creator not liable for damages or legal consequences
- Includes direct, indirect, incidental, consequential, or punitive damages

### No Support
- Creator provides no support for malicious activities
- All inquiries regarding misuse will be ignored

### Acceptance
- Using the tool signifies acceptance of these terms
- Do not use if disagreeing with disclaimer terms

## Implementation Details
The malware uses multiple modules with specific responsibilities:

```go
// Example module structure
type Module struct {
    Name        string
    Description string
    Function    func() error
}

var modules = []Module{
    {"anti_debug", "Terminates debuggers", antiDebug},
    {"anti_vm", "Detects VMs", detectVM},
    // Additional modules...
}
```

Each module handles specific data extraction techniques:
- Browser data via browser-specific parsers
- System information via Windows API calls
- Clipboard manipulation via Windows clipboard API
- Process enumeration via Win32 API

## Technical Execution Flow
1. Anti-analysis checks
2. Privilege escalation via fodhelper.exe
3. Multi-user session enumeration
4. Data extraction from each user session
5. Data exfiltration via encrypted channels
6. Persistence setup

## Security Considerations
- Uses encrypted communications (TLS 1.3)
- Implements code signing verification
- Validates file integrity before execution
- Implements secure key storage

## Deployment Methods
- MSI installer
- PowerShell execution
- Scheduled task creation
- WMI event subscription

## Monitoring & Reporting
- Real-time logging to remote server
- Screenshot capture (interval configurable)
- Keylogger implementation
- Webcam capture (if available)

## Response Handling
- Graceful termination handlers
- Silent process deletion after exfiltration
- Cleanup of artifacts post-execution

This implementation provides a comprehensive framework for Windows credential theft with modular design allowing easy extension of new data sources.
