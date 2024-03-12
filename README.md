# FacialfeaturesDNN
How to extract features from facial images using a pretrained DNN

# Initial steps
## Download Anaconda
Make sure you have Anaconda installed on your system. If you haven't already, you can download it for free from the [Anaconda website](https://www.anaconda.com/download).

## Creating and activating your environment
Once Anaconda is installed, open the Anaconda Powershell Prompt. This command line interface allows you to perform various tasks, including creating Python environments and installing packages. When you open it, you should see the following (or similar):
```console
(base) PS C:\>
```
Note that `(base)` refers to the environment that you are using, which is the default base environment. At this current stage, if you install any python package, it will be installed to your base environment.

Next we want to create a soecific python environment for our task. Think of this environment as a separate section of your computer which is isolated from other components. This separation is important, especially when dealing with packages like TensorFlow and Keras, where compatibility issues between different versions can arise. By maintaining a separate environment, you minimise the risk of inadvertently disrupting the functionality of other Python packages when updating or modifying dependencies.
To create an environment:
```console
(base) PS C:\> conda create -n facestuff
```
In this case, our new environment will be called "facestuff"

To activate this environment:
```console
(base) PS C:\> conda activate facestuff
```
You will notice that `(base)` has changed to `(facestuff)` meaning that we are in a new environment.
```console
(facestuff) PS C:\>
```

## Installing programs and packages into your environment
Next we need to install the necessary programs and packages. Not all versions of python work with tensorflow and keras. So the following are versions of packages and programs that I know work for me.
First we install python version 3.10.9.
```console
(facestuff) PS C:\> conda install python==3.10.9
```

Then install Tensorflow and Keras. 
Install keras version 2.11.0 and tensorflow version 2.11.0
```console
(facestuff) PS C:\> pip install keras==2.11.0
(facestuff) PS C:\> pip install tensorflow==2.11.0
```
Then install jupyter notebook. Jupyter notebook is an interactive programming interface. 
```console
(facestuff) PS C:\> conda install jupyter notebook
```
## Running Jupyter notebook
To launch jupyter notebook:
```console
(facestuff) PS C:\> jupyter notebook
```

You may get an error saying:
```console
(facestuff) PS C:\> jupyter notebook
Traceback (most recent call last):
  File "C:\Users\s4357180\Anaconda3\envs\facestuff\lib\site-packages\requests\compat.py", line 11, in <module>
    import chardet
ModuleNotFoundError: No module named 'chardet'
```

To fix this, install ```chardet```
```console
(facestuff) PS C:\> conda install chardet
```
Now try runnning jupyter notebook again.

Once Jupyter Notebook is up and running, you can proceed to download and open the provided notebook file, "Extracting facial features.ipynb". Follow the instructions within the notebook.
