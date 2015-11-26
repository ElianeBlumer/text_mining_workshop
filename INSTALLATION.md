# Getting Started With IPython Notebooks

(original source for these instructions: https://github.com/saloot/IPythonClass#insana)

### Python

Python is a very popular general-purpose language, with all the modern and classic constructs of a programming language that every software developer appreciates. This is what makes Python beneficial over MATLAB, besides the fact that it is not proprietary and various open source python distributions are freely and publicly available.

However, the very fact that Python is a general purpose language and not a software specific to scientific computing may be considered a drawback of it, too. To address this problem, several scientific computing packages (i.e. sets of function,classes,...) have been developed and released for it so far. These packages contain a large variety of functions which can solve everyday computational problems of researchers in many fields of engineering and science.

But the remaining problem is to find, install, maintain, manage updates and retain the consistency among all such packages as well as the Python system itself. This is where Anaconda comes in.




### Anaconda

Anaconda is a completely free Python distribution (i.e. set of packages) for scientific purposes, as stated in their website. It contains more than 125 Python packages for science, mathematics, engineering and data analysis.

Installing Anaconda will not only give you an out-of-the-box ready python system as well as a fully-featured IDE (Integrated Development Environment), but also it will release you from the burden of manually installing and taking care of dependency and consistency requirements between various packages.


## Installing Python and IPython Notebooks

To download Anaconda, go to http://continuum.io/downloads and download the zip file compatible with your system. The download page looks like this:


<img title="Image: https://d396qusza40orc.cloudfront.net/dsp/img/dl.png" alt="window" src="https://d396qusza40orc.cloudfront.net/dsp/img/dl.png" width="600">


It may ask for your e-mail as well. **Please note that we will use the 2.7 Python version!**


### Installation on Linux

Installing Anaconda is pretty simple. On Linux-based systems, all you need to do is running the following command.

    $ bash Anaconda-1.x.x-Linux-x86[ 64].sh

No root access is required. However, you will need to manually add Python executable files to your Path environment if you want to run them from every folder. This can be done by adding the following line of code to your `~/.bashrc` file:

    export PATH= /anaconda:$PATH

### Installation on Windows

Installing Anaconda on Windows should be easy. It is automatically added to Path. In case of any prospective problem, disabling your anti-virus can be a potential solution.

<img title="Image: https://d396qusza40orc.cloudfront.net/dsp/img/win.png" alt="window" src="https://d396qusza40orc.cloudfront.net/dsp/img/win.png" width="600">


### Installation on Mac

On MacOS,  all you need to do is running the graphical installer. Anaconda will be automatically added to your path. However, in some cases an error message may appear at the installation time which is not a big deal. You can simply click *Install for me only* and go on.

<img title="Image: https://d396qusza40orc.cloudfront.net/dsp/img/osx.png" alt="window" src="https://d396qusza40orc.cloudfront.net/dsp/img/osx.png" width="600">

It seems to happens for older versions of OS X that the following error is generated when launching the ipython notebook (see </span><a href="#ipynb" title="Link: #ipynb">section 12</a>)
<div class="code">ValueError: unknown locale: UTF-8</div>

In that case, run the command <strong>locale</strong> in the terminal and inspect the value of the environment variable <code>LC_CTYPE</code>. It is probably just <code>UTF-8</code>.

Now open the file ~/.profile and add the following line

`export LC_CTYPE='us_EN.UTF-8'`


Then close the terminal session and try again. You might need to replace `us_EN` by a different value matching your system configuration.

## Reading more about Python basics

If you are new to Python, you can start with some introdcutory online courses (such as [this one](https://www.udacity.com/course/programming-foundations-with-python--ud036)).

Alternatively, you might be interested in taking a look at [this tutorial](https://github.com/LCAV/SignalsOfTheDay/blob/master/Tutorial/Tutorial.ipynb), which was procided by [LCAV](http://lcav.epfl.ch) here at EPFL.


## IPython Notebooks

IPython notebooks are very interesting novel features added to recent versions of IPython. Notebooks are interactive documents that allow running Python code and reading (or writing) notes and documentations *in the same place*. Therefore, one can not only see the results he is reading about, but also can produce different results by changing the documented code. 

A notebook is actually an extended HTML file which contains specific markup to distinguish Python codes inside the page. When displayed using a custom web server, it allows interactive execution and editing of the code inside the document. However, it can also be viewed as a usual, nicely-formatted HTML page. The document you are currently reading is itself an IPython notebook.

The command to run the IPython Notebooks web server is the following:

`$ ipython notebook`

When you execute the command above, a new browser window is opened which shows the notebooks in the current folder. The IPython notebook files have the ".ipynb" extension.
