This binary is intended to be run on background and scan for NFC tags.
This program first retrieve the list of playlists present on the squeezebox server.

When a new NFC tag is recognized the Tag ID is compared to all names present in the playlist. If the ID is found in playlist name, this one is loaded and played on the player. The mac address of the player has to be given as command line argument.

When the NFC Tag is removed, Stop command is sent to the player.

# Build

Use meson/ninja for compilation .
Depends on libcurl, libnfc and cJSON.
* https://curl.haxx.se/libcurl/
* https://github.com/nfc-tools/libnfc
* https://github.com/DaveGamble/cJSON

```
$ meson . build && cd build && ninja
```

# License

GPLv3

Only test with libnfc and libnfc acr122_usb driver.

