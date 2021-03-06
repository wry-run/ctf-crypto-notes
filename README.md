# capture-the-flag tutorials

Training material for capture-the-flag cryptographic challenges - see [ctftime.org](https://ctftime.org/) - provided as [jupyter](https://jupyter-notebook.readthedocs.io/en/stable/index.html) notebooks.

There are several cryptography libraries, with varying degrees of user-friendliness and capabilities - see for instance this [crypto API comparison](https://www.cl.cam.ac.uk/~rja14/shb17/fahl.pdf). I like [pycryptodome](https://github.com/Legrandin/pycryptodome) and [cryptography](https://github.com/pyca/cryptography).

## Running notebooks in the cloud

You can use [![Binder](https://mybinder.org/badge_logo.svg)](https://gke.mybinder.org/v2/gh/caffeine-elemental/ctf-crypto-notes/master) or [![Azure Notebooks](https://notebooks.azure.com/launch.png)](https://notebooks.azure.com/import/gh/caffeine-elemental/ctf-crypto-notes) - see this [introduction](https://notebooks.azure.com/help/introduction) - to clone this github repo to your projects.

## Setup and run on a local linux machine

Tested on [linux mint](https://www.linuxmint.com/) 20, with [jupyterthemes](https://github.com/dunovank/jupyter-themes).

```bash
python3 -m pip install --user --upgrade pip
python3 -m pip install --user --upgrade virtualenv
python3 -m venv venv
source venv/bin/activate
python3 -m pip install --upgrade wheel 
python3 -m pip install --upgrade -r requirements.txt
jt -t monokai
jupyter notebook
```

Additionally, for `gmpy2` and `pyecm` you will probably need libmpc-, libmpfr-, and libgmp-dev, which you can install (credit: [monolune](https://www.monolune.com/installing-apt-packages-from-a-requirements-file/)) with

```bash
sed 's/#.*//' requirements-gmpy2.txt | xargs sudo apt-get install -y
wget https://raw.githubusercontent.com/martingkelly/pyecm/master/pyecm.py
```


