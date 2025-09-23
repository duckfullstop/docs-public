---
{"publish":true,"created":"2025-08-20T23:10:20.076+01:00","modified":"2025-09-23T20:59:09.086+01:00","cssclasses":""}
---

## Intention
This Runbook will guide you through the process of configuring ChromeOS Flex on a customer system.

### Target Audience
Repairers skilled in IT repairs. A basic understanding of alternative operating systems is required to complete this Runbook.

## Pre-Requisites
* **The customer must know what they are getting into** - that is, they know that they're going to have a big learning curve and that a lot of stuff is going to be different.
* **IT Disclaimer & Alternative Operating System Disclaimer signed & countersigned**
* Ideally **Alternative OS Take-Home sheet completed**
* The system must be **x86_64**. ARM64 is not presently supported by ChromeOS Flex.

## Required Equipment
* Installation USB for ChromeOS Flex
	* Only available in x86_64
* (optional) User's new SSD / HDD for installation
	* (optional) Caddy to house original SSD / HDD for data retrieval

## Resources
* ChromeOS Flex Installation Guide: [support.google.com](https://support.google.com/chromeosflex/answer/11552529?sjid=17173899618332271556-EU)
* Review the Hardware Support section of the "Differences" page: [support.google.com](https://support.google.com/chromeosflex/answer/11542901?sjid=17173899618332271556-EU)
## Steps
1. Before anything else: **Validate with the customer that their backup is known working!**
	* A common pitfall would be to clone the disk with Bitlocker still enabled. Data on this backup would likely be irretrievable from ChromeOS. 
2. Check for known hardware incompatibilities: google the make and model of the system (or constituent parts), any accessories the customer has, etcetera. The Take-Home Sheet can be a big help here.
	* Use the Certified Models list: [support.google.com](https://support.google.com/chromeosflex/answer/11513094?sjid=17173899618332271556-EU) - If it's on this list, that will shortcut you substantially.
3. Validate Bitlocker **disabled** in Windows
	* This is particularly important if you intend to use the "new disk" method, so you can still access files on the original disk.
4. Reboot to UEFI. Validate Secure Boot setting, ensure USB Disk boot enabled.
	* Secure Boot is supported **and recommended** on ChromeOS. Only disable if it's causing you an issue.
	* Remember, if you can't figure out how to get to the UEFI, hold shift while clicking "Restart" in Windows. Then `Troubleshoot -> Advanced options -> UEFI Firmware Settings -> Restart`
5. (if using new drive) Turn off system. Remove existing drive, install new OS drive.
6. Insert ChromeOS Flex USB and boot system.
	* Method will vary by system - see if there's a boot menu or similar.
7. Select "Try it First" on the "Start using ChromeOS Flex" screen. You'll need to sign in with a google account.
8. Validate functionality of the following:
	* [ ] Display - can I change brightness? Is it running at full resolution / refresh rate? Might need to install proprietary driver.
		* [ ] Graphics acceleration - can I play back a 4K Youtube clip without stuttering?
	* [ ] Keyboard - are all the keys working? Can I change the backlight if one is installed?
	* [ ] Wi-Fi - can I see networks? Can I connect to one? Do I have internet access?
	* [ ] Bluetooth - can I connect to a device?
	* [ ] Audio - is sound working? What about the microphone?
	* [ ] Webcam - open Cheese; can I see myself?
	* [ ] Sleep - can I put the computer to sleep and wake it up again? Does closing the lid work?
	* [ ] Trackpad - do multi-touch gestures work as expected?
	* [ ] Backup (if the customer brought it along) - can I access it?
9. Hand system to Customer. Let them fiddle with the system and start to get to know it - this will be what it looks like if they give the go-ahead.
10. **This is the last opportunity for the customer to back out.**
11. Click the time on the taskbar, then click Sign Out.
12. At the bottom of the sign-in screen, select Install ChromeOS Flex, and follow the instructions.
13. Reboot into new installation. Have customer sign into their Google account.
14. Re-validate functionality (particularly sleep)
15. Briefly show Customer around OS. 
	* Explain how to install software; where printers are configured; how to connect to their home Wi-Fi network; how to change mouse sensitivity; how to perform software updates; how to log out; how to turn off.
16. Hand system back to Customer. **Runbook completed**