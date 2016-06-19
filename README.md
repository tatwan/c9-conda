# How to install Python NumPy, Pandas and Matplotlib on Cloud 9
Instructions below are for Python v2.7 Minconda 2. For Python 3.x just replace Miniconda2 with Miniconda3

Check python version on c9 terminal.
```
python -V
```

### Install Miniconda

1. http://conda.pydata.org/miniconda.html , right clik on the 64-bit Linux and copy the file address for the proper version you need.
2. Prepare to install Miniconda. Download Miniconda 64Bits for Linux using wget. 
```
wget https://repo.continuum.io/miniconda/Miniconda2-latest-Linux-x86_64.sh
```

3.Changing file permission for execution
```
chmod a+x Miniconda2-latest-Linux-x86_64.sh
```

4.Installing Miniconda
```
./Miniconda2-latest-Linux-x86_64.sh
```
5. Before installing packages. Close the current c9 bash terminal. Open a new terminal.
### Install packages
```
conda install numpy
```
You may be promopted
```
The following NEW packages will be INSTALLED:

    pandas:          0.18.1-np111py27_0
    python-dateutil: 2.5.3-py27_0      
    pytz:            2016.4-py27_0     
    six:             1.10.0-py27_0     

Proceed ([y]/n)? 
```
Just type **y** and hit enter.

Install other packages similarly.
```
conda install pandas
conda install matplotlib
```
In the terminal type Python you should see something like this:
```
Python 2.7.11 |Continuum Analytics, Inc.| (default, Dec  6 2015, 18:08:32) 
[GCC 4.4.7 20120313 (Red Hat 4.4.7-1)] on linux2
Type "help", "copyright", "credits" or "license" for more information.
Anaconda is brought to you by Continuum Analytics.
Please check out: http://continuum.io/thanks and https://anaconda.org
```
To validate packages installed properly try:
```
import pandas as pd
import numpy as np
```
you should not see an error like this 
```
ImportError: No module named matplotlib
```
if you do, then you need to make sure you install the package correclty using conda.

[Thanks to this Stackoverflow post](http://stackoverflow.com/questions/31598883/installing-python-module-pandas-in-cloud9)

## Note: If you are interested in installing OpenCV, Conda makes it very easy to install
```
conda install opencv
```
