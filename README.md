# script-collection
A collection of scripts mainly focused on work with Galaxy

## Usage

### Conda Environment

#### Get conda / mamba

```bash
cd /tmp
wget https://github.com/conda-forge/miniforge/releases/latest/download/Miniforge3-Linux-x86_64.sh
bash Miniforge3-Linux-x86_64.sh
source ~/.bashrc
conda --version
mamba --version
```

#### Get the environment

```bash
mamba env create -f environment.yml
```



### Enviromnent Vars

The scripts require