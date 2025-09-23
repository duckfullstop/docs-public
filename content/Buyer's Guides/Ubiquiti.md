---
{"publish":true,"created":"2023-07-13T18:47:57.000+01:00","modified":"2025-09-23T21:23:28.779+01:00","cssclasses":""}
---

> [!info]
> This buyer's guide was put together for a family friend who isn't particularly technologically versed.
> It's got a focus on a Protect setup, but you might find some of the recommendations here pertinent.
### Console
* Is network routing desired?
	* Yes:
		* **Dream Machine Pro** (~£400) - rackmount, comes **empty** with 1 HDD bay, built in 8 port ethernet switch and internet in / LAN out ports for gigabit routing
		* **Dream Machine Pro SE** (~£530) - as above, but 8 port ethernet switch is PoE
		* **Dream Router **(~£200) - standalone, built in WiFi AP and router with 4 ports, recording storage on MicroSD (which severely limits maximum storage, and can die with little to no warning)

	* No:
		* **Cloud Key Gen 2+ **(~£210) - standalone, comes with upgradable 1TB HDD, power via either PoE or USB (Qualcomm QuickCharge 3 brick required)
		* **Network Video Recorder **(~£320) - rackmount, comes **empty** with 4 HDD bays, power via standard kettle lead
		* **Network Video Recorder Pro** (~£530) - as above, but with 7 HDD bays, and stackable for extremely overkill setups
* Both “no” options can also run networking, but require use of external gateway (which doesn’t exist at a sane price right now, thanks Ubiquiti)
* All options can manage WiFi APs

### Cameras (Protect)
* Doorbells
	* **G4 Doorbell** (~£210) - WiFi only, power via chime power supply (DIN-mountable transformer included in box), includes automatic porch light and customisable text display
	* **G4 Doorbell Pro **(~£320) - As above, except in black, PoE / Ethernet (with optional adapter), colour display, additional “package camera” looking downwards
		* Very popular and routinely out of stock, can be difficult to acquire
	* **Protect Chime** (~£60) - Optional remote chime module, kind of redundant if you already have a door chime
* Surveillance
	* All cameras are PoE unless otherwise mentioned - power either via injector (included in box with single purchases) or via PoE switch
	* G3: basic cameras, motion detection only
		* **G3 Flex** (~£83) - very small 1080p mini turret camera for indoor or outdoor use, lots of mounting options
		* **G3 Micro** (~£210) - extremely small 1080p golfball-sized camera for indoor use
		* **G3 Instant** (~£79) - very small 1080p indoor camera, **WiFi **(power via USB-C), two-way audio for yelling at people
	* G4, G5, AI: more advanced, can do object detection (filter by “car”, “person”, “package”, etcetera)
		* **G4 Instant** (~£105) - as G3 Instant except 2K video
		* **G4 Bullet** (~£211) - classic style 4MP camera for outdoor use, optional IR extender (though can be unreliable)
		* **G4 Pro** (~£480) - classic style 4K camera with 3X optical zoom for outdoor use
		* **G4 Dome** (~£191) - dome-style (ceiling or wall mount only) 4MP camera for indoor or outdoor use, wide angle
		* **AI 360** (~£425) - ceiling-mount camera for indoor use, ultra-wide fisheye lens giving a top-down view of a room
		* **AI Theta** (~£316) -** extremely unique** indoor camera using absolutely tiny lens modules connected to a main processing module, do your own research

		* **G4 PTZ** (~£1,920) - 4K pan-tilt-zoom camera for indoor or outdoor use, 22x optical zoom, for spying on all of your neighbours dinner plans simultaneously
* Access
	* Via Protect app (iOS, Android, Apple TV clients available)
		* Supports scrubbing through timeline-style activity / event feed
		* Full, continuous recording
		* Works away from home
		* Provides Doorbell functionality
	* Via HomeKit (iOS), Google Home (Android), etc
		* Requires bridge device running bridge software, please ask if you’d like more information!
		* HomeKit bridge supports chiming HomePods on doorbell push

### WiFi Access Points
* If so desired
* Lite options are generally a good fit for home environments, Pro is probably overkill, LR would probably cover a small neighbourhood
* Ubiquiti started out doing Access Points, definitely their strong suit and do exactly what they say on the tin reliably
* Can be meshed for extended coverage

