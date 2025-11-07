# Installation

1. [Download Max 9](https://cycling74.com/downloads) from Cycling ‘74 and launch it.

	!!! note

		SousaFX remains fully functional after [Max’s 30-day trial ends](https://support.cycling74.com/hc/en-us/articles/360049995834-Max-8-Max-7-Authorization#link-2). Max authorization is not required.
	<br>

2. Click on "menubar > Max > Preferences..."

	![main](img/max_prefs.webp)

	- Set the Audio Input Device and Output Device to the connected audio interface.
	- Set the Sampling Rate to 48000.
	- Set the two Vector Sizes to 128 or less. Lower vector sizes result in lower latency, and better timing, but a higher possibility of CPU-overload-induced crackles in the audio.
	- Enable Overdrive (but not Scheduler in Audio Interrupt).
	- Click the "Audio I/O Mappings" button on the bottom left, to the left of the speaker button. These mapping will likely be correct by default, but it's good to check.

	![main](img/max_iomap.webp)

	- Set Input Mapping 1 to the tuba's mic. (For my interface that's "Mic/Line 1")
	- Set Output Mapping 1-2 to the speaker outputs, and 3-4 to the monitor/headphone outputs. (For my interface that's "Analog 1" for the left speaker output, "Analog 2" for the right speaker output, "Phones 3" for the left headphone output, and "Phones 4" for the right headphone output)
	- The rest of the IO mappings can be Off.

3. Download [SousaFX-v0.11.1](https://github.com/Sousastep/SousaFX-rnbo/releases/download/v0.11.1/SousaFX-v0.11.1.zip) to your `~/Documents/​Max 9/​Projects/` folder (create the Projects folder if it doesn't exist), then double-click `SousaFX-v0.11.1.maxproj` to launch the rig.

	!!! note

		SousaFX remains fully functional after [SousaFX's 30-day trial ends](purchase.md).

