# HP EliteBook Folio 9480m OpenCore EFI

Tested with OpenCore 1.0.6 on Monterey. Your mileage may vary; this config has
worked with Catalina in the past.

## Setup

You MUST generate new PlatformInfo data; you can use the GenSMBIOS utility for
this. I recommend identifying as a `MacBookPro11,4` for Monterey support, but
going for anything older you can use `MacBookAir6,2`.

## Note for El Capitan users

You might also need ACPIBatteryManager.kext; it's been a while since I needed
anything that old for a hackintosh, so you might be able to work without it.

## System configuration

A stock lowest configuration HP EliteBook Folio 9480m.

I use the generic Intel wifi card that came with the computer; yours likely still
has it installed too. This repo is currently configured to use itlwm.kext + HeliPort.
You can configure it to use AirportItlwm.kext, but this is not recommended as it is
less stable and prone to crashes on crappy WiFi connections.
