# HP EliteBook Folio 9480m OpenCore EFI

Tested with OpenCore 0.7.5 on OS X 10.9 Mavericks through macOS 12.0.1 Monterey.

## Note for El Capitan users

Because El Capitan sucks, you have to use ACPIBatteryManager.kext. I don't know why, and don't really care why; it just needs it for some reason.

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
Due to a bug in a recent version of HP's BIOS, the CMOS gets reset every time you restart.

This can be fixed by just updating the BIOS; it rolls back to a 2018 version, and you should be good to go.
