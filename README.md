## some news (macOS 11 support with OC 0.6.4???)
A new release of OC got released today -- 0.6.4. This new update has the following listed in the release info, "Added `BlacklistAppleUpdate` to fix macOS 11 broken update optout". Since this is a new feature that literally has "BlacklistAppleUpdate" in it's name and is discribed as "...to fix macOS 11 broken update optout", this feature might help me with updating to macOS 11. We'll just have to find out.

# ktg5's H370 HD3, i7-8700 Hackintosh EFI.
The EFI I use for my H370 HD3 i7-8700 Hackintosh.

[You can easily download the latest version of this EFI folder by looking in the releases section.](https://github.com/ktg5/H370-HD3-i7-8700-Hackintosh-OC/releases)

## Note.
My "custom" EFI is only built for systems running an Gigabyte H370 HD3, an i7-8700 CPU, and an Gigabyte RX 590 and with IGPU disabled. The reason why I'm talking about this is because in the config.plist, some settings may not match your configzation.

Any other things you want to change is all up to you, just make sure you know what you're doing.

## Installation process.
If you already have an installation of Clover or OC, I recommend to save yours as a backup in case anything goes wrong when using my config. And if you already installed macOS onto your system that has some other EFI -- I recommend you reinstall macOS as there could be some issues when booting your original installation of macOS if you have one.

First, you'll want to mount the EFI on your macOS drive and install the latest Opencore release from [here](https://github.com/acidanthera/OpenCorePkg/releases). Make sure to remove all the files in /Kexts, /Drivers (BUT LEAVE "OpenRuntime.efi", THIS COMES FROM ONLY THE LATEST OPENCORE RELEASE AND GETS UPDATED).

Second, copy the files from this repo into your Opencore installation. Make sure to include the config and delete the dummy config stored in your Opencore installation. Also you'll have to run [CorpNewt's GenSMBIOS application](https://github.com/corpnewt/GenSMBIOS) because all strings in `PlatformInfo/Generic` are all set to blank MAY cause issues when using services like iMessage and other iCloud services on your system.

Lastly, test it out for yourself and enjoy!

## What does and doesn't work.
### Working:
* Networking (I don't remember anything I needed to do for this?...).
* HDMI, DVI, and DisplayPort (thanks to Lilu and WEG).
* HDMI and DisplayPort sound (thanks to AppleALC).
* Video editing, and Photoshopping.
* iMessage and other iCloud services.
### Not working:
* Sleep/Shutdown/Restart - Can be solved with [`FixShutdown-USB-SSDT`](https://github.com/dortania/OpenCore-Post-Install/blob/master/extra-files/FixShutdown-USB-SSDT.dsl) patch (I have no idea how to manually do this, no one will help me...)
### Unknown:
* AirDrop and other WiFi services
