<style>
.md-typeset table thead {
    display: none;
}
</style>

# Bindings

A list of all connections between the game controller and audio effect parameters.

## Start, Select, Cardinal

Start and Select are used for changing the function of the North, East, South, and West buttons.

- Without start or select pressed:

	| Direction | Function |
	|-----------|----------|
	| north 	| tap tempo |
	| east 		| drum [looper](loopers.md) start / stop / clear |
	| south 	| main stutter enable |
	| west 		| bassline [looper](loopers.md) start / stop / clear |


- With start pressed:

	| Direction | Function |
	|-----------|----------|
	| north 	| toggle kick-ducker |
	| east 		| toggle kick-ducker |
	| south 	| toggle kick-ducker |
	| west 		| toggle kick-ducker |

- With select pressed:

	| Direction | Function |
	|-----------|----------|
	| north 	| toggle metronome |
	| east 		|  |
	| south 	| toggle bumper drumming |
	| west 		|  |

- With start and select pressed:

	| Direction | Function |
	|-----------|----------|
	| north 	| set time signature numerator via number of clicks (3 - 7)|
	| east 		|  |
	| south 	| increment drum kit preset number |
	| west 		|  |

## Shoulder Buttons

While the tuba isn't playing, and the drum looper isn't looping, pressing the shoulder buttons triggers drum samples, and holding the shoulder buttons retriggers drum samples at the rate set by the d-pad.

| button 	| samples  |
|-----------|----------|
| Left Trigger 		| clap     |
| Left Bumper 		| snare    |
| Right Trigger 		| tom      |
| Right Bumper 		| kick     |

While the tuba is playing, or the drum looper is looping, the shoulder buttons operate as follows:

The left trigger, and right bumper, are used to adjust the function of the thumbsticks.

Holding the right trigger lets an ADSR modulate the overdriven lowpass filter.

### D-pad

The left bumper, and the d-pad, are used for setting the subdivision of the auto-wah, delays, and stutters. If a subdivision is triggered twice in a row, then while the button is held down the second time, the stutters are reversed, and the wah shifts to the offbeat. 

The left trigger is used for changing the function of the d-pad and the left bumper.

- Without the left trigger pressed:

	| d-pad	    | Function	  |
	|-----------|-------------|
	| L2 		| disable auto-wah LFO |
	| d-pad up 	| quarter |
	| up right	| dotted quarter |
	| right 	| 8th triplet |
	| down right| 16th triplet |
	| down		| 16th |
	| down left	| 32nd |
	| left		| 8th |
	| up left	| dotted eighth |

- With the left trigger pressed:

	| d-pad	    | Function	  |
	|-----------|-------------|
	| L2 		| half |
	| d-pad up 	| quarter triplet |
	| right 	| 16th triplet |
	| down		| quarter quintuplet |
	| left		| 8th quintuplet |

## Left Thumbstick

### Vertical

- LFO floor envelope sensitivity.

- Envelope crossfade position.

- Bassline looper filtersweep.

### Up 

- Drum stutter enable:

	Allowed while the drum looper is looping, & the tuba isn't playing a bassline.

- Drum stutter autopan amount.

### Horizontal

- LFO ceiling envelope sensitivity.

- Drum filter sweep:

	Allowed when the tuba's silent, & the left thumbstick is within its deadzone.

	Denied when the tuba's playing, & the left thumbstick is within its deadzone.

- LFO shape:

	Allowed when the right bumper is pressed, & the left thumbstick is within its deadzone.

	Denied when the right bumper is released, & the left thumbstick is within its deadzone.

- Delay time adjustment for bassline, solo, drums, and loopers:

	Allowed while the left trigger is pressed.

### Left

- looper stutter enable:

	Allowed when the bassline looper is looping, & the left thumbstick is within its deadzone.

	Denied when the bassline looper isn't looping, & the left thumbstick is within its deadzone.

- Looper stutter autopan amount.

### Magnitude

- Lowpass filter resonance boost.

!!! note

	The magnitude is the distance of the thumbstick from the center.


## Right Thumbstick

### Up

- Bassline delay feedback amount, & solo delay feedback amount.

- Solo stutter autopan amount.

- Drum delay feedback amount:

	Allowed when the tuba's silent, & the right thumbstick is within its deadzone.

	Disallowed when tuba starts playing.

- LFO acceleration:

	Allowed when the right bumper is released, & the right thumbstick is within its deadzone.

	Denied when the right bumper is pressed, & the right thumbstick is within its deadzone.

### Down

- Either LFO decceleration, or swing amount, depending on subdivision.

- Bassline looper delay feedback amount:

	Allowed when the tuba's silent, & the right thumbstick is within its deadzone.

	Disallowed when tuba starts playing.

### Horizontal

- Delay filter frequency adjustment for bassline, solo, drums, and loopers.

- Stutter Acceleration for bassline, solo, drums, and loopers:

	Allowed when the right bumper is released, & the right thumbstick is within its deadzone.

	Denied when the right bumper is pressed, & the right thumbstick is within its deadzone.

- Drum retrigger rate adjustment:

	While the drum samples are being retriggered, this adjusts the retrigger rate.

### Left

- Bassline delay send, and solo delay send.

### Right

- Main reverb send.

- Bassline looper reverb send, and Drum reverb send:

	Allowed when the tuba's silent, & the right thumbstick is within its deadzone.

	Denied when the tuba's playing, & the right thumbstick is within its deadzone.

### Left and Right

- Drum delay send, and bassline looper delay send:

	Allowed when the tuba's silent, & the right thumbstick is within its deadzone.

	Disallowed when the tuba starts playing.

