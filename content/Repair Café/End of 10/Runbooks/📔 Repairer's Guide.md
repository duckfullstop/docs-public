---
{"publish":true,"created":"2025-08-20T16:14:24.669+01:00","modified":"2025-09-23T20:59:05.233+01:00","cssclasses":""}
---

This guide is intended as a support tool for helping you guide your customer through the End of 10 journey.


> [!note]
> It must be stressed to the customer that we are a repair / reuse service, **not a support service.** 
> Support with any of these outcomes cannot and will not be provided by us, although we are happy to signpost.

> [!danger]
> **Under no circumstances are Repairers to be involved in making backups, or handling Customer data of any kind.**
> 
> This is for safeguarding and liability reasons - there are mandatory reporting processes that have to be followed if a Repairer inadvertently handles, for example, illegal content, which must be avoided at all costs!
> 
> Equally, if we make a backup of a system that is not complete, and the customer holds us liable for any missing files, it is extremely challenging for us to prove good faith.
> 
> **It is explicitly forbidden for Repairers to take any Customer data home with them, e.g as a backup.**

## Possible Outcomes
In no particular order:
1. Upgrade to Windows 11 with no modifications
	* These are easily identified as the upgrade is waiting for the customer in `System Settings -> Windows Update`.
2. Upgrade to Windows 11 with minor settings changes
	* This would be something like simply turning the TPM on in the UEFI settings.
3. Upgrade to Windows 11 with hardware upgrade
	* Likely to be comparatively rare.
	* Some desktop systems, for example, may simply need a CPU upgrade - of note are older AMD AM4 systems, such as Athlon systems, which can be made compatible with a drop in Ryzen 3 processor.
	* If the issue is a missing TPM 2.0 chip, then this can be retrofitted in some systems using a special TPM 2.0 daughter board.
	* Consider also upgrading RAM / HDD -> SSD at the same time.
4. Forcibly upgrade to Windows 11
	* **The Ringwood Repair Café does not recommend this solution** due to the potential for updates breaking down the line.
	* This is achieved by creating an installation USB using _Rufus_ that ignores pre-installation requirements.
	* Windows Updates are quite likely to break, especially if the CPU is not supported - as such **this should be a last resort option**.
5. Stay on Windows 10 with mitigations
	* Extended updates are available for a year (through October 2026) _provided_ the following criteria are met:
		* The customer must be signing into Windows with a Microsoft account, **and one of the following:**
			* PC Settings Sync is enabled in System Settings, or
			* the customer uses 1,000 Microsoft Reward points, or
			* spend ~£20.
	* Realistically, extended updates are there as an option to defer a longer-term decision.
	* Third party patching is available through https://0patch.com, however this might become expensive.
	* Microsoft are likely to continue offering paid extended support, but the cost is likely to rise exponentially.
6. Change to Alternative Operating System
	* The customer will have to show eagerness and willingness to learn how their new operating system works.
	* We recommend two alternative OS's:
		* ChromeOS Flex: Proprietary OS from Google. Same thing that runs on Chromebooks. Web-focused but with an increasing suite of utilities that run on-device. Updates guaranteed. Some hardware likely to not be supported - requires UEFI boot & post-2015.
		* Linux Mint: Open OS. Very beginner friendly, holds the user through operation. Strong community support online. Extensive hardware support.
	* Installing as dual-boot is risky, as Windows often likes to destroy the Linux bootloader for little to no reason, which will be extremely difficult for the customer to troubleshoot without further support. You can use discretion here however (especially as, once updates to Windows 10 cease, it is highly unlikely that it will overwrite the bootloader)
	* **It is absolutely critical to ensure that the customer's software / hardware workflows will not be impacted.** For example, if a customer makes heavy use of Windows-only software (such as a specific CAD programme), this is unlikely to be a good option. Live USB is essential for validating that things work as expected.
	* Customer must be made aware that all data will be lost; it will be like having a new system straight from the shop. The Data Disclaimer must be read and accepted before performing any work.
		* A good option is to recommend the customer buy a new SSD for their new alternative-OS installation, alongside an external caddy - this way they can continue to access their old Windows data when necessary, or roll back temporarily by simply installing the old drive again.
7. Throw in the towel: New Hardware
	* We're trying to avoid this if at all possible, but there will likely be occasions where the customer's best (or only) choice is to buy a new system.
	* Recommend an appropriate new or used / refurbished system for their use case - perhaps sell their old system on eBay or Gumtree / Facebook Marketplace for reuse?
## The Decision Tree
1. *"Can your system be upgraded to Windows 11?"*
	1. Check `System Settings -> Windows Update`. Force Check for Updates.
	2. Update available? 🎉 **Outcome:**  "System Eligible for Windows 11 Upgrade"
	3. No update available? It's now time to understand _why_ the system is not eligible. Use the Windows 11 PC Health Check app: https://support.microsoft.com/en-us/windows/check-if-a-device-meets-windows-11-system-requirements-after-changing-device-hardware-f3bc0aeb-6884-41a1-ab57-88258df6812b
	4. The outcome of this will influence next steps.
		1. Missing TPM 2.0: Investigate whether the system should have a TPM available. Check UEFI settings - does it just need to be enabled? Is there an option to retrofit a TPM daughterboard?
		2. Secure Boot not supported: Check UEFI settings - you might just need to turn it on. **Make sure Bitlocker is disabled before changing this setting - it can cause a recovery key to be required.**
		3. Processor not supported: is it possible to upgrade this system? Consider the platform / era of system, whether the CPU is socketed, etcetera.
	5. System can be upgraded? 🎉 **Outcome:** "System Eligible for Windows 11 Upgrade after (steps taken)". You might also consider recommending a memory upgrade, to improve performance further.
	6. System cannot be upgraded? Move on to Step 2.
2. *"Can we mitigate the end of support on your current system, to give you more time to make a decision?"*
	1. Review the ESU programme KB article: https://support.microsoft.com/en-us/windows/windows-10-consumer-extended-security-updates-esu-program-33e17de9-36b3-43bb-874d-6c53d2e4bf42
	2. Remember, for this option to show, the system must be running Windows 10 22H2, and the user must be signed into a Microsoft account.
	3. Mitigation an option? 🎉 **Outcome**: "System not eligible for Windows 11 upgrade; enrolled onto extended security updates"
		1. You **must** educate the user that this is a stop-gap solution only, and that they will have to make a decision down the line, be that using an alternative OS or purchasing a new system.
	4. Mitigation not an option? Go to step 3.
3. *"Unfortunately, you are likely to require either a replacement system, (or an alternative operating system)"*
	1. Discuss options with the customer. A refurbished system that meets the Windows 11 requirements (such as a used Thinkpad) will likely fulfil their needs. They have the option to buy new if they value support, though this will obviously incur more expense.
		* We can thoroughly recommend Framework laptops - we can even help them build the DIY edition! (though it's also available pre-built for an additional charge)
	2. If the customer is financially constrained and cannot purchase a replacement, there are three options:
		1. If the system must be upgraded (for example, customer software will stop working), and if you have confidence that the customer understands the risks, you can offer a forced upgrade to Windows 11. The customer **must** have a backup before this option is pursued, and it must be made clear that this comes with no warranty / updates are likely to break down the line. It will be on the customer to maintain this option. 🎉 **Outcome**: "System not eligible for Windows 11 upgrade; forcibly upgraded using modified installer USB, customer counselled on risks."
		2. Otherwise, counsel the customer that their system will continue to function, but will become increasingly vulnerable to security risks including to personal data and financial data - including to any such data on their home network. 🎉 **Outcome**: "System not eligible for Windows 11 upgrade; user counselled on risks of continuing to run Windows 10."
		3. The customer also has the option to pursue an alternative operating system, such as ChromeOS or Linux Mint.
			1. You're going to need a good amount of information and confidence before you pursue this option.
			2. Firstly, consult with the user. You'll need positive answers to all of these questions:
				1. Are they open and keen to learn a new way of doing things, on a fresh system? Things are likely to not be in the same places as they are on Windows, and there's a learning curve to be followed.
				2. Do they rely on any Windows-only applications or devices? You will need to ask questions about everything they use their system for. Ask them to show you all of the apps they use, then research whether Linux / ChromeOS alternatives are available. They may not be the same application (for example, Office is replaced by LibreOffice on Linux, Google Docs / Sheets etc. on ChromeOS). Also, what devices do they use - is there a good Linux driver available for them? Printers are likely to be a potential sticking point.
				3. Are they confident in taking a backup of all of their data? You can suggest the option of buying a new, equivalently-sized SSD for their system, alongside a caddy; that way they can access all of their data on demand, and move it across for day-to-day use.
			3. You can show the customer a ChromeOS or Linux Mint system to help them make their mind up - a laptop with multi-boot is available on demand from the service desk. You can also boot ChromeOS or Linux Mint off the appropriate Live USB drive - this will also give you an indication as to hardware compatibility, and gives the customer an opportunity to see it working with no strings attached.
			4. If this is an option - ✅ **Further work required**: "System to be migrated to (Alternative Operating System)"
				* Give the customer a copy of the "Alternative OS - Thinking about a new Operating System" take-home sheet. This will help steer their next café appearance.

## Resources
* "Windows 10 End of Life" on the Restarters Wiki: https://wiki.restarters.net/Windows_10_End_of_Life
* "End of Windows 10 Toolkit for Repair Groups": https://therestartproject.org/end-of-windows-10-toolkit-for-repair-groups/ (particularly "What volunteers in your group will need to know")
* "End of 10" project: https://endof10.org