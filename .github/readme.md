## readme

This is the documentation for [SousaFX-rnbo](https://github.com/Sousastep/SousaFX-rnbo).

## snippets

### setup
```
git clone https://github.com/Sousastep/SousaFX-rnbo-docs.git
cd SousaFX-rnbo-docs
python3 -m venv myenv
source myenv/bin/activate
pip install mkdocs
pip install mike
pip install mkdocs-autorefs
pip install mkdocs-material
pip install mkdocs-open-in-new-tab // https://github.com/squidfunk/mkdocs-material/discussions/3660#discussioncomment-5434673

mike serve // preview versioning w/o auto-reload
mkdocs serve --livereload // preview current version w/ auto-reload

cd ~/Documents/SousaFX-rnbo-docs && git status; source myenv/bin/activate; mkdocs serve --livereload
```
"--livereload" needed due to https://github.com/squidfunk/mkdocs-material/issues/8478#issue-3476831556


### version & deploy
```
git add .;git commit -m "newest commit"
mike deploy v#.#.#
mike set-default v#.#.#
git push origin --all
```

### local build
```
OFFLINE=true mkdocs build --clean --site-dir /Users/jbaylies/Documents/Max\ 8/Projects/SousaFX-rnbo/.docs 
```

### convert
```
for f in *.png; do cwebp "$f" -o "${f%.png}.webp"; done
```