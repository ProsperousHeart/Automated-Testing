<a href='https://www.learntocodeonline.com/'>![Learn To Code Online By Clicking Here](../Images/learn-to-code-online.png?raw=true "Learn To Code Online")</a>

# Installation Roadmap

For what will be outlined in this training, you will need to install the following (in order):
1. [Python](https://www.python.org/) (python3 is your best option, however you may want to consider doing [virtual environments](https://github.com/ProsperousHeart/cheatsheets/blob/master/Tools/VirtualEnvironments.md))
2. [PyCharm Community Edition](https://www.jetbrains.com/pycharm/) (free code editor)
3. [Intellibot](https://plugins.jetbrains.com/plugin/7386-intellibot) - plugin used if you want to support robot programming in PyCharm (supports robot keywords)
4. [PIP](https://pypi.org/project/pip/) - python install manager used to install libraries
5. [Robot Framework](https://robotframework.org/)
6. [SeleniumLibrary](http://github.com/robotframework/SeleniumLibrary/) - and external library for Robot Framework

# Setup On Windows 64bit Machine

Quick Tip:  I've touched on installation and [environment variable setup](https://github.com/ProsperousHeart/cheatsheets/blob/master/Processes/SetEnvVars.md) in my [basic python training](https://github.com/ProsperousHeart/TrainingUsingJupyter/tree/master/Python/Basics) (all done in JupyterNotebooks).

I would also highly suggest learning about [virtual environments](https://github.com/ProsperousHeart/cheatsheets/blob/master/Tools/VirtualEnvironments.md) - especially with [virtualenv-wrapper](https://github.com/ProsperousHeart/cheatsheets/blob/master/Processes/virtualenvs.md)!

1. Download latest version of [Python](https://www.python.org/)

2. Install Python

You can choose the predefined location or a customized location with which to install python.

Be sure to choose **customize installation** if you wish to install to a customized location.

Many programmers prefer to have a single location for their different languages, so you might consider installing it:
`C:\PythonVER` wherein VER is the version ... like `C:\Python37` for 3.7 version.

3. Setup Environment Variable

    1. Go to location where python is installed. (If you have more than one version of python, it is wise to add the version to the `python.exe` file.)
    2. This executable is what you will need to ensure is in your environment variables.
        1. Copy the address of the file's location
        2. Right click on **My Computer** and choose **Properties**
        3. Go to **Advanced System Settings**
        4. Go to **Environment Variable**
    3. Check the **System Variables** > **Path** variable. Add your location to this path using a `;` to separate multiple paths.
    
    You can also press the Windows key and search for **environment variable** and it should pull it up as well.
    
    From here, you should be able to open a command prompt and run `python -V` to see the version. If it shows, it works! 