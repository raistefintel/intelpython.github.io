# Get Started With Intel® Distribution for Python\*
Intel® Distribution for Python\* is a cluster of packages including Numba, NumPy and more. All these packages are optimized via Intel® oneAPI Math Kernel Library (oneMKL) and Intel® oneAPI Data Analytics Library (oneDAL) to make Python\* application more efficient.

## Supported Installation Options
### Install via Intel® AI Analytics Toolkit
Intel® AI Analytics Toolkit includes Intel Distribution for Python. So the Intel Distribution for Python is ready for use once the Intel AI Analytics Toolkit installation is finished and the environment activation is run.
#### Environment Setup
1. Install Intel AI Analytics Toolkit. To download Intel Distribution for Python* from the Intel AI Analytics Toolkit, visit [here](https://www.intel.com/content/www/us/en/developer/tools/oneapi/ai-analytics-toolkit-download.html) and choose the installation method of your choice. Find detailed information about the toolkit [here](https://www.intel.com/content/www/us/en/developer/tools/oneapi/ai-analytics-toolkit.html#gs.48ofa2).
2. Set up Intel AI Analytics Toolkit environment. <br>
Source the setvars script located in the root of your oneAPI installation.
* Linux\*:
  - Sudo:
  ```
  . /opt/intel/oneapi/setvars.sh
  ```
  - User:
  ```
  . ~/intel/oneapi/setvars.sh
  ```
* Windows:
```
C:\Program Files(x86)\Intel\oneAPI\setvars.bat
```
For more information on environment variables, view [Use the setvars Script for Linux or macOS](https://www.intel.com/content/www/us/en/docs/oneapi/programming-guide/2023-0/use-the-setvars-script-with-linux-or-macos.html), or [Windows](https://www.intel.com/content/www/us/en/docs/oneapi/programming-guide/2023-0/use-the-setvars-script-with-windows.html).
3. Activate the conda environment.
* Linux\*:
  - If you have root access to your oneAPI installation path or if you use the Intel® DevCloud: <br>
Intel Python environment will be activated by default. However, if you have activated another environment, you can return with the following command:
```
source activate base
```
  - If you do not have root access to your oneAPI installation path: <br>
    By default, the Intel AI Analytics Toolkit is installed in the /opt/intel/oneapi folder, which requires root privileges to manage it. If you would like to bypass using root access to manage your conda environment, then you can clone your desired conda environment using the following command:
    ```
    conda create --name usr_intelpython --clone base
    ```
    Then activate your conda environment with the following command:
    ```
    source activate usr_intelpython
    ```
* Windows:
    ```
    C:\ProgramFiles(x86)\Intel\oneAPI\intelpython\python3.x\Scripts\activate
    ```
### Install via Anaconda
1. Follow [Conda Installation Guide](https://docs.conda.io/projects/conda/en/latest/user-guide/install/) to install Conda in your environment. If you already have conda installed in your system, please update your conda:
   ```
   conda update conda
   ```
2. Add Intel channel. <br>
Tell conda to choose Intel packages over default packages, when available.
  ```
  conda config --add channels intel
  ```
3. Install Intel Distribution for Python\* via conda. We recommend that you create a new environment while installing. To install the core python3 environment, run:
   ```
   conda create -n idp intelpython3_core python=3.x
   ```
   **Please note that “x” in “python=3.x” should signify which version of Python\* you would like to install.** For example, for Python\* version 3.9: conda create -n idp intelpython3_core python=3.9.
4. Acitvate conda environment, then follow the usual steps for activating the environment:
   ```
   conda activate idp
   ```
   
    
