
[!(Intel® Distribution for Python*)](https://www.intel.com/content/www/us/en/developer/tools/oneapi/distribution-for-python.html) is a cluster of packages that includes Numba*, NumPy* and more. All these packages are optimized via [!(Intel® oneAPI Math Kernel Library (oneMKL))](https://www.intel.com/content/www/us/en/developer/tools/oneapi/onemkl.html#gs.ddfdq4) and [!(Intel® oneAPI Data Analytics Library (oneDAL))](https://www.intel.com/content/www/us/en/developer/tools/oneapi/onedal.html) to make the Python* application more efficient. The distribution includes a multitude of popular components, some of which include:

Libraries:
- Python
- numPy
- SciPy
Mkl interfaces:
- Mkl-service
- Mkl-random
- Mkl-fft
- Mkl-umath
GPU components:
- Dpctl
- Dpnp
- Numba-dpex

## System Requirements

CPUs:
- Intel® Core™ processor family
- Intel® Xeon® processor family
GPUs:
- Intel® UHD Graphics for 11th generation Intel processors or newer
- Intel® Iris® Xᵉ graphics
- Intel® Arc™ graphics
- Intel® Data Center GPU Flex Series
- Intel® Data Center GPU Max Series
Operating systems:
- Unix family*
- Windows® 10
- Windows* 11
- pported versions:
- Python 3.11, Python 3.12
Package management:
- conda*
- Pip
- mamba
Compatible with:
- VS Code
- Jupyter Notebook
- Microsoft Visual Studio*
- PyCharm*

## Supported Installation Options

The Intel ® Distribution for Python* supports several installation options

Supported operating systems are outlined under System Requirements.
You may select the components you wish to install. The full list of components in the Intel® Distribution for Python* is outlined on the landing page section [!(What’s Included)](https://www.intel.com/content/www/us/en/developer/tools/oneapi/distribution-for-python.html).

## GPU USers
You can use [!(Intel® Distribution for Python* in  Intel® Tiber™ Developer Cloud)](https://www.intel.com/content/www/us/en/developer/tools/devcloud/services.html). After getting access to the cloud system, follow the instructions below to install Intel® Distribution for Python* with one of the available installation options.

## Offline Installer
1. To download Intel Distribution for Python*, visit here and choose the installation method of your choice. 
2. Run the following commands to install on respective platform:
```bash
# Linux installation (Interactive) 
# Note that the file name must be changed to how to appears in your downloads folder.
bash ~/intelpython3-202X.X.X.sh 

# Linux installation (CLI) 
bash ~/intelpython3.sh -b -u -p ~/intelpython3 

# The flags can be included as necessary. They are used as follows:
# -b enables batch mode, running the installation without interactive prompts.
# -u updates the current installation. You may omit this if this is the first time you’re installing IDP on this machine.
# -p specifies the installation path prefix. In this example, ~/intelpython3 is the target directory.

# Windows installation (Interactive) 
intelpython3.exe 

# Windows installation (CLI) 
start /wait intelpython3.exe /S /RegisterPython=0 /D=%LOCALAPPDATA%\intelpython3 
```

3. Activate the conda environment.
*Linux*
The following commands can be used to activate the Intel® Distribution for Python installation:
```bash
#Root access or Intel(R) Developer Cloud installation*
source /opt/intel/intelpython3/bin/activate

#Home installation
source $HOME/intelpython3/bin/activate
```
   
*Windows*
Navigate to the installation directory of Intel Python and find the "Scripts" directory, then run `.\activate` in the terminal. This runs the base activate script found at
`C:/User/path/to/intelpython3\Scripts\activate`

The command prompt should point to installation when running `where python`
`(base) C:/User/path/to/intelpython3`

Installation verification – `conda list`
   
*Deactivating environment for Offline Installer*
To deactivate your IDP environment, run `conda deactivate` until base env is deactivated
`conda deactivate`

## Conda
1. Follow conda Installation Guide to install conda in your environment. If you already have conda installed in your system, update it with the command: 
`conda update conda `
2. Add Intel channel and conda-forge to tell conda to choose Intel packages over default packages when available.
```bash
conda config --add channels https://software.repos.intel.com/python/conda/
conda config --add channels conda-forge

# Remove defaults channel from .condarc if it exists
conda config --remove channels defaults
```
3. Install Intel® Distribution for Python* via conda. We recommend that you create a new environment while installing. To install the core python3 environment, run the following command: 
`conda create -n idp intelpython3_full python=3.x`
Please note that “x” in “python=3.x” should signify which version of Python* you would like to install. For example, for Python* version 3.9: 
`conda create -n idp intelpython3_core python=3.9`
For individual installation commands, refer to the [!(What’s included](https://www.intel.com/content/www/us/en/developer/articles/tool/whats-included-distribution-for-python.html#packageEnvironmentManagers) section.
4. Activate the conda environment:
`conda activate idp` 

## Mamba
1.	If you do not have Mamba, get Miniforge by following the instructions here 
`conda update mamba`
2.	Add Intel channel and conda-forge to tell conda to choose Intel packages over default packages, when available.
```bash
conda config --add channels https://software.repos.intel.com/python/conda/
conda config --add channels conda-forge

# Remove defaults channel from .condarc if it exists
conda config --remove channels defaults
```
3.	Install Intel® Distribution for Python* via Mamba. We recommend that you create a new environment while installing. To install the core python3 environment, run the following command: 
`mamba create -n idp intelpython3_full python=3.x`
Please note that “x” in “python=3.x” should signify which version of Python* you would like to install. 
4.	Acitvate conda environment, then follow the usual steps for activating the environment: 
mamba activate idp
5.	Installation verification
`mamba list	`

## Docker
1.	If you don’t have Docker installed on your machine, follow [!(these instructions)](https://docs.docker.com/engine/install/) to install it.
2.	Pull the image from [!(DockerHub)](https://hub.docker.com/r/intel/python) using the following command:
`docker pull intel/python:latest `
3.	Run a performance sample by running the following commands:
```bash
git clone https://github.com/intel/ai-containers
cd ai-containers/python
docker run --rm -it \
    -v $PWD/tests:/tests \
    intel/python:latest \
    python /tests/perf_sample.py
```
4. Installation verification
`conda list`

## Proof of Concept
You can see the benefits of using the Intel® Distribution for Python* on your own machine by comparing a simple program’s runtime between both distributions. First, run the sample code below in your new Intel® Distribution for Python* environment, and take note of the total runtime which should be displayed in the output. 
```bash
import numpy as np
import time

start = time.time()

rd = np.random.RandomState(88)
a = rd.randint(1,1000,(1000,1000))
y = rd.randint(1,1000,(1000))
res = np.linalg.solve(a,y)

end = time.time()

print(res)
print('Time Consuming:',end-start)
```

Once you have taken note of the runtime of this program, switch the environment back to stock Python* and run the script again. Compare the runtime in the stock environment to the runtime in the Intel® distribution environment. You should see the benefits provided by the Intel® Distribution for Python* through the significantly decreased runtime.

## Code Samples
[needs table
this]

## Build Your Own Project
No special modifications to your existing Python* projects are required to start using them with this toolkit. You can refer to samples on GitHub to learn more about this distribution.#

## Profiling Python Code
- [!(Intel® VTune™ Profiler)](https://www.intel.com/content/www/us/en/developer/tools/oneapi/vtune-profiler.html)
- [!(•	Intel® Advisor)](https://www.intel.com/content/www/us/en/developer/tools/oneapi/advisor.html)

## Additional Resources
- [!(Data Parallel Extension for NumPy* documentation)](https://intelpython.github.io/dpnp/)
- [!(Data Parallel Control Library* documentation  )](https://intelpython.github.io/dpctl/latest/index.html)
- [!(Data Parallel Extension for Numba* documentation)](https://intelpython.github.io/numba-dpex/latest/index.html)

## Support
If you have further questions or need support on your workload optimization, please submit your queries to the [!(Intel® Distribution for Python* Forum)](https://community.intel.com/t5/Intel-Distribution-for-Python/bd-p/distribution-python) or [!(Intel® Distribution for Python* GitHub)](https://github.com/IntelPython), on the Issues or Discussions pages, depending on the type of support required.

## Notices and Disclaimers
Performance varies by use, configuration and other factors. Learn more at www.Intel.com/PerformanceIndex.

Performance results are based on testing as of dates shown in configurations and may not reflect all publicly available updates. See backup for configuration details. No product or component can be absolutely secure.

Your costs and results may vary.

Intel technologies may require enabled hardware, software or service activation.
© Intel Corporation. Intel, the Intel logo, and other Intel marks are trademarks of Intel Corporation or its subsidiaries. Other names and brands may be claimed as the property of others.

## Product and Performance Information
Performance varies by use, configuration and other factors. Learn more at www.Intel.com/PerformanceIndex.
