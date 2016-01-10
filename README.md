# Empirical Analysis and Modeling of Black-Box Mutational Fuzzing

This repository contains data and scripts for the work Empirical Analysis and Modeling of Black-Box Mutational Fuzzing. 

Please email us (muz127@ist.psu.edu) for any question.


## 1. Data

The fuzzing data for analysis is contained in results/results.zip. We have pruned out some large and unnecessary files.
Please unzip the content to the results/ folder.

## 2. The Analysis

The scripts/ folder has all scripts used for data analysis. Among these scripts, the Jupyter notebook (IPython notebook) 
main_analysis.ipynb contains all results presented in Section 4, 5 and 6. You could directly view the notebook on Github. 

To run it locally, please first install the following packages:

(1) Python 3
    A simple way to set up the environment is to install Anaconda. By doing this, you can skip (2) and (3).
    https://www.continuum.io/downloads

(2) The latest Jupyter Notebook from:
    http://jupyter.org/
  
(3) Some common data analysis packages such as matplotlib, scipy, etc. 

(4) The powerlaw package
    https://pypi.python.org/pypi/powerlaw

Then launch Jupyter notebook and play with the main_analysis.ipynb.
	
## 3. The Fuzzing Process

Below, we list all steps of our fuzzing experiment, from seed collection to running fuzzing.
NOTICE: We do not share seed files, because the size of the seed collection is too large (10GB+).

### 3.1 Prepare the fuzzing environment

(1) Download the VM image of BFF 2.7 and follow the installation guide.
https://www.cert.org/vulnerability-analysis/tools/bff.cfm?

(2) After launching the VM, install the target application using apt-get. We list program version numbers in the paper.

(3) Install the pincoverage tool we wrote. First, copy pincoverage/ to the bff shared folder in the host OS.
Then in the guest OS, enter pincoverage/ and do make

### 3.2 Seed Collection

### 3.3 Collect and Analyze Coverage Data

### 3.4 Run Fuzzing

*Commands used for fuzzing programs*:

autotrace:
autotrace $SEEDFILE > test.pdf

convert:
~/convert $SEEDFILE /dev/null

feh: 
feh $SEEDFILE

ffmpeg: 
ffmpeg -i $SEEDFILE -f rawvideo -y /dev/null

gif2png:
gif2png -r -f -h -O $SEEDFILE

gifsicle:
gifsicle -i < $SEEDFILE > /dev/null

jpegtran:
jpegtran $SEEDFILE

mp3gain:
mp3gain $SEEDFILE

mupdf:
mupdf $SEEDFILE

Outside In Viewer: 
<Directory>/sdk/demo/simple $SEEDFILE

xpdf:
xpdf $SEEDFILE






