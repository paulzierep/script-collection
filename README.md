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

#### Acivate the environment

```bash
conda activate script-collection
```

### Get environment variables permanently into the conda env 

Add environment vars to .env

```bash
GALAXY_URL=https://usegalaxy.eu
GALAXY_API_KEY=<your key>
```

Add permanently to conda

```bash
# For each line in .env
while IFS='=' read -r key value; do
    # skip empty lines or comments
    [[ -z "$key" || "$key" == \#* ]] && continue
    conda env config vars set "$key=$value"
done < .env

conda deactivate
conda activate script-collection
conda env config vars list
```