---
{"publish":true,"created":"2025-08-20T21:23:16.808+01:00","modified":"2025-09-23T20:59:41.455+01:00","published":"2025-09-23T20:59:41.455+01:00","cssclasses":""}
---


## Intention
This Runbook will guide you through the process of configuring Linux Mint on a customer system.

### Target Audience
Repairers skilled in IT repairs. A basic understanding of Linux & alternative operating systems is required to complete this Runbook.

## Pre-Requisites
* **The customer must know what they are getting into** - that is, they know that they're going to have a big learning curve and that a lot of stuff is going to be different.
* **IT Disclaimer & Alternative Operating System Disclaimer signed & countersigned**
* Ideally **Alternative OS Take-Home sheet completed**

## Required Equipment
* Installation USB for Linux Mint
	* In desired architecture - likely x86_64
* (if optical drive) Test CD / DVD for functionality verification
* (optional) User's new SSD / HDD for installation
	* (optional) Caddy to house original SSD / HDD for data retrieval

## Steps
1. Before anything else: **Validate with the customer that their backup is known working!**
	* A common pitfall would be to clone the disk with Bitlocker still enabled. Data on this backup would likely be irretrievable from Linux. 
2. Check for known hardware incompatibilities: google the make and model of the system (or constituent parts), any accessories the customer has, etcetera. The Take-Home Sheet can be a big help here.
3. Validate Bitlocker **disabled** in Windows
	* This is particularly important if you intend to use the "new disk" method, so you can still access files on the original disk.
4. Reboot to UEFI. Validate Secure Boot setting, ensure USB Disk boot enabled.
	* Secure Boot is supported on newer Linux Mint versions; we would encourage it being turned on if available.
	* Remember, if you can't figure out how to get to the UEFI, hold shift while clicking "Restart" in Windows. Then `Troubleshoot -> Advanced options -> UEFI Firmware Settings -> Restart`
5. (if using new drive) Turn off system. Remove existing drive, install new OS drive.
6. Insert Linux Mint Install USB and boot system to **live** installation.
	* Method will vary by system - see if there's a boot menu or similar.
7. Validate functionality of the following:
	* [ ] Display - can I change brightness? Is it running at full resolution / refresh rate? Might need to install proprietary driver.
		* [ ] Graphics acceleration - can I play back a 4K Youtube clip without stuttering?
	* [ ] Keyboard - are all the keys working? Can I change the backlight if one is installed?
	* [ ] Wi-Fi - can I see networks? Can I connect to one? Do I have internet access?
	* [ ] Bluetooth - can I connect to a device?
	* [ ] Optical - can I play back a DVD?
	* [ ] Audio - is sound working? What about the microphone?
	* [ ] Webcam - open Cheese; can I see myself?
	* [ ] Sleep - can I put the computer to sleep and wake it up again? Does closing the lid work?
	* [ ] Trackpad - do multi-touch gestures work as expected?
	* [ ] Biometrics - does the fingerprint reader work?
	* [ ] Backup (if the customer brought it along) - can I access it?
8. Hand system to Customer. Let them fiddle with the system and start to get to know it - this will be what it looks like if they give the go-ahead.
9. **This is the last opportunity for the customer to back out.**
10. Install Linux Mint using the installer wizard. Settings as appropriate - use correct keyboard layout, install multimedia codecs, erase disk, etc.
11. Reboot into new installation
12. Check for additional / proprietary drivers in _Driver Manager_; check for updates in _Update Manager_. (Show the Customer how to do updates!)
13. Re-validate functionality (particularly sleep)
14. Briefly show Customer around OS. Perhaps install a package or two - maybe their favoured web browser?
	* Explain how to install new software; where printers are configured; how to connect to their home Wi-Fi network; how to change mouse sensitivity; how to perform software updates; how to log out; how to turn off.
15. Hand system back to Customer. **Runbook completed**