# Installation



## Python

You need a working python 3.x installation to be able to use. We highly recommend installing Anaconda, which takes care of installing Python and managing packages. In the following it will be assumed that you use Anaconda. Download and install it from [here](https://www.anaconda.com/download). Make sure to download the latest version with python 3.7.

### python dependency

All the python requirements are also given in the `requirements.txt` of our [Github repository](https://github.com/ZeeUTao/zi_labrad). 

```
ipython
matplotlib~=3.3.2
numba~=0.51.2
pylabrad==0.98.1
PyVISA~=1.11.1
scipy~=1.5.2
Twisted~=20.3.0
zhinst~=20.7.2325
```

You can download the file or copy above as `requirements.txt` and run 

```bash
pip install -r requirements.txt
```



## scalabrad

To install and run scalabrad, you can click on [scalabrad](https://github.com/labrad/scalabrad) to the github repository, or our [forked ones](https://github.com/ZeeUTao/scalabrad), and follows their introduction. 

If you do not need to change or develop it, a simpler way is go to [binary](https://bintray.com/labrad/generic/scalabrad#files), which provides the packages to download, e.g., [scalabrad-0.8.3.tar.gz](https://bintray.com/labrad/generic/download_file?file_path=scalabrad-0.8.3.tar.gz). 

### Java

Java8 is required for running the binary distribution of scalabrad. 

> You'll need to have Java 8 installed on your system. 

After installation of Java8, you need add the environmental variable `JAVA_HOME  ` to be the directory of installation, for example `D:\Java8`



Now you can unzip the scalabrad files, and remember the targeted directory. It would be better to map a specific folder into a disk (like `M:`) , you can

- go to the targeted directory
- run the following bash in CMD (command)

```bash
@echo off
subst m: /d
subst m: %cd%
```

Then the folder can be found as disk M, and we can start scalabrad by the bash

```bash
M:\scalabrad-0.8.3\bin\labrad --registry file:///M:/Registry?format=delphi
```

You need to change the file name 'scalabrad-0.8.3' and the path `M:/Registry`  (for storing experimental parameters) into yours.  



