# adsf-venv-test

This is a test of asdf version manager's workflow with python 3's virtual environments.

## When starting a new project:
```zsh
# create repo
git init

# create .gitignore
echo .venv/ > .gitignore

# create .tool_versions
asdf local python latest

# create venv
python -m venv .venv

# activate venv
source .venv/bin/activate

# install packages
pip install pendulum

# export requirements
pip freeze > requirements.txt

# deactivate venv
deactivate
```

## When working on an existing project:
```zsh
# clone repo
git clone https://...

# install python
asdf install

# create venv
python -m venv .env

# activate venv
source .env/bin/activate

# install packages
pip install -r requirements.txt

# make binaries accessible from PATH
asdf reshim python

# deactivate venv
deactivate
```
