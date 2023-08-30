# Python Virtual Environment on Windows

Assuming you are on windows 11 platform and already installed python from [here](https://www.python.org/ftp/python/3.10.11/python-3.10.11-amd64.exe), let's create python virtual environment.


1. Step 1

Open windows terminal and type:

```
pip install virtualenv
```

2. Step 2

```
virtualenv myMLENV
myMLENV\Scripts\activate.bat
```

3. Step 3

Once your virtual environment `activated`, you can start install relevant python libraries.


## Windows: CUDA & cuDNN setup (for Tensorflow or PyTorch)

Assuming you are using latest Windows 11 build and using Nvidia enable PC/laptop, 

1) download nvidia graphic driver from [here](https://www.nvidia.com/download/index.aspx). Once download, install as usual.

2) Download cuda 11.8 from [here](https://developer.nvidia.com/cuda-11-8-0-download-archive). Once download, install `without` choosing graphic driver

3) Download cuDNN v8.6.0 for CUDA 11.x from [here](https://developer.nvidia.com/rdp/cudnn-archive). Once download, uncompress and copy all the files to `C:\Program Files\NVIDIA GPU Computing Toolkit\CUDA\v11.8`

4) Download `Build Tools for Visual Studio 2022` from [here](https://visualstudio.microsoft.com/downloads/?q=build+tools) and install c++ build tools

5) Download and extract the zlib package from [ZLIB DLL](http://www.winimage.com/zLibDll/zlib123dllx64.zip). Copy `zlibwapi.dll` from `dll_x64` folder and paste it at `C:\Program Files\NVIDIA GPU Computing Toolkit\CUDA\v11.8\bin`

5) reboot and proceed installing Tensorflow 2.10.1: `pip3 install tensorflow-gpu==2.10.1`

## Reference

[Creating Python Virtual Environment in Windows and Linux](https://www.geeksforgeeks.org/creating-python-virtual-environment-windows-linux/)
[NVIDIA Guide](https://docs.nvidia.com/deeplearning/cudnn/install-guide/index.html#install-windows)
