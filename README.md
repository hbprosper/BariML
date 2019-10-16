# BariML
## Introduction
An introduction to fully connected deep neural networks (DNN) and convolutional neural networks (CNN) in which their mathematical underpinning is explained. Machine learning (ML) models are mathematical functions that happen to be much more complicated than the ones typically found in textbooks for scientists and engineers. The exponential growth in ML-based applications is due, in part, to four breakthroughs. The first is the current ability to fit enormously complicated functions to data, something that was technologically impossible at the start of the century. The second is the ability to use huge data sets for fitting these models. The third is the discovery that these complicated functions can mimic behavior associated with intelligence and last but not least is the invention by machine learning researchers of highly expressive models and very effective fitting methods.

Much of the work in the machine learning community has indeed been, and continues to be, extremely creative. But, all too often, when described, machine learning models come across as mysterious and inscrutable. In part this is because of the highly suggestive jargon that permeates the machine learning field. For example, the word "learning" is misleading. Learning, as ordinarily understood, implies understanding. But can it really be said that a mathematical function understands? The answer, at the very least,  is unclear.

This tutorial comprises several __jupyter__ notebooks (see below) that are known to work with Python 2.7.x with x > 9. They may also work with Python 3.x.y, but this has not been checked.

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

The easiest way to install these standard packages is to follow the instructions at

https://www.scipy.org/install.html

Follow similar instructions at

https://jupyter.org/install

in order to install the jupyter notebook.

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
git clone https://github.com/hbprosper/BarML
```
This should download the package BariML to your current directory.

### 2. Unpack MNIST data set
A couple of the tutorials use data from the MNIST website, reformatted in a way that is quicker to load. Go to the jupyter Home tab in your browser and navigate to __BariML/datasets__ where you will find the notebook __prepare_mnist_data.ipynb__. Click on this filename to activate this notebook and run it to completion. You can find help on running notebooks here

https://jupyter.readthedocs.io/en/latest/running.html#running

