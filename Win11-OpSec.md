# Windows 11 Operation-Security

## Stopping a Windows11 machine from being discoverable on a local network

- **Set the network to Public.** Go to **Settings → Network & internet → Wi‑Fi or Ethernet**, click your connection, and choose **Public network**. This alone turns off discovery and sharing for that network, so it's probably the main thing you changed back then.
- **Turn off discovery and sharing everywhere.** Open **Settings → Network & internet → Advanced network settings → Advanced sharing settings**. Under both *Private* and *Public* networks, turn off **Network discovery** and **File and printer sharing**. Under *All networks*, turn off **Public folder sharing**.
- **Remove any folders you shared.** Press Win+R, type `fsmgmt.msc` and press Enter, then open **Shares**. Leave anything ending in `$`, like `C$`, `ADMIN$` or `IPC$`, because Windows creates those itself. If you see any other share, such as a folder you shared, right-click it and choose **Stop Sharing**.
- **Undo the discovery services.** A common guide for showing a PC on the network tells you to set these services to Automatic. Press Win+R, type `services.msc` and press Enter. Find **Function Discovery Resource Publication** and **SSDP Discovery**, set each one's Startup type to **Manual**, and click **Stop**.
- **Turn off SMB 1.0 if it's on.** Old guides often have you enable it. Search Start for **Turn Windows features on or off**, then uncheck **SMB 1.0/CIFS File Sharing Support**. It's an old, insecure protocol, so it's worth turning off either way.
- **Optional: disable NetBIOS.** Open Control Panel → **Network and Sharing Center → Change adapter settings**. Right-click your adapter and choose **Properties**, then open **Internet Protocol Version 4 → Properties → Advanced → WINS** tab. Select **Disable NetBIOS over TCP/IP**. This stops the PC's name from being announced on older networks.
