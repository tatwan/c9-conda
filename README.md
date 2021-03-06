# How to install Jupyter, NumPy, Pandas and Matplotlib on Cloud 9 or Docker Container
Instructions below are for Python v2.7 Minconda 2. For Python 3.x just replace Miniconda2 with Miniconda3 anywhere you see it below.

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

If `wget` command was not recognized you may need to install it using `apt-get update && apt-get install wget`

3.Changing file permission for execution
```
chmod a+x Miniconda2-latest-Linux-x86_64.sh
```

4.Installing Miniconda
```
./Miniconda2-latest-Linux-x86_64.sh
```

If you ran into an error like `bunzip2: not found`, the easiest way is to manually install it via `apt-get install bzip2`. 

If during the install you got interrupted, then when you rerun the just `-u` for update as in `./Miniconda2-latest-Linux-x86_64.sh -u`. You will be prompted to, type `yes` and hit enter.

5. Before installing packages. Close the current bash terminal and open a new terminal (either on c9 or docker container). 

### Install packages

```
conda install -y numpy
```
You may be promopted
```
The following NEW packages will be INSTALLED:

    pandas:          0.18.1-np111py27_0
    python-dateutil: 2.5.3-py27_0      
    pytz:            2016.4-py27_0     
    six:             1.10.0-py27_0     

```

Install other packages similarly.
```
conda install -y pandas matplotlib 
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

## Note: If you are interested in installing OpenCV, Conda makes it very easy to install
```
conda install opencv
```

### Install Jupyter
```
conda install jupyter
```

To run Jupyter notebook in c9 run:
```
jupyter notebook --ip=0.0.0.0 --port=8080 --no-browser
```

Then open your browser using port 8080 for example. 


[Thanks to this Stackoverflow post](http://stackoverflow.com/questions/31598883/installing-python-module-pandas-in-cloud9)
