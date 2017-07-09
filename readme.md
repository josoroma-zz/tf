# Python 3 + Anaconda (data science ecosystem)

![navigator](img/anaconda-navigator.png)

## Xcode

### Check if command line tools is installed

```
xcode-select -p
```

### Install Xcode

```
xcode-select --install
```

## Brew Python 3 Formula

 * http://brewformulas.org/Python3

### Search

```
brew search python
```

### Install

```
brew install python3
```

### Upgrade

```
brew upgrade python3
```

## Pip3

### Upgrade

```
pip3 install --upgrade pip setuptools wheel
```

### Install

```
pip3 install wheel

pip3 install numpy
```

### Help

```
pip3 -h
```

### List installed packages

```
pip3 list
```

### Show information about installed packages

```
pip3 show pip setuptools wheel
```

### Show Python version

```
python3 -V

Python 3.x.x
```

## Create a virtual environment (venv)

Virtual environments are isolated spaces for our Python projects.

```
python3 -m venv my_env
```

### Activate and use the environment

```
source my_env/bin/activate
```

Feel free to use the command `python` instead of python3, and `pip` instead of pip3.

```
python -V

Python 3.x.x
```

### To leave the environment

```
deactivate

python -V

Python 2.x.x
```

### To re-activate the environment

```
source my_env/bin/activate

python -V

Python 3.x.x
```

## Anaconda data science ecosystem

  * https://docs.continuum.io/anaconda/install

### Search

```
brew search anaconda

caskroom/cask/anaconda
```

### Install

```
brew cask install caskroom/cask/anaconda
```

```
brew cask install miniconda
```

### Add  to our PATH environment variable

```
atom ~/.bash_profile

export PATH="/usr/local/anaconda3/bin:/usr/local/miniconda3/bin:$PATH"
```

![launchpad](img/launchpad-anaconda.png)

Note: Cask anaconda installs files under `/usr/local`. The presence of such
files can cause warnings when running `brew doctor`, which is considered
to be a bug in Homebrew-Cask.

## Conda

 * https://docs.continuum.io/anaconda

 * https://conda.io/docs/py2or3.html

### Create environment

```
conda create --name tf python=3
```

```
python -V

Python 2.7.10
```

```
source activate tf
```

```
python -V

Python 3.6.1 :: Continuum Analytics, Inc.
```

### Show conda environments

```
conda info --envs

# conda environments:
#
tf                    *  /usr/local/anaconda3/envs/tf
root                     /usr/local/anaconda3
```

### List all packages

```
conda list

# packages in environment at /usr/local/anaconda3/envs/tf:
#
openssl                   1.0.2l                        0  
pip                       9.0.1                    py36_1  
python                    3.6.1                         2  
readline                  6.2                           2  
setuptools                27.2.0                   py36_0  
sqlite                    3.13.0                        0  
tk                        8.5.18                        0  
wheel                     0.29.0                   py36_0  
xz                        5.2.2                         1  
zlib                      1.2.8                         3  
```

### Search for a package

```
conda search numpy
```

### Install a package

```
conda install --name tf numpy
```

![conda](img/conda-install-package.png)

## Launch anaconda navigator

 * https://docs.continuum.io/anaconda/navigator/getting-started

```
anaconda-navigator
```

## Jupyter notebook

 * http://jupyter.org/install.html

### Install

![jupyter](img/install-jupyter.png)

### Open

![open](img/open-jupyter.png)

### New

![new](img/new-notebook.png)

### Run

![run](img/run-notebook.png)
