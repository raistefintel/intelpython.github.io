# Intel® Distribution for Python*

[Intel® Distribution for Python*](https://www.intel.com/content/www/us/en/developer/tools/oneapi/distribution-for-python.html) is a cluster of packages that includes Numba*, NumPy* and more. All these packages are optimized via [Intel® oneAPI Math Kernel Library (oneMKL](https://www.intel.com/content/www/us/en/developer/tools/oneapi/onemkl.html#gs.ddfdq4) and [Intel® oneAPI Data Analytics Library (oneDAL](https://www.intel.com/content/www/us/en/developer/tools/oneapi/onedal.html) to make the Python* application more efficient. The distribution includes a multitude of popular components, some of which include:

Libraries:
- Python
- NumPy
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

Supported versions:
- Python 3.11, Python 3.12

Package management:
- conda*
- Pip
- Mamba

Compatible with:
- VS Code
- Jupyter Notebook
- Microsoft Visual Studio*
- PyCharm*

## Supported Installation Options

1.	[Intel® Distribution for Python* Selector]((https://www.intel.com/content/www/us/en/developer/tools/oneapi/distribution-python-download.html))
2.	Intel® Data Parallel Control (Coming Soon)

Supported operating systems are outlined under System Requirements.
You may select the components you wish to install. The full list of components in the Intel® Distribution for Python* is outlined on the landing page section [What’s Included](https://www.intel.com/content/www/us/en/developer/tools/oneapi/distribution-for-python.html).

## GPU Users
**For Linux users**
The driver packages needed on Linux are described in the [Data Center GPU Series Driver Installation](https://dgpu-docs.intel.com/driver/installation.html) and [Client GPU Driver Installation](https://dgpu-docs.intel.com/driver/client/overview.html) pages.

**For Windows users**
For GPU development, the latest GPU drivers need to be installed. This can be downloaded from [Intel® Arc™ & Iris® Xe Graphics - Windows*](https://www.intel.com/content/www/us/en/download/785597/intel-arc-iris-xe-graphics-windows.html).


## Intel® Tiber™ Developer Cloud Users
You can use [Intel® Distribution for Python* in  Intel® Tiber™ Developer Cloud](https://www.intel.com/content/www/us/en/developer/tools/devcloud/services.html). After getting access to the cloud system, follow the instructions below to install Intel® Distribution for Python* with one of the available installation options.

## Selector-Specific Installation Options
### Conda
[Installation Instructions]

### Mamba
[Installation Instructions]

### Pip
[Installation Instructions]

### Docker
[Installation Instructions]

## Example with NumPy
You can see the benefits of using the Intel® Distribution for Python* on your own machine by comparing a simple program’s runtime between both distributions. First, run the sample code below in your new Intel® Distribution for Python* environment, and take note of the total runtime which should be displayed in the output. 

Once you have taken note of the runtime of this program, switch the environment back to stock Python* and run the script again. Compare the runtime in the stock environment to the runtime in the Intel® distribution environment. You should see the benefits provided by the Intel® Distribution for Python* through the significantly decreased runtime.

## Code Samples
[needs table
this]

## Build Your Own Project
No special modifications to your existing Python* projects are required to start using them with this toolkit. You can refer to samples on GitHub to learn more about this distribution.#

## Profiling Python Code
- [Intel® VTune™ Profiler](https://www.intel.com/content/www/us/en/developer/tools/oneapi/vtune-profiler.html)
- [Intel® Advisor](https://www.intel.com/content/www/us/en/developer/tools/oneapi/advisor.html)

## Additional Resources
- [What's Included](https://www.intel.com/content/www/us/en/developer/tools/oneapi/distribution-for-python.html)
- [Data Parallel Extension for NumPy* documentation](https://intelpython.github.io/dpnp/)
- [Data Parallel Control Library* documentation](https://intelpython.github.io/dpctl/latest/index.html)
- [Data Parallel Extension for Numba* documentation](https://intelpython.github.io/numba-dpex/latest/index.html)

## Support
If you have further questions or need support on your workload optimization, please submit your queries to the [Intel® Distribution for Python* Forum](https://community.intel.com/t5/Intel-Distribution-for-Python/bd-p/distribution-python) or [Intel® Distribution for Python* GitHub](https://github.com/IntelPython), on the Issues or Discussions pages, depending on the type of support required.

## Notices and Disclaimers
Performance varies by use, configuration and other factors. Learn more at www.Intel.com/PerformanceIndex.

Performance results are based on testing as of dates shown in configurations and may not reflect all publicly available updates. See backup for configuration details. No product or component can be absolutely secure.

Your costs and results may vary.

Intel technologies may require enabled hardware, software or service activation.
© Intel Corporation. Intel, the Intel logo, and other Intel marks are trademarks of Intel Corporation or its subsidiaries. Other names and brands may be claimed as the property of others.

## Product and Performance Information
Performance varies by use, configuration and other factors. Learn more at www.Intel.com/PerformanceIndex.
