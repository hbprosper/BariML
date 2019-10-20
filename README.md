# BariML
## Introduction
An introduction to fully connected deep neural networks (DNN) and convolutional neural networks (CNN) in which their mathematical underpinning is explained. Machine learning (ML) models are mathematical functions that happen to be much more complicated than the ones typically found in textbooks for scientists and engineers. The exponential growth in ML-based applications is due, in part, to four breakthroughs. The first is the current ability to fit enormously complicated functions to data, something that was technologically impossible at the start of the century. The second is the ability to use huge data sets for fitting these models. The third is the discovery that these complicated functions can mimic behavior associated with intelligence and last but not least is the invention by machine learning researchers of highly expressive models and very effective fitting methods.

Much of the work in the machine learning community has indeed been, and continues to be, extremely creative. But, all too often, when described, machine learning models come across as mysterious and inscrutable. In part this is because of the highly suggestive jargon that permeates the machine learning field. For example, the word "learning" is misleading. Learning, as ordinarily understood, implies understanding. But can it really be said that a mathematical function understands? The answer, at the very least,  is unclear.

This tutorial comprises several __jupyter__ notebooks (see below) that should work with Python 2.7.x with x > 9 as well as Python 3.7.4. 

### Dependencies and Installation
The jupyter notebooks in this package depend on a few well-known Python packages:

| __modules__   | __description__     |
| :---          | :---        |
| pandas        | data table manipulation, often with data loaded from csv files |
| numpy         | array manipulation and numerical analysis      |
| matplotlib    | a widely used plotting module for producing high quality plots |
| pylab         | embedded within matplotlib and provides Matlab-like features |
| scikit-learn  | easy to use machine learning toolkit |
| pytorch       | a powerful, flexible, machine learning toolkit |

Also recommended are

| __modules__   | __description__     |
| :---          | :--- |
| scipy         | scientific computing    |
| sympy         | an excellent symbolic algebra module |

The simplest way to install these packages is first to install miniconda (or Anaconda) on your laptop by following the instructions at:

https://docs.conda.io/projects/conda/en/latest/user-guide/install/index.html

Software release systems such as Anaconda (__conda__ for short) make it possible to have several separate self-consistent named *environments* on a single machine, say your laptop. For example, you may need to use Python 2.7.14 sometimes and Python 3.7.4 at other times. If you install software without using *environments* there is the very real danger that the software on your laptop will become inconsistent. Anaconda (and its lightweight companion miniconda) provide a way, for example, to create a software *environment* consistent with Python 2.7.14 and another that is consistent with Python 3.7.4. 

Let's assume you want to run this tutorial using Python 3.7.4. It is a good idea to update conda using the command
```bash
conda update conda
```
Assuming conda is properly installed and initialized on your laptop, you can create an environment, here we call it *python3*, containing a large subset of the packages in the conda system using the command
```bash
conda create -n python3 python=3.7.4 anaconda
```
Before pressing __y__ to continue with the installation, scan through the list of packages and identify which of the above are in the list. That way, you will know which ones are missing and need to be installed using the conda install command. For example, as of this writing neither __pytorch__ nor the CERN __ROOT__ package are available by default. In order to install these packages, first be sure to choose in which conda environment they are to be installed. First activate the desired environment, by doing, for example,
```bash
conda activate python3
```
Then to install pytorch do
```bash
conda install pytorch torchvision -c pytorch
```
and to install ROOT do
```bash
conda install root -c conda-forge
```
You may also wish to install the rather impressive 3D animation package __vpython__,
```bash
conda install vpython -c vpython
```
If all goes well, you will have installed a rather complete set of amazing high quality *absolutely free* software packages on your system that are consistent with Python 3.7.4.

More some quick help on conda see 

https://uoa-eresearch.github.io/eresearch-cookbook/recipe/2014/11/20/conda/


If you still prefer to do everything by hand, follow the instructions at

https://www.scipy.org/install.html

and 

https://jupyter.org/install


### 1. Download
It is a good idea to organize your computer-based projects in a systematic way. For example, in your home directory (usually the area identified by the environment variable $HOME), you may wish to create a directory (i.e., folder) called __Projects__ and create within it a sub-directory called __Tutorials__ as follows
```bash
cd
mkdir -p Projects/Tutorials
```
In a terminal window dedicated to running the jupyter notebook, do
```bash
cd
cd Projects
juypter notebook
```
This will run the notebook in your browser and block the terminal window, which you can iconize.

In another terminal window, go to your Tutorials sub-directory
```bash
cd
cd Projects/Tutorials
```
and execute the command
```bash
git clone https://github.com/hbprosper/BariML
```
This should download the package BariML to your current directory.

### 2. Unpack MNIST data set
__NOTE:__ Some of the tutorials use data from the MNIST website, reformatted in a way that is quicker to load. In order to create the reformatted MNIST files,  go to the jupyter __Home__ tab in your browser and navigate to __BariML/datasets__. There you will find the notebook __prepare_mnist_data.ipynb__. Click on this filename to activate this notebook and run it to completion. You can find help on running notebooks here

https://jupyter.readthedocs.io/en/latest/running.html#running

This will create two files __mnist_train.pkl__ and __mnist_test.pkl__ that are needed by the notebooks.

### 3. Notebooks

The notebooks provide detailed background information and explanations and are well-commented.

| __notebooks__                   | __description__     |
| :---          | :--- |
datasets/prepare_mnist_data.ipynb     | Create files mnist\_train.pkl and mnist\_test.pkl |
roofit/roofit_example.ipynb           | Use RooFit (needs ROOT from CERN) to fit cosmological models to Type 1a supernova data |
sklearn/scikit-learn_exercise_0.ipynb | Fit a purely empirical model (a neural network) to Type 1a supernova data | 
sklearn/scikit-learn_exercise_1.ipynb | Regression (wine quality estimation) using a neural network model |
sklearn/scikit-learn_exercise_2.ipynb | Classification of MNIST data using a deep neural network model |
pytorch/pytorch_exercise_1.ipynb      | Classification of MNIST data using a shallow neural network model |
pytorch/pytorch_exercise_2.ipynb      | Classification of MNIST data using a convolution neural network model  |

