# Installation 

The packages requires a python version >=3.5, as well as some libraries listed in [requirements file](requirements.txt). For some additional functionalities, more libraries are needed for these extra functions and options to become available. Here is a quick install guide of the package, starting off with the minimal install up to the full installation. 

**Note** : A (mini/ana)conda framework would help installing all those packages and therefore could be recommended for non-expert users. 

## Miniconda installation [optional]
As miniconda is lighter and has most of the interesting functionalities of anaconda, we would recommand using Miniconda. 
1. Go to https://conda.io/miniconda.html and download the lastest version of the software in 64bits. The python version here (2.7 or 3.6) does not make any importance at this stage. 
2. Go to your downloaded folder and execute the installation script. For linux users, in a terminal : 
```
$ bash Miniconda-X.sh
```
3. Start off by creating your first environment named _'py35'_: open a (new, or refresh the .bashrc) terminal and type :
```
$ conda create --name py35 python=3.5
```
4. Activate your new environment by using the command :
```   
$ source activate py35
```
**Note**: Keep your environment activated in order to install all your libraries in your environment. 

## Python 3.5 or higher
If you installed a Miniconda framework at the last step, you already installed python3.5 in an environment, and therefore you can skip this step. 

To check if python 3.5 is installed on your device, execute the command : 
```	
$ python --version
```
If not, you can install it with the command (Debian distribution): 
```
$ sudo apt-get install python3 python3-pip python3-wheel
```
## Install tensorflow
As some of the key algorithms in the _cdt_ package use the TensorFlow package, it is required to install it. If you possess cuda-enabled GPUs to perform computations, you can install TensorFlow with the command : 
```	
$ pip install tensorflow-gpu
```	
If you don't possess any compatible GPU, install the CPU-version of TensorFlow : 
```
$ pip install tensorflow 
```
## Install the python requirements and the _cdt_ package
After having installed tensorflow, we can proceed to install the _cdt_ package : 
```
$ git clone https://github.com/Diviyan-Kalainathan/CausalDiscoveryToolbox.git  # Download the package 
$ cd CausalDiscoveryToolbox
$ pip install -r requirements.txt  # Install the requirements
$ python setup.py install develop --user
```
**The package is then up and running ! You can run most of the algorithms in the CausalDiscoveryToolbox, you might get warnings: some additional features are not available, but you can just ignore them**

## Additional : Pytorch
[Not yet functional, in development]

## Additional : R wrapper and R libraries
[In development]
In order to have access to additional algorithms from various R packages such as bnlearn, kpcalg, pcalg, minet while using the _cdt_ framework, it is required to install R as well as the wrapper package rpy2.

<!-- python>=3.5 -->

<!-- Install dependencies  -->
<!-- ```  -->
<!-- pip install -r requirements.txt -->
<!-- ``` -->

<!-- Get source code -->
<!-- ``` -->
<!-- git clone https://github.com/Diviyan-Kalainathan/CausalDiscoveryToolbox.git -->
<!-- ``` -->

<!-- Setup python package -->
<!-- ``` -->
<!-- python setup.py -->
<!-- or -->
<!-- python setup.py install develop --user -->
<!-- ``` -->
<!-- Extra : rpy2 -->
<!-- tensorflow-gpu or tensorflow -->
<!-- pytorch -->
