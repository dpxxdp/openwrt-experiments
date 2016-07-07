...having set up your router under manufacturer's guidelines and connected to it with an ethernet cable.

#Installing OpenWRT

Make sure you do this while connected via ethernet **NOT** wifi.

1. Download the binary (this is specific for the router version): https://downloads.openwrt.org/chaos_calmer/15.05/ar71xx/generic/openwrt-15.05-ar71xx-generic-tl-wdr3600-v1-squashfs-factory.bin
2. Visit the router's IP address (192.168.0.1) in your browser.  The manufacturer has set up a reasonably nice-looking http interface.  **Note:** you can find the Router's address in Network Preferences > Ethernet > Router.
3. In the http interface go to System Tools > Firmware Upgrade.
4. Choose the binary file you downloaded from OpenWRT.  Hit Upload. **Note:** when I tried this, the file wouldn't upload- turns out the name was too long, I renamed it to tl-wdr3600.bin and it worked.
6. It will take a few minutes and will restart automatically.  Disconnect and reconnect the ethernet cable after the bounce.  Your router is now running OpenWRT.
7. Again visit the router's address in your browser.  It should default to 192.168.1.1 this time.  Again you can check the Network Preferences if it's different.
8. You can log in with username: root and no password.  Be sure to set a password shortly after setting it up.  This is *not* your wifi password, but the password for the root account on the router's firmware.

#Setting up Wifi
1. In the OpenWRT browser interface, go to Network > Wifi.
2. The TL N600 router has two radios, broadcasting at 2.4Ghz and 5Ghz.
3. Click "Add" to add a network interface under each radio frequency.  Set the SSID (the name of your wireless network) and under Wireless Security set a secure WPA2-PSK password with a cipher of "auto".
