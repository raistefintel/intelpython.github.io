## Mamba
1.	If you do not have Mamba, get Miniforge by following the instructions [here](https://github.com/conda-forge/miniforge?tab=readme-ov-file#install). Otherwise, ensure that it is updated:
```bash
conda update mamba
```
2.	Add Intel channel and conda-forge to tell conda to choose Intel packages over default packages, when available.
```bash
conda config --add channels https://software.repos.intel.com/python/conda/
conda config --add channels conda-forge
```
Remove defaults channel from .condarc if it exists.
```bash
conda config --remove channels defaults
```
3.	Install Intel® Distribution for Python* via Mamba. We recommend that you create a new environment while installing. To install the core python3 environment, run the following command: 
```bash
mamba create -n idp intelpython3_full python=3.x
```
Please note that “x” in `python=3.x` should signify which version of Python* you would like to install. 

4.	Activate the environment: 
```bash
mamba activate idp
```
5.	Verify installation.
```bash
mamba list	
```

[Selector - Get Started Guide](https://github.com/raistefintel/intelpython.github.io/blob/master/docs/source/IDP_GSG.md)
[Intel® Distribution for Python* Installation Selector](https://www.intel.com/content/www/us/en/developer/tools/oneapi/distribution-python-download.html)