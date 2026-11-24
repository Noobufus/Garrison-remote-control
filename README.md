# Garrison Automation Client

For the Roblox game Idle Mafia Game

Software exclusive to members of the Bingus family

A Windows-based automation client designed to improve Garrison management. The application connects to a Discord bot through a WebSocket relay, allowing authorized users to execute predefined Garrison commands remotely.

## Features

### Remote Garrison Management
- **Station All:** Automatically navigates to a specified territory and stations available crew members.
- **Recall All:** Recalls stationed crew members through a predefined sequence.
- **Discord Integration:** Receive and execute supported commands through the connected Discord bot.
- **Device Pairing:** Connect individual computers to their corresponding Discord users.

### Automated Puzzle Detection
- Detects supported in-game Bot Checks using Windows OCR.
- Reads and processes puzzle instructions automatically.
- Verifies successful completion through an on-screen confirmation.
- Continues the Garrison workflow after successful verification.

### Integrated Setup Wizard
- Configure mouse click positions through a graphical interface.
- Supports separate calibration for Station All and Recall All.
- Pause and resume calibration using keyboard shortcuts.
- Preview saved positions before running automation.
- Saves click positions locally for future sessions.

### Connection & Startup
- Automatically reconnects after temporary network interruptions.
- Remembers previously paired devices.
- Optionally launches and connects when signing in to Windows.
- Supports Cloudflare Tunnel and Cloudflare Access authentication.
- Protects locally stored credentials using Windows DPAPI.

### Macro Compatibility
- Supports configurable hotkeys for external automation scripts.
- Automatically pauses and resumes compatible macros around Garrison operations.
- Manages game window focus before executing supported commands.

### Security & User Control
- Remote automation must be explicitly enabled by the user.
- Only predefined automation commands are accepted.
- Authentication failures and revoked credentials stop the connection.
- Click coordinates and OCR processing remain local to the user's computer.
- Remote orders are denied if the Roblox window is not focused or in the background.

## Installation

1. Download the latest Windows release.
2. Extract the ZIP archive.
3. Keep `GarrisonClient.exe` and the `_internal` folder together.
4. Launch `GarrisonClient.exe`.
5. Configure the relay connection and pair your device.
6. Use the integrated setup wizard to calibrate click positions.
7. Enable remote automation when ready.

## How It Works

**Discord Command → WebSocket Relay → Garrison Client → Roblox**

The Discord bot sends an authorized command through the relay. The client receives the request, performs the corresponding sequence of mouse and keyboard actions, handles Bot Checks if encountered, and reports the operation's result.

## Notes

- The client must remain running and connected to receive remote commands.
- Automatic startup does not automatically enable remote automation.
- Click positions may need recalibration if the Roblox window layout or display configuration changes.
- The application is an independent community project and is not affiliated with Roblox or the developers of *Idle Mafia Game*.
