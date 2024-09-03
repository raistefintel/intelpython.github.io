## Offline Installer
1. To download the Intel® Distribution for Python*, visit [here](https://www.intel.com/content/www/us/en/developer/tools/oneapi/distribution-python-download.html) and choose the installation method of your choice. 
2. Run the following commands to install on the respective platform:

**Linux installation (Interactive)**
Note that the file name must be changed to how it appears in your downloads folder.
```bash
bash ~/intelpython3-202X.X.X.sh 
```

**Linux installation (CLI)**
```bash
bash ~/intelpython3.sh -b -u -p ~/intelpython3 
```
The flags can be included as necessary. They are used as follows:
-b enables batch mode, running the installation without interactive prompts.
-u updates the current installation. You may omit this if this is the first time you’re installing IDP on this machine.
-p specifies the installation path prefix. In this example, ~/intelpython3 is the target directory.

**Windows installation (Interactive)**
```bash
intelpython3.exe 
```

**Windows installation (CLI)**
```bash
start /wait intelpython3.exe /S /RegisterPython=0 /D=%LOCALAPPDATA%\intelpython3 
```

3. Activate the conda environment on your respective platform.

**Linux**
The following commands can be used to activate the Intel® Distribution for Python installation:
```bash
#Root access or Intel(R) Developer Cloud installation*
source /opt/intel/intelpython3/bin/activate

#Home installation
source $HOME/intelpython3/bin/activate
```
   
**Windows**
Navigate to the Intel Python installation directory, find the "Scripts" directory, and run' .activate` in the terminal.

The command prompt should now show `(base)` at the start of the command prompt.

4. Verify instalaltion.
```bash
conda list
```

**Deactivating environment for Offline Installer**
To deactivate your IDP environment, run the command below until base env is deactivated.

```bash
conda deactivate
```

[Selector - Get Started Guide](https://github.com/raistefintel/intelpython.github.io/blob/master/docs/source/IDP_GSG.md)
[Intel® Distribution for Python* Installation Selector](https://www.intel.com/content/www/us/en/developer/tools/oneapi/distribution-python-download.html)