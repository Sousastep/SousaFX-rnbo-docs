## readme

this is the documentation for [SousaFX-rnbo](https://github.com/Sousastep/SousaFX-rnbo)

## snippets

### setup

git clone https://github.com/Sousastep/SousaFX-rnbo-docs.git

cd SousaFX-rnbo-docs

python3 -m venv myenv

source myenv/bin/activate

python3 -m pip install mike

python3 -m pip install mkdocs

python3 -m pip install mkdocs-open-in-new-tab // https://github.com/squidfunk/mkdocs-material/discussions/3660#discussioncomment-5434673

python3 -m pip install mkdocs-autorefs

mike serve // preview versioning w/o auto-reload

mkdocs serve // preview current version w/ auto-reload

cd ~/Documents/SousaFX-rnbo-docs && git status; source myenv/bin/activate; mkdocs serve

### version & deploy

git add .;git commit -m "newest commit"

mike deploy v#.#.#

mike set-default v#.#.#

git push origin --all

### local build

OFFLINE=true mkdocs build --clean --site-dir /Users/jbaylies/Documents/Max\ 8/Projects/SousaFX-rnbo/.docs 
