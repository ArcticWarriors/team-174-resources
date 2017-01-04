# Python

Python is a very powerful scripting language, that doesn't have a lot of the cumbersome syntax of C++ or Java.  On the team, we currently use it for plotting tools and webdesign, but it could be expanded in the future.

## Installing Python

Go to https://www.python.org/downloads/ Download the latest stable version of 2.7 It should have simple installation instructions

### Fixing your PATH
In somebodies infinite wisdom, when you install python it does not update your path to point to the Scripts folder, which is pretty important if you want to do anything but “Hello World”  We will have to update your system path, which requires admin privileges, and you have the potential of f-ing up.  I will be talking in terms of Windows 7, but I imagine it isn’t too different for 8 or 10.  Worst case, google how to update environment variables.

Open up explorer, and navigate to “Computer”
Right click in empty space, and select “Properties”
Click on “Advanced System Settings”, then “Environment Variables”
You should see a window like this.  Go to the “Path” variable, and click edit
You want to make sure that both `C:\<wherever python is>/` and `C:\<wherever python is>\Scripts` are in there.  Make sure that you don’t delete all the other garbage in there, that would probably wreck some havoc.  When you add the path, you delimiter them with a semicolon, like `<everything that was there before>;C:\Python27;C:\Python2\Scripts;`
Whenever you change envvars, you have to close any consoles you have open and reopen them.  There have been times at work where I have had to rage-logged-off for them to take effect.
Close anything related to this.  The same thing happens with eclipse, shut it down and start it back up


### General tool installation
Most of the tools that we use are fairly common, and can be installed with easy_install, pip, or by using the setup scripts.

If they work, pip and easy_install are the easiest to use.  From the command line, you can simply type in
* pip install <tool_name>  (i.e. pip install matplotlib)
* OR easy_install <tool_name> (i.e. easy_install matplotlib)

This method may complain that you are missing the windows compiler.  It should print out a link to a website where you can download the necessary tools.  Do that, re-open your command window, and try again.

The more old-school way to do this, is to download the source code, and use the given setup script to install the plugins.  Most sites have a .zip file, or a .tar.gz file that you can download and extract.  If you open a command window in there, and run (without quotes) "setup.py install"  The tool will install

NOTE: You will probably need to install "Microsoft Visual C++ Compiler for Python 2.7" for the install tools to work.  So if you get errors go to the site the error message says to download and install the required files.  (i.e. http://aka.ms/vcpython27)

## Python Tools

### PyDev
PyDev is an Eclipse plugin that does syntax highlighting, auto-completion and all that other good IDE stuff for python.  Their instructions are here, if you need more help, let me know.  
On the website scroll down to “Installing with the update site” and follow the instructions there.
http://www.pydev.org/manual_101_install.html 

### numpy
numpy is a numeric processing engine that works very similar to MATLAB under the hood.  It is very fast and efficient at matrix multiplication and doing some array manipulation.  This is required for matplotlib to work, and if you follow those instructions you should get this as well.

### Matplotlib
Matplotlib is a tool that allows us to create dynamic plots with python.  It uses a similar syntax to MATLAB, and can be used as a replacement for it.  I used pip to install this on my new computer

### Django
Django is a tool that allows us to create a decently complicated backend for a webservice.  Websites like Instagram, Pintrest and the Onion all use Django to power their websites.  We have a whole page dedicated to [Django](https://github.com/ArcticWarriors/snobot2015/wiki/Django) located here
