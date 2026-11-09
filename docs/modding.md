---
description: >-
  Mod SousaFX by replacing drum samples, looper alerts, and metronome sounds. Access and edit the Max/RNBO patcher source code.
---

# Modding

## Samples

The drum samples, looper alerts, and metronome click can be changed by replacing the files in `/SousaFX-rnbo/media/`

## Code

To access the internals (on mac):

Clone this repository: [https://github.com/Sousastep/SousaFX-rnbo](https://github.com/Sousastep/SousaFX-rnbo) (or click the green "Code" button, then click "Download ZIP")

And this repository: [https://github.com/Sousastep/sousa_fx_generator](https://github.com/Sousastep/sousa_fx_generator)

run `/sousa_fx_generator/tools/generate_maxpats.py` and `generate_v8uis.py`

Open `SousaFX-rnbo.maxproj`

Add `sousa_fx_generator` to `SousaFX-rnbo.maxproj`'s Project File Paths.

Disable the custom menubar with `option m`, or `menubar > File > Max Menus`

Exit presentation mode with `option command e`, or `menubar > View > Presentation`

Click the message that says `window flags nofloat, window flags zoom, window flags grow, window exec, savewindow 0`

Fullscreen the window by double-clicking the title bar.

Find the `rnbo~ @patchername gamepad_input @parameter_enable 0 @autosave 0 @autobuild 0` object, and double-click it.

Press `option command m`, or click the pencil icon in the bottom left, to modify read-only.

Keep Overdrive off in Max's preferences or else replaceable arguments in rnbo won't propagate properly after compilation.

Feel free to ask questions in the discord, linked below.
