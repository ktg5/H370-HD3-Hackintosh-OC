# ktg5's H370 HD3, i7-8700 Hackintosh EFI.
The EFI I use for my H370 HD3 i7-8700 Hackintosh.

[You can easily download the latest version of this EFI folder by looking in the releases section.](https://github.com/ktg5/H370-HD3-i7-8700-Hackintosh-OC/releases)

## Note.
My "custom" EFI is only built for systems running an Gigabyte H370 HD3, an i7-8700 CPU, and an Gigabyte RX 590 and with IGPU disabled. The reason why I'm talking about this is because in the config.plist, some settings may not match your configzation.

Also you'll have to run [CorpNewt's GenSMBIOS application](https://github.com/corpnewt/GenSMBIOS) because all strings in `PlatformInfo/Generic` are all set to blank MAY cause issues when using services like iMessage and other iCloud services on your system.

Any other things you want to change is all up to you, just make sure you know what you're doing.

If you are switching EFIs; I recommend you reinstall macOS as there could be some issues when booting your original installation of macOS if you have one.

## What does and doesn't work.
### Working:
* Networking (I don't remember anything I needed to do for this?...).
* HDMI, DVI, and DisplayPort (thanks to Lilu and WEG).
* HDMI and DisplayPort sound (thanks to AppleALC).
* Video editing, and Photoshopping.
* iMessage and other iCloud services.
### Not working:
* Sleep/Shutdown/Restart - Can be solved with [`FixShutdown-USB-SSDT`](https://github.com/dortania/OpenCore-Post-Install/blob/master/extra-files/FixShutdown-USB-SSDT.dsl) patch (Pretty sure I have to "properly" disable the "red" USB, I must find what `SB` it is.)
### Unknown:
* AirDrop and other WiFi services
