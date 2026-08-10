Namerer + Supervisorer
A two-application Windows controller inventory, player-assignment, and HidHide isolation suite for arcade cabinets, emulation hosts, and Steam Remote Play systems.
Official product information: https://troylien.me/namerer.html
Buy and download on Gumroad: https://troylien.gumroad.com/l/NamererAndSupervisorer
Buy and download on Payhip: https://payhip.com/b/2RgDi
Overview
Namerer creates persistent, human-readable controller identities on the computer that owns the physical hardware. Supervisorer consumes those names on the game computer and stores a separate ordered controller allow-list for each game, emulator executable, or core. The applications can run together on one PC or coordinate through a shared folder on a private local network.
Key capabilities
Persistent controller names using SDL paths, Windows PnP information, adapter ports, and controller-specific inventory slots.
Live button, axis, and D-pad feedback for identifying physical controllers.
Profiles for games, emulator executables, and cores with numeric Player 1, Player 2, Player 3... ordering.
Per-profile observed-player calibration that corrects RetroArch joypad indices before a core launches.
Optional per-core RetroArch A/B face-button remapping applied to every selected player without changing other cores.
Allow-list isolation: all present unselected endpoints are hidden, including controllers that exist only on a Steam streaming client.
Late-arriving endpoint reconciliation and cached-scan recovery for temporary HidHide access-denied conditions.
Exact HidHide snapshot and restore on both computers, with lease-expiry and Steam-client-exit recovery.
SHA-256-verified update installers for direct-download releases.
Architecture
controller_names.json: durable named controller inventory written by Namerer and read by Supervisorer.
controller_runtime.json: Namerer's live machine identity, heartbeat, and current controller status.
controller_isolation_request.json: leased, machine-targeted, ordered player request written by Supervisorer.
controller_isolation_status.json: Namerer's acknowledgement, active state, and recovery/error status.
LocalAppData: machine-specific HidHide mappings and recovery snapshots remain local and are never treated as portable identities.
Tested and confirmed controller hardware
USB NES controller.
USB SNES controller.
Steam Controller.
PlayStation 3 controller with its working Windows driver.
Xbox / XInput controller.
Nintendo Wii Remotes.
Nintendo GameCube controllers through a Mayflash GameCube adapter.
Other Windows DirectInput or XInput gamepads may work, but have not been advertised as tested and confirmed. Adapter models, clones, drivers, and hardware revisions can differ.
Same-PC setup
Install Namerer, Supervisorer, and HidHide on the gaming computer.
Use Namerer to name controllers and pair local endpoints.
Use Supervisorer to add executables/cores and assign named controllers in player order.
Arm the selected profile before launching the game or emulator.
Split-PC Steam Remote Play setup
On the controller/client PC, install Namerer and HidHide; name every controller and complete Steam Isolation Setup.
On the game/host PC, install Supervisorer and HidHide; configure games, emulators, cores, and player assignments.
Point both programs to the same private-network shared folder. Keep Namerer running on the controller PC.
Arm isolation in Supervisorer before starting the stream. Namerer hides client-side extras before Steam can forward them, while Supervisorer handles host-local and VirtualHere endpoints.
Important HidHide behavior
Close the HidHide Configuration Client before using either application's endpoint tools. Only one HidHide configuration client can hold the control device at a time. A stale Present=NO endpoint is a cached Windows device interface and should not be mapped. Some devices may require a reconnect before another already-running program notices a visibility change.
Requirements
Windows 10/11 x64 on Intel or AMD hardware.
HidHide on every PC where endpoints must be hidden.
Working Windows drivers for every controller before setup.
A private LAN shared folder or mapped drive for split-PC coordination.
Distribution
The customer download is one package containing NamererSetup-X.X.X.exe and SupervisorerSetup-X.X.X.exe. Install the appropriate component on each computer. The compiled customer package does not require Python. Direct-download builds use separate HTTPS update manifests so each installed component can update itself independently.
Copyright (c) 2026 Troy Lien. All rights reserved.
