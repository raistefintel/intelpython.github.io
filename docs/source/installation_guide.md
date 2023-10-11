# Installation Guide

### Install via Intel® AI Analytics Toolkit
The Intel® AI Analytics Toolkit includes the Intel Distribution for Python. So the Intel Distribution for Python is ready for use once the Intel AI Analytics Toolkit installation is finished and the environment activation is run.

#### Environment Setup
1. **Install the Intel AI Analytics Toolkit.** <br>
To download the Intel Distribution for Python* from the Intel AI Analytics Toolkit, visit [here](https://www.intel.com/content/www/us/en/developer/tools/oneapi/ai-analytics-toolkit-download.html) and choose the installation method of your choice. Find detailed information about the toolkit [here](https://www.intel.com/content/www/us/en/developer/tools/oneapi/ai-analytics-toolkit.html#gs.48ofa2).
2. **Set up Intel the AI Analytics Toolkit environment.** <br>
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
For more information on environment variables, check out how to [use the setvars Script for Linux or macOS](https://www.intel.com/content/www/us/en/docs/oneapi/programming-guide/2023-0/use-the-setvars-script-with-linux-or-macos.html), or [Windows](https://www.intel.com/content/www/us/en/docs/oneapi/programming-guide/2023-0/use-the-setvars-script-with-windows.html).

3. **Activate the conda environment.**
* Linux\*:
  - If you have root access to your oneAPI installation path or if you use the Intel® DevCloud, Intel Python environment will be activated by default. However, if you have activated another environment, you can return with the following command:
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
### Install as a Single Component
Achieve fast math-intensive workload performance without code changes for data science and machine learning problems. This component is part of the Intel® AI Analytics Toolkit. <br>

[![sign-up-for-updates](https://img.shields.io/badge/Sign_up_for_updates-blue)](https://software.seek.intel.com/developer-products-sign-up?dwnld=Intel%C2%AE%20Distribution%20for%20Python%2A)

Intel® Distribution for Python (version 2023.2.0) has been updated to include functional and security updates. Users should update to the [latest version](https://www.intel.com/content/www/us/en/developer/articles/tool/oneapi-standalone-components.html#python).

|Name (Click to initiate download)   | Version  |  Size | Installer  | Date  |
|---|---|---|---|---|
| [Intel Distribution for Python for Linux](https://registrationcenter-download.intel.com/akdlm/IRC_NAS/03aae3a8-623a-47cf-9655-5dd8fcf86430/l_pythoni39_oneapi_p_2023.2.0.49422.sh)  | 2023.2.0  | 19 MB	  | Online  | Jul. 17, 2023  |
| [Intel Distribution for Python for Linux](https://registrationcenter-download.intel.com/akdlm/IRC_NAS/03aae3a8-623a-47cf-9655-5dd8fcf86430/l_pythoni39_oneapi_p_2023.2.0.49422_offline.sh)  | 2023.2.0  | 1.1 GB  | Offline  | Jul. 17, 2023  |
| [Intel Distribution for Python for Windows](https://registrationcenter-download.intel.com/akdlm/IRC_NAS/fbbbbffd-dc8c-4b9c-bb7b-8347b777f6b5/w_pythoni39_oneapi_p_2023.2.0.49423.exe)  | 2023.2.0  | 12 MB  | Online  | Jul. 17, 2023  |
| [Intel Distribution for Python for Windows](https://registrationcenter-download.intel.com/akdlm/IRC_NAS/fbbbbffd-dc8c-4b9c-bb7b-8347b777f6b5/w_pythoni39_oneapi_p_2023.2.0.49423_offline.exe)  | 2023.2.0  | 1.0 GB  | Offline  | Jul. 17, 2023  |
| [Intel Distribution for Python for macOS](https://registrationcenter-download.intel.com/akdlm/IRC_NAS/58964c88-5b45-427e-9ae8-ad18a23af930/m_pythoni39_oneapi_p_2023.2.0.49425.dmg)  | 2023.2.0  | 28 MB  | Online  | Jul. 17, 2023  |
| [Intel Distribution for Python for macOS](https://registrationcenter-download.intel.com/akdlm/IRC_NAS/58964c88-5b45-427e-9ae8-ad18a23af930/m_pythoni39_oneapi_p_2023.2.0.49425_offline.dmg)  | 2023.2.0  | 468 MB  | Offline  | Jul. 17, 2023  |


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
4. Activate the conda environment:
   ```
   conda activate idp
   ```
### Install Using YUM Repository

For the latest instructions on how to install Intel® Distribution for Python* using YUM, please check out [this guide](https://www.intel.com/content/www/us/en/developer/articles/guide/installing-free-libraries-and-python-yum-repo.html).

### Install Using APT Repository

For the latest instructions on how to install Intel® Distribution for Python* using APT, please check out [this guide](https://www.intel.com/content/www/us/en/developer/articles/guide/installing-free-libraries-and-python-apt-repo.html).

## Sanity Check
After the activation of the environment, type `python` in the command line to find the Python\* distribution info.
- Linux\* & Windows\*: `python` <br>
  The distribution info should include `Intel Corporation`:
    * Linux:
      ```
      Python 3.7.10 (default, Jun 4 2021, 06:52:02)
      [GCC 9.3.0] :: Intel Corporation on linux
      Type "help", "copyright", "credits" or "license" for more information.
      Intel(R) Distribution for Python is brought to you by Intel® Corporation.
      Please check out: https://software.intel.com/en-us/python-distribution
      ```
    * Windows:
      ```
      Python 3.9.10 (main, Mar 21 2022, 08:44:00) [MSC v.1916 64 bit (AMD64)] :: Intel Corporation on win32
      Type "help", "copyright", "credits" or "license" for more information.
      Intel(R) Distribution for Python is brought to you by Intel Corporation.
      Please check out: https://software.intel.com/en-us/python-distribution
      ```
  These methods can be used as a sanity check that Intel Distribution for Python is properly installed.

## Sample Code
Run this numpy sample code in a stock Python\* environment and in an IntelPython environment. You will see benefits from IntelPython.
```
import numpy as np
import time
  
start = time.time()
  
rd = np.random.RandomState(88)
a = rd.randint(1,1000,(1000,1000))
y = rd.randint(1,1000,(1000))
res = np.linalg.solve(a,y)
  
end = time.time()
  
print(res)
print('Time consumed:',end-start)
```

## Build Your Own Project
No special modifications to your existing Python* projects are required to start using them with this toolkit. Check out the [Reference Section](#references) for Github samples.

## References
- [Intel Distribution for Python Landing Page](https://huiyan2021.github.io/intelpython.github.io/2023.1.1/getting_started.html)
- [Intel AI Analytics Toolkit Landing Page](https://www.intel.com/content/www/us/en/developer/tools/oneapi/toolkits.html#analytics-kit)
- [Code Samples](https://github.com/oneapi-src/oneAPI-samples/tree/master/AI-and-Analytics/Getting-Started-Samples)
- [Get Started with the Intel AI Analytics Toolkit for Linux\*](https://www.intel.com/content/www/us/en/docs/oneapi-ai-analytics-toolkit/get-started-guide-linux/2023-1/overview.html)

## Support
If you have further questions or need support on your workload optimization, please submit your queries to the Intel AI Analytics Toolkit Forum or [IntelPython](https://github.com/IntelPython) GitHub, on the Issues or Discussions pages depending on the type of support required.

## Notices and Disclaimers
Performance varies by use, configuration and other factors. Learn more at www.Intel.com/PerformanceIndex. <br>
<br>
Performance results are based on testing as of dates shown in configurations and may not reflect all publicly available updates. See backup for configuration details. No product or component can be absolutely secure. <br>
<br>
Your costs and results may vary.<br>
<br>
Intel technologies may require enabled hardware, software or service activation.<br>
<br>
© Intel Corporation. Intel, the Intel logo, and other Intel marks are trademarks of Intel Corporation or its subsidiaries. Other names and brands may be claimed as the property of others.

## Product and Performance Information
Performance varies by use, configuration and other factors. Learn more at www.Intel.com/PerformanceIndex.
  
