# Release Notes

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
