# How To Release SousaFX

test `rnbo~` obj. once decently happy, cont.

export to external

```
	Output Directory:	~/Documents/Max 8/Projects/SousaFX-rnbo/externals
	External Platform:	all
	external name: 		sousafx
	author name: 		sousastep
	description: 		dubstep tuba
popup: Overwrite? 		OK
```

Open about_SousaFX.maxpat without the project.

Open license bpatcher using the super secret method, save to trigger savebang clears.

In the main patcher, edit and save `loadmess #.#.#`

make one last commit for this version, with the rnbo~ obj loaded in SousaFX-rnbo.maxproj, not the external.

(click toggle next to the "external / rnbopat" switch.)

```
cd ~/Documents/Max\ 8/Projects/SousaFX-rnbo && git status
git commit -m "message"
git tag v#.#.#
git push
git push origin --tags
```

click the "0" above the `list.lookup external rnbopat` object to load the external.

File > Save As Project...

name `SousaFX-v#.#.#`

open project inspector
- don't keep project folder organized
- hide project window after opening

remove files from `/sousaFX-v#.#.#/` if present:

```
	/data/license.sousafx
	/other/license.sousafx
	/externals/js.xmo
	/code/interfacecolor.js
	/media/.
```

add files from `/sousaFX-rnbo/` to `/sousaFX-v#.#.#/`:

```
	/media/click
	/media/alert
	/media/kick
	/media/snare
	/media/clap
	/media/tom
	/media/input_display
	/media/logo.png
	/externals/.
		/externals/docs/sousafx~.maxref.xml
		/externals/docs/sousafx~.readme.txt
		/externals/externals/sousafx~.mxe64
		/externals/externals/sousafx~.mxo
		/externals/init/
	/.docs/. ---> see OFFLINE in sousaFX-rnbo-docs below
```

zip, named `SousaFX-v#.#.#.zip`

download zip to blank user profile on macbook to test

https://github.com/Sousastep/SousaFX-rnbo/releases

Draft a new release

Release Title:	SousaFX v#.#.#

attach zip to github release as a binary.


## sousaFX-rnbo-docs

add release notes by rewriting your favorite commit messages:

`git log --graph --pretty=format:'%Cred%h%Creset -%C(yellow)%d%Creset %s %Cgreen(%cr) %C(bold blue)<%an>%Creset' --abbrev-commit`

find/replace past version with current version, then:

```
cd ~/Documents/SousaFX-rnbo-docs && git status; source myenv/bin/activate
git add .;git commit -m "message"
mike deploy v#.#.#
mike set-default v#.#.#
git push origin --all

OFFLINE=true mkdocs build --clean --site-dir /Users/jbaylies/Documents/Max\ 8/Projects/SousaFX-rnbo/.docs
```