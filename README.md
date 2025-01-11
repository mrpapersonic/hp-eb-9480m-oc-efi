# HP EliteBook Folio 9480m OpenCore EFI

Tested with OpenCore 0.7.5 on OS X 10.9 Mavericks through macOS 12.0.1 Monterey.

## Note for El Capitan users

You also need ACPIBatteryManager.kext, El Capitan sucks.

## System configuration

A stock lowest configuration HP EliteBook Folio 9480m, with a different WiFi card.

I use a DW1560; you may want to choose a card that's natively supported by macOS instead.

## Kexts

A list of kexts to download is provided at `EFI/OC/Kexts/kext-list.txt`, alongside a file named `USBMapBundle.zip`. This zip file contains two kext(s) necessary for USB functionality. Unzip them both, as OpenCore won't boot without both of them (if you really need the extra space, look in the details below).

<details>
  <summary>More details on USBMapBundle.zip</summary>

  `USBMap.kext` is used for Catalina and up, and `USBMapLegacy.kext` is used for Mojave and lower.
  
  To optimize, remove the entry for the kext you don't need in `config.plist` and remove it from the Kexts folder.
  
  Congratulations! You now have 4 extra KB of space. Use it wisely, m'kay?
</details>

## CMOS reset notice
The CMOS intermittently gets reset on some restarts. I haven't bothered to fix this since I don't use macos nearly often enough to care about it. If anyone can figure out whats up with it, be my guest.
