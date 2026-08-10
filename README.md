# 🎮 Namerer + Supervisorer
Version 1.2.5 for Windows 10/11 x64
Name every controller once, choose the player order for each game, emulator, or core, and temporarily hide every controller that was not selected.
Official product information: https://troylien.me/namererSupervisorer.html
Buy and download on Gumroad: https://troylien.gumroad.com/l/NamererAndSupervisorer
Buy and download on Payhip: https://payhip.com/b/2RgDi
---
## What the suite solves
Large arcade and emulation systems can expose many controllers at once. Windows, Steam, and emulators may use generic device names, select the wrong controllers, or put the right controllers in the wrong player order. Namerer + Supervisorer turns the chosen profile into an ordered controller allow-list for that game.
## Two applications, one workflow
- **Namerer:** runs where the physical controllers are connected, provides live input identification, saves persistent custom names, and pairs those names with local HidHide endpoints.
- **Supervisorer:** runs where the games and emulators are installed, stores game/executable/core profiles, and assigns the named controllers to Player 1, Player 2, Player 3, and later positions.
- **Arm Isolation:** exposes only the controllers selected for the active profile and restores the previous HidHide state when the session ends.
The applications can run together on one gaming PC or coordinate across two PCs through a shared folder on a private local network.
## Key capabilities
- Persistent custom controller names and fixed inventory slots.
- Live button, axis, and D-pad feedback for identifying physical controllers.
- Separate controller profiles for games, emulator executables, and cores.
- Ordered Player 1, Player 2, Player 3... assignments.
- HidHide allow-list isolation that hides every present unselected endpoint.
- Client-side filtering for controllers that never appear as host endpoints.
- Saved RetroArch observed-player calibration for correcting joypad indices before launch.
- Optional per-core RetroArch A/B face-button swap for every selected player.
- Automatic restoration after disarming, Steam-client exit, normal shutdown, or lease expiry.
- Customer-approved updates with SHA-256 installer verification.
## Tested and confirmed controllers
- USB NES controller
- USB SNES controller
- Steam Controller
- PlayStation 3 controller with its working Windows driver
- Xbox / XInput controller
- Nintendo Wii Remotes
- Nintendo GameCube controllers through a Mayflash GameCube adapter
Other Windows DirectInput or XInput gamepads may work, but are not advertised as tested and confirmed. Adapter models, clones, drivers, and hardware revisions can differ.
## Same-PC setup
1. Install Namerer, Supervisorer, and HidHide on the gaming PC.
2. Use Namerer to name the controllers and pair their local endpoints.
3. Use Supervisorer to add games, emulator executables, and cores, then assign controllers in player order.
4. Select the desired profile and click **Arm Isolation** before launching it.
## Split-PC Steam Remote Play setup
1. On the controller/Steam-client PC, install Namerer and HidHide, name every controller, and complete Steam Isolation Setup.
2. On the game/Steam-host PC, install Supervisorer and HidHide, then configure the games, emulators, cores, and player assignments.
3. Point both applications to the same shared folder on the private local network.
4. Keep Namerer running on the controller PC, arm the profile in Supervisorer, and then start the stream.
Namerer hides unwanted client-side controllers before Steam can forward them. Supervisorer simultaneously handles host-local and VirtualHere endpoints.
## RetroArch player order and GameCube controls
Supervisorer's Quick Controller Mapper can save the player position each selected controller actually controlled during a test. It writes the corrected joypad-index permutation before that RetroArch core launches.
For GameCube/Dolphin profiles, **Swap A/B for this RetroArch core** corrects the common face-button layout for every selected player without changing other cores.
## Requirements
- Windows 10 or Windows 11, 64-bit Intel/AMD (x64)
- HidHide installed on every PC where controller endpoints must be hidden
- Working Windows drivers for every controller before setup
- A private LAN shared folder or mapped drive for split-PC coordination
- Not compatible with 32-bit Windows; not a native ARM64 build
## Package
```text
NamererSetup-1.2.5.exe # Controller identification and client-side isolation
SupervisorerSetup-1.2.5.exe # Game profiles, player order, and host-side isolation
README.txt # Same-PC and split-PC setup guide
SHA256SUMS.txt # Release integrity values
```
## Updates
Each application can check troylien.me for its own newer Windows installer. An update runs only after customer approval and SHA-256 verification.
## Important HidHide note
Close the HidHide Configuration Client before using endpoint setup or arming isolation. Only one HidHide configuration process can hold the control device at a time. A stale Present=NO endpoint is a cached Windows device interface and should not be mapped.
## Publishing note — remove before posting publicly
Keep the application source private unless Troy deliberately chooses a source-available license. A public GitHub page may contain documentation, release notes, issue tracking, and links to paid downloads without publishing the source code or paid installer for free.
Copyright (c) 2026 Troy Lien. All rights reserved.
