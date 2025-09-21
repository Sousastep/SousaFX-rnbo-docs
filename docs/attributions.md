# Attributions

## Patchers

The pitch shifter, overdrive, noise gate, plate reverb, limiter, and compressor are from the [RNBO Guitar Pedals Package](https://cycling74.com/products/rnbo-guitar-pedals). [K-weighting](https://www.itu.int/dms_pubrec/itu-r/rec/bs/R-REC-BS.1770-5-202311-I!!PDF-E.pdf) has been added to the compressor and limiter's sidechain.

A handful of gen abstractions are from [Graham Wakefield](https://github.com/grrrwaaa) & [Gregory Taylor](https://cycling74.com/articles/an-interview-with-gregory-taylor) - [Generating Sound and Organizing Time](https://cycling74.com/books/go)

`deadzone scaled radial.maxpat` thanks [TFL](https://cycling74.com/forums/scaled-radial-deadzone-for-gamepad-joystick#reply-68021c0c3bd53f00135efbe2), [Minimuino](https://github.com/Minimuino/thumbstick-deadzones), and [Josh Sutphin](https://joshsutphin.com/gamedev/doing-thumbstick-dead-zones-right.html)

`jb.autowah` utilizes work from [Emmanuel Jourdan and Oren Shoham](https://cycling74.com/forums/math-behind-function-curve#reply-6006263e0da59906d7aff1c2
) to emulate the `function` object at audio-rate in rnbo. It also uses [h1data](https://github.com/h1data/max-custom-adsr)'s custom gen~ adsr.

## Filters

[Surreal Machines](https://www.surrealmachines.com/) - [smFIlterPack](https://cycling74.com/articles/an-interview-with-surreal-machines)

- ladder

	```
	Zero Delay Feedback 24dB Lowpass Ladder filter, Newton-Raphson model
	based on: "Computational optimization of nonlinear zero-delay feedback by second-order piecewise approximation"
	and: “Preserving the LTI system topology in s- to z-plane transforms”
	theory by Vadim Zavalishin, Native Instruments GmbH
	gen~ realisation by Pete Dowling & Matt Jackson @Surreal Machines, thanks to Graham Wakefield
	```

- sallenkey

	```
	12/24dB multimode Sallen & Key filter
	by Pete Dowling & Matt Jackson @Surreal Machines, thanks to Alex Harker
	based on "Linear trapezoidal integrated filters" by Andy Simper
	```

[Ess Mattisson](https://fors.fm/) - [gen filters](https://github.com/ess-m/gen-filters)

- fc.diode

	```
	Zero Delay Feedback filters
 	using trapezoidal integrator by Vadim Zavalishin
 	https://www.discodsp.net/VAFilterDesign_2.1.2.pdf
	
 	based on implementations by Will Pirkle and Steven Yi for Csound
 	
 	http://www.willpirkle.com/Downloads/AN-4VirtualAnalogFilters.2.0.pdf
 	http://www.willpirkle.com/Downloads/AN-5Korg35_V3.pdf
 	http://www.willpirkle.com/Downloads/AN-6DiodeLadderFilter.pdf
 	http://www.willpirkle.com/Downloads/AN-7Korg35HPF_V2.pdf
 	https://github.com/csound/csound/blob/master/Opcodes/wpfilters.c
 	```

- fc.svf-as.gendsp

	```
	SVF structure by Andrew Simper
 	https://cytomic.com/files/dsp/SvfLinearTrapOptimised2.pdf
 	```

- fc.k35lp.gendsp

	```
	Korg 35 lowpass
	```

[Joshua Clayton](https://www.youtube.com/watch?v=H06YfIkDOQQ) - [4x oversampled ladder](https://discord.com/channels/289378508247924738/289379241345155073/1403631842346799216)

- halfband_ppiir.genexpr

	```
	Polyphase recursive filter for up/down sampling by 2.
    This particular variant is extremely fast, but does not have linear phase.
    Based on algorithms published by Fred Harris.
    Copyright (c) 2025 Cycling '74
    ```

- moogladder_dv.genexpr

    ```
    This model is based on a reference implementation of an algorithm developed by
	Stefano D'Angelo and Vesa Valimaki, presented in a paper published at ICASSP in 2013.
	This improved model is based on a circuit analysis and compared against a reference
	Ngspice simulation. In the paper, it is noted that this particular model is
	more accurate in preserving the self-oscillating nature of the real filter.
	
	References: "An Improved Virtual Analog Model of the Moog Ladder Filter"
	Original Implementation: D'Angelo, Valimaki
	
	Copyright 2012 Stefano D'Angelo <zanga.mail@gmail.com>
	Conversion to RNBO Copyright 2025 Cycling '74 
	```

[Rusty Allred](https://web.archive.org/web/20071003115434/http://www.planetanalog.com/article/printableArticle.jhtml?articleID=12802683), [Trond Lossius](https://github.com/jamoma/JamomaCore/blob/master/DSP/extensions/FilterLib/source/TTLowpassLinkwitzRiley4.cpp), [Timothy Place](https://cycling74.com/tutorials/crossover-filter-design-video-tutorial), [J Curtis](https://cycling74.com/tutorials/crossover-filter-design-video-tutorial#reply-5e4377db8a6f416613deaf7c) -  4th-order Linkwitz Riley Crossover Filter

 	4th order Linkwitz-Riley filters are typically used as crossover filters, with the following properties:
 	1. Absolutely flat amplitude response throughout the passband with a 6 dB/octave rolloff rate after the crossover point.
 	2. The acoustic sum of the two driver responses is unity at crossover. (Amplitude response of each is -3 dB at crossover, i.e., there is no peaking in the summed acoustic output.)
 	3. Zero phase difference between drivers at crossover. (Lobing error equals zero, i.e., no tilt to the polar radiation pattern.) In addition, the phase difference of zero degrees through crossover places the lobe of the summed acoustic output on axis at all frequencies.
 	4. The low pass and high pass outputs are everywhere in phase. (This guarantees symmetry of the polar response about the crossover point.)
 	5. All drivers are always wired the same (in phase). 


!!! note

	The LPF freq mod LFO is tapered to match the [Moog MF-101S](https://software.moogmusic.com/store/mf-101s)' filter freq parameter. 

## Docs

SousaFX's documentation is made with [Material for MkDocs](https://squidfunk.github.io/mkdocs-material/).

The [EULA](eula.md) is modified from [Reaper's](https://www.reaper.fm/).

## Many thanks to

Brooklyn College's Sonic Arts program, and Performance and Interactive Media Arts Program

The Jim and Jamie Self Creative Award

Cycling 74`

Eventide Audio

[Brian Wolff](https://www.youtube.com/watch?v=f7TNKVm4E20)

My friends and family

Everyone in the Max discord channel

YOU for reading this far :)
