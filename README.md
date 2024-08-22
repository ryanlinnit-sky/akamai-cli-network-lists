# Akamai Network Lists


## Development

This project is using [hatch](https://hatch.pypa.io/latest/) as it's build system. For this reason I also used it to manage the development environment. The following commands can be used or alternatively you're free to use the Python `venv` module.

You may need to [install](https://hatch.pypa.io/latest/install/) `hatch` (`pip install hatch`)

```bash
hatch env create
hatch shell
```


## Build

```bash
python3 -m pip install --upgrade build
python3 -m pip install --upgrade twine

python3 -m build
python3 -m twine upload dist/*
```


## Install in akamai-cli

```bash
python3.11 -m venv test_venv
source test_venv/bin/activate
PYTHONUSERBASE="test_venv/lib/python3.11/site-packages"
akamai install https://github.com/ryanlinnit-sky/akamai-cli-network-lists.git

akamai network-lists
```
