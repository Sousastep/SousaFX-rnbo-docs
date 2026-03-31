# Release Notes

All releases are available here: [https://github.com/Sousastep/SousaFX-rnbo/releases](https://github.com/Sousastep/SousaFX-rnbo/releases)

## 0.11.5

- Refine delay feedback mechanism for hold and release:

	- Adjust bindings: Select places hold, and Select + West releases hold.

	- Slower fadeout of filter delay feedback amount after hold is released. 

	- Auto-release if delay goes silent.

- Remove all main LPFs except Simper's. 

- To main LPF, Add resonance gain compensation, and add resonance limiter below 400 Hz.

- Add binding to crossfade main LFO between triangle and square, as well as rising saw and falling saw. Improve phase of all shapes.

- The Left and Right Thumbsticks' button press actions are now determined by whether or not Start and/or Select are held.

- The main LPF's envelope modulation can be toggled on/off by pushing L3 while holding Start.

- Lengthen looper's mechanism for auto-switching from recording to playing.

- Remove crossover filter modulation, Hardcode to 80 Hz.

- Increase pitchshifter mix when powerchord enabled.

- Add free-rate wah, enabled via R3.


## 0.11.4

- Make delay feedback binding taper linear.

- Don't sent drum delay into drum looper.

- Add talkback mic binding with auto-mute logic.

- Improve default preset.


## 0.11.3

- Add Active Bindings window.

- The left thumbstick button, L3, sets the crossfade mode: 

	1. Transient helper on (while the audio input is below the noisegate's threshold, the crossfade envelope is pushed rightwards to help clarify the attack).

	2. Transient helper off.

	3. Crossfade off (no detuned dry sound).

- Pressing the Start button places a hold on the current delay feedback amount until either 16 bars have passed or the right thumbstick button (R3) is pressed.

- Mute respective delay if its feedback or send parameter is released quickly.

- Criss-cross left and right channels in delay's feedback loop.

- Rotate LFO floor, ceiling, and wah-adjust bindings 45 degrees.

- Disable bumper drumming while the left thumbstick is outside of its deadzone.

- Use one single reverb for all.

- Use stuttered LPF freq env to modulate LPF.

- Swap rnbo.noisegate~ for "regular" noisegate.
	
- Adjust smoothing for all envelopes.

- Refine wah swing and phase.

- Declick looper clear.

- Add clipper to end of FX chain.


## 0.11.2

- Now fully functional on the [Raspberry Pi 5](https://github.com/Sousastep/sousaFX-rpi-scripts).

- Declick stutter fx & DJ-filter.

- Fix erroneous looper state transitions.

- Compress drum's low freqs with bassline, instead of compressing bassline's low freqs with drums.

- As the joystick's magnitude increases, the amount that the tuba envelope affects the LPF's LFO's floor/ceiling decreases. (removed in next version)

- The bassline delay is now sent into the main stutter so it can be perma-enabled while looping the next drumbeat.

- Replaced CPU-heavy filters with more efficient filters.

- Add binding to transpose pitchshifter up a 5th.


## 0.11.1

First SousaFX-RNBO release! 🥳


## Past releases:

[doc.sousastep.quest/content/releasenotes.html](https://sousastep.github.io/SousaFX-docs/content/releasenotes.html)
