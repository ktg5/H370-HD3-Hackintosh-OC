# ktg5's H370 HD3, i7-8700 Hackintosh EFI.
The EFI I use for my H370 HD3 i7-8700 Hackintosh.

(macOS Big Sur still doesn't work)

[You can easily download the latest version of this EFI folder by looking in the releases section.](https://github.com/ktg5/H370-HD3-i7-8700-Hackintosh-OC/releases)

## Notice (Feb. 22, 2021)
I've recently I decided to stop this project and move on from Hackintoshing. At times it can be too compliated and I can't get passed somethings due to how unspported my system is for this. If you'd like to continue this projec on your own, you can fork this project and mess with it.

Thanks for sticking around and looking at this repo.

## Note.
My "custom" EFI is only built for systems running an Gigabyte H370 HD3, an i7-8700 CPU, and an Gigabyte RX 590 and with IGPU disabled. The reason why I'm talking about this is because in the config.plist, some settings may not match your configzation.

Any other things you want to change is all up to you, just make sure you know what you're doing.

## Installation process.
If you already have an installation of Clover or OC, I recommend to save yours as a backup in case anything goes wrong when using my config. And if you already installed macOS onto your system that has some other EFI -- I recommend you reinstall macOS as there could be some issues when booting your original installation of macOS if you have one.

First, you'll want to mount the EFI on your macOS drive and install the latest Opencore release from [here](https://github.com/acidanthera/OpenCorePkg/releases).

Second, copy and paste/replace the files from this repo into your Opencore installation. Make sure to include the config and delete the dummy config stored in your Opencore installation. Also you'll have to run [CorpNewt's GenSMBIOS application](https://github.com/corpnewt/GenSMBIOS) because all strings in `PlatformInfo/Generic` are all set to blank MAY cause issues when using services like iMessage and other iCloud services on your system.

Lastly, test it out for yourself and enjoy!

## What does and doesn't work.
### Working:
* Networking (I don't remember anything I needed to do for this?...).
* HDMI, DVI, and DisplayPort (thanks to Lilu and WEG).
* HDMI and DisplayPort sound (thanks to AppleALC).
* Video editing, and Photoshopping.
* iMessage and other iCloud services.
* Sleep/Shutdown/Restart - I know how to work with ACPI now!
### Unknown:
* AirDrop and other WiFi services - should work if you have a supported WiFi card.
