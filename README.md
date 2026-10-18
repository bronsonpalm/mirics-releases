# Mirics releases

Mirics follows Spotify playback and displays synchronized lyrics in a Lock Screen or CarPlay Dashboard Live Activity. CarPlay Live Activities require iOS 26 or later.

[Download the latest Mirics IPA](https://github.com/bronsonpalm/mirics-releases/releases/latest/download/Mirics.ipa) · [Release notes](https://github.com/bronsonpalm/mirics-releases/releases) · [SideStore source](https://github.com/bronsonpalm/mirics-releases/releases/latest/download/source.json)

The IPA is unsigned. Install and sign it with your own SideStore setup, keeping its Live Activity extension. This repository hosts the app files, icon, version metadata and checksums. The app source code stays local.

## Updates

Mirics 0.1.2 and later provide a **Get Mirics update** Shortcuts action. It checks the current public release, downloads a newer IPA, and verifies its size and SHA-256 before returning it to Shortcuts. SideStore handles signing and installation.

An update-enabled daily shortcut connects LocalDevVPN, waits five seconds, gets the Mirics update, passes it to SideStore **Install IPA** if a file was returned, runs **Refresh All Apps**, and disconnects LocalDevVPN. Each iPhone needs its own VPN/app action selections and personal automation. **Refresh All Apps** alone renews signatures; it does not install new app versions.

Publishing makes a release available for the next scheduled shortcut check. A manual, unlocked iPhone test successfully updated 0.1.2 to 0.1.3 and disconnected the VPN. Locked scheduled installation remains unverified and may need unlocking or confirmation. An interrupted shortcut can leave the VPN connected.
