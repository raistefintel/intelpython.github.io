## Pip
1.	If you do not have pip, use the following instructions to install it. After installation, make sure that you can run pip from the  command line. 
[Installation Instructions](https://packaging.python.org/en/latest/tutorials/installing-packages/#ensure-you-can-run-pip-from-the-command-line)

2.	Create and activate a virtual environment.  Please note that “x” in “python=3.x” should signify which version of Python* you would like to install.
```bash
python3.x -m venv idp 
```
For Lunix:
```bash
source idp/bin/activate 
```
For Windows:
```bash
idp\Scripts\activate
```

3.	Install Intel® Distribution for Python* components via PIP 
>Note: Components not available in https://pypi.anaconda.org/intel/simple  can be found in PyPI main repository
Search for individual installation commands in [What’s included](https://www.intel.com/content/www/us/en/developer/articles/tool/whats-included-distribution-for-python.html#packageEnvironmentManagers) page



4. Verify installation.
```bash
pip list	
```

[Selector - Get Started Guide](https://github.com/raistefintel/intelpython.github.io/blob/master/docs/source/IDP_GSG.md)
[Intel® Distribution for Python* Installation Selector](https://www.intel.com/content/www/us/en/developer/tools/oneapi/distribution-python-download.html)