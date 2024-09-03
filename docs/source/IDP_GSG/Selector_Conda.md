## Conda
1. Follow conda Installation Guide to install conda in your environment. If you already have conda installed in your system, update it with the command: 
```bash
conda update conda
```
2. Add Intel channel and conda-forge to tell conda to choose Intel packages over default packages when available.
```bash
conda config --add channels https://software.repos.intel.com/python/conda/
conda config --add channels conda-forge
```
Remove defaults channel from .condarc if it exists
```bash
conda config --remove channels defaults
```
3. Install Intel® Distribution for Python* via conda. We recommend that you create a new environment while installing. To install the python3 environment, run the following command: 
`conda create -n idp intelpython3_full python=3.x`
Please note that “x” in “python=3.x” should signify which version of Python* you would like to install. For example, for Python* version 3.9: 
`conda create -n idp intelpython3_full python=3.9`

>For individual installation commands, refer to the [What’s included](https://www.intel.com/content/www/us/en/developer/articles/tool/whats-included-distribution-for-python.html#packageEnvironmentManagers) section.
4. Activate the conda environment:
```bash
conda activate idp
```

[Selector - Get Started Guide](https://github.com/raistefintel/intelpython.github.io/blob/master/docs/source/IDP_GSG.md)
[Intel® Distribution for Python* Installation Selector](https://www.intel.com/content/www/us/en/developer/tools/oneapi/distribution-python-download.html)

