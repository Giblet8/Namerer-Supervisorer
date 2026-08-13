# 🎮 Namerer + Supervisorer
Version 1.3.2 for Windows 10/11 x64 - released 08.11.2026
Name every controller once, choose the player order for each game, emulator, or core, and temporarily hide every controller that was not selected.
Official product information: https://troylien.me/namererSupervisorer.html
Watch the demonstration video: https://www.youtube.com/watch?v=brB5V0cKNMY
Support Gib's Arcade on Patreon: https://patreon.com/GibsArcade
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
- Core-wide or controller-specific RetroArch A/B face-button swaps.
- Ordered virtual-controller bridge for selected USB NES, USB SNES, and generic DirectInput pads.
- Controller input-engine recovery between consecutive streamed games without restarting Namerer.
- Automatic verified Snes9x Port 2 multitap setup for three to five selected game players.
- Auto-scrolling Supervisorer status messages when the complete result does not fit the window.
- Automatic restoration after disarming, Steam-client exit, normal shutdown, or lease expiry.
- Paid-safe update notices that open the official product page without publicly hosting installers.
## Tested and confirmed controllers
- USB NES controller
- USB SNES controller
- Steam Controller
- PlayStation 3 controller with its working Windows driver
- Xbox / XInput controller
- Nintendo Wii Remotes
- Nintendo GameCube controllers through a Mayflash GameCube adapter
Other Windows DirectInput or XInput gamepads may work, but are not advertised as tested and confirmed. Adapter models, clones, drivers, and hardware revisions can differ.
## Tested and confirmed emulators / cores
Test environment: RetroArch 1.22.2 for Windows x64.
- Nintendo GameCube games in RetroArch using `cores\dolphin_libretro.dll`, confirmed with Super Smash Bros and ordered four-player isolation.
- Nintendo NES games in RetroArch using `cores\nestopia_libretro.dll`, confirmed with NES P1, NES P2, SNES P1, and GameCube P1 in order.
- Confirmed core-wide and controller-specific A/B remapping, including leaving NES/SNES pads native while swapping only GameCube P1 in the NES profile.
- Nintendo SNES games in RetroArch using `cores\snes9x_libretro.dll`, confirmed with four correctly ordered controllers and automatic verified Snes9x multitap setup.
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
## RetroArch player order and controller remapping
Supervisorer's Quick Controller Mapper can save the player position each selected controller actually controlled during a test. It writes the corrected joypad-index permutation before that RetroArch core launches.
A profile can swap A/B for every selected controller or only for individually checked controller slots. These choices affect only that RetroArch core.
Selected USB NES/SNES and generic DirectInput pads can be mirrored into separate ordered virtual Xbox controllers. Namerer Setup includes the official signed Nefarius ViGEmBus 1.22.0 installer.
AntiMicroX can remain open for extra hotkeys, but gameplay and D-pad keyboard mappings must be disabled because keyboard input has no player identity.
## Requirements
- Windows 10 or Windows 11, 64-bit Intel/AMD (x64)
- HidHide installed on every PC where controller endpoints must be hidden
- Working Windows drivers for every controller before setup
- A private LAN shared folder or mapped drive for split-PC coordination
- Not compatible with 32-bit Windows; not a native ARM64 build
## Package
```text
NamererSetup-1.3.2.exe # Controller identification and client-side isolation
SupervisorerSetup-1.3.2.exe # Game profiles, player order, and host-side isolation
README.txt # Same-PC and split-PC setup guide
SHA256SUMS.txt # Release integrity values
```
## Updates
Each application checks troylien.me for a newer-version notice. After customer approval it opens the official product page, where existing buyers can sign in to Gumroad or Payhip. Paid installers are not hosted on the public website.
## Important HidHide note
Close the HidHide Configuration Client before using endpoint setup or arming isolation. Only one HidHide configuration process can hold the control device at a time. A stale Present=NO endpoint is a cached Windows device interface and should not be mapped.
## Project links
GitHub: https://github.com/Giblet8/Namerer-Supervisorer
---
## Need Steam ROM Manager library metadata synchronization?
Custom SteamRM Library Syncer synchronizes the Steam ROM Manager collection metadata needed by a receiving client PC at startup without copying games, ROMs, artwork, or the entire Steam configuration folder.
View Custom SteamRM Library Syncer on GitHub: https://github.com/Giblet8/CustomSteamRMLibrarySyncer
Copyright (c) 2026 Troy Lien. All rights reserved.
