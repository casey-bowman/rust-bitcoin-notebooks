# Rust Bitcoin Notebooks

To run the notebooks, you need to install Jupyter Lab and a Rust kernel

## Jupyter Lab 

### Install python3 and python3-venv
(if not already installed)
```bash
sudo apt install -y python3 python3-venv
```

### Setup env
```bash
python3 -m venv venv
```

### Start env
```bash
source venv/bin/activate
```

### Install dependencies
```bash 
pip install -r requirements.txt
```

### Start jupyter
```bash
jupyter lab
```

### Close env
(when done, after closing jupyter)
```bash
deactivate
```

## Rust Kernel

### Install Rust
(if not already installed)
```bash
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
```
See [rustlang.org](https://www.rust-lang.org/tools/install) for more information.

### Install Rust kernel from source
```bash
git clone git@github.com:evcxr/evcxr.git
cd evcxr
cargo install --locked evcxr_jupyter
evcxr_jupyter --install
```

> ⚠️ **_WARNING:_** Run jupyter lab at least once before installing the Rust kernel. The last command depends on there already being the folder  `~/.local/share/jupyter`.

### Install Rust source code
```bash
rustup component add rust-src
```