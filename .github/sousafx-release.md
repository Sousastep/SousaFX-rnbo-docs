# How To Release SousaFX

## sousaFX-rnbo-docs
```
cd ~/Documents/SousaFX-rnbo-docs && git status; source myenv/bin/activate
```

### build & deploy docs
```
git add .;git commit -m "message"
mike deploy v#.#.#
mike set-default v#.#.#
git push origin --all

OFFLINE=true mkdocs build --clean --site-dir /Users/jbaylies/Documents/Max\ 8/Projects/SousaFX-rnbo/.docs
```

## sousaFX-rnbo
```
cd ~/Documents/Max\ 8/Projects/SousaFX-rnbo && git status
```

open project. in "About SousaFX" window, edit and save loadmess #.#.#

```
git commit -m "message"
git tag v#.#.#
git push
git push origin --tags
```

File > Save As Project...

name sousaFX-v#.#.#

file edits
	remove .js files
	add drum samples
	compile and add externals for mac and windows
	add local documentation

zip, named sousaFX-v#.#.#.zip

attach zip to github release as a binary.
