# Install Multiple Python Versions (Linux)

## How to Handle Multiple Versions of Python

### One-Time Setup for Multi-Python Configurations

Follow these steps to set up `pyenv` for managing multiple Python versions on Linux.

### 1. Clone Pyenv Repository
```bash
cd $HOME
git clone https://github.com/pyenv/pyenv.git ~/.pyenv
```

### 2. Edit `.bashrc` File
Open the `.bashrc` file using any text editor (e.g., `nano`):
```bash
sudo nano ~/.bashrc
```

### 3. Add the Following Lines at the End of the File
```bash
# Pyenv environment variables
export PYENV_ROOT="$HOME/.pyenv"
export PATH="$PYENV_ROOT/bin:$PATH"
# Pyenv initialization
if command -v pyenv 1>/dev/null 2>&1; then
  eval "$(pyenv init --path)"
fi
```

### 4. Restart the Terminal
```bash
exec $SHELL
```

### 5. Install Required Dependencies
```bash
sudo apt-get update --yes
sudo apt-get install --yes libssl-dev zlib1g-dev libbz2-dev libreadline-dev libsqlite3-dev llvm libncurses5-dev libncursesw5-dev xz-utils tk-dev libgdbm-dev lzma lzma-dev tcl-dev libxml2-dev libxmlsec1-dev libffi-dev liblzma-dev wget curl make build-essential python-openssl
```

---

## Installing Specific Python Versions

### 1. Install a Specific Python Version
```bash
pyenv install 3.10.9
```

### 2. Set a Global Python Version
```bash
pyenv global 3.10.9
```

### 3. Set a Directory-Specific Python Version
Navigate to the desired directory and run:
```bash
pyenv local 3.10.9
```

---

## Creating a Virtual Environment
To create a virtual environment that follows a specific Python version:
```bash
python3 -m venv VENV_NAME
```

---

