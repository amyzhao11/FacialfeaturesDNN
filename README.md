# FacialfeaturesDNN
How to extract features from facial images using a pretrained DNN

# Initial steps
Download [Anaconda](https://www.anaconda.com/download) for free

Once downloaded, you should have access to Anaconda Powershell Prompt. This is a command line interface that allows you to do things such as create python environments and install packages.

# Inside Anaconda Powershell Prompt
## Creating and activating your environment
Once open, you should see (or similar):
```console
(base) PS C:\>
```
Note that (base) refers to the environment that you are using, which is the default base environment. At this current stage, if you install any python package, it will be installed to your base environment.

Next, we want to create a separate environment for the task at hand. You can think of this as a separate section of your computer that is isolated from other sections. This is important for installing tensorflow and keras because some package versions do not agree with one another, so it is good to keep that separate in case updating one thing might affect the functionality of some other python package that you might use.
To create an environment:
```console
(base) PS C:\> conda create -n facestuff
```

In this case, our new environment will be called "facestuff"

To activate this environment:
```console
(base) PS C:\> conda activate facestuff
```
You should then see instead of ```(base)```, you will see that your current environment is ```(facestuff)```. 
```console
(facestuff) PS C:\>
```

## Installing programs and packages into your environment
Next we need to install the necessary programs and packages.

I found out the hard way that not all versions of python work with tensorflow and keras. So the following are versions of packages and programs I know that work for me.
First we install python version 3.10.9.
```console
(facestuff) PS C:\> conda install python==3.10.9
```

Then we install tensorflow and keras (these are the packages that will run the neural networks). While we can install them within python later, I prefer to install them early. Installing a different python package first might prevent these specific package versions from installing.
Install keras version 2.11.0
```console
(facestuff) PS C:\> pip install keras==2.11.0
```
Install tensorflow version 2.11.0
```console
(facestuff) PS C:\> pip install tensorflow==2.11.0
```

Then install jupyter notebook. Jupyter notebook is a programming interface that is beginner friendly. You can run chunks of code at a time and the output will display under those codeblocks.
```console
(facestuff) PS C:\> conda install jupyter notebook
```

