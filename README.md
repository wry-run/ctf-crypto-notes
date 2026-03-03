# capture-the-flag tutorials

Training material for capture-the-flag cryptographic challenges - see [ctftime.org](https://ctftime.org/) - provided as [jupyter](https://jupyter-notebook.readthedocs.io/en/stable/index.html) notebooks.

There are several cryptography libraries, with varying degrees of user-friendliness and capabilities - see for instance this [crypto API comparison](https://www.cl.cam.ac.uk/~rja14/shb17/fahl.pdf). Commonly used libraries are [pyca](https://github.com/pyca/cryptography) and [pycryptodome](https://github.com/Legrandin/pycryptodome).

## Setup and run on a local linux machine

Tested on ubuntu 25.10.

```bash
python3 -m venv venv
source venv/bin/activate
python3 -m pip install --upgrade pip
python3 -m pip install --upgrade -r requirements.txt
jupyter notebook
```

Additionally, for `gmpy2` and `pyecm` in the RSA notebook you will need `libmpc-dev`, `libmpfr-dev`, and `libgmp-dev`, which you can install (credit: [monolune](https://www.monolune.com/installing-apt-packages-from-a-requirements-file/)) with

```bash
sed 's/#.*//' apt.txt | xargs sudo apt install -y
wget https://raw.githubusercontent.com/martingkelly/pyecm/master/pyecm.py
```

## Running notebooks in the cloud

You may use [![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/wry-run/ctf-crypto-notes/main). Not guaranteed to work without hiccups.

