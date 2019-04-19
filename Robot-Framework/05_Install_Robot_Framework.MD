<a href='https://www.learntocodeonline.com/'>![Learn To Code Online By Clicking Here](../Images/learn-to-code-online.png?raw=true "Learn To Code Online")</a>

In this section, we will be using `pip` to install our required packages.

But before we do that, I woudd HIGHLY enourage you to get in the habit of doing [virtual environments](https://github.com/ProsperousHeart/cheatsheets/blob/master/Tools/VirtualEnvironments.md).

While you likely want this available to all future projects (and therefore will not want to do this in a virtual environment) I would suggest using this for testing.

# Setting Up Virtual Environments

I personally LOVE using [virtualenv](https://github.com/ProsperousHeart/cheatsheets/blob/master/Processes/virtualenvs.md#virtualenv) with [virtualenvwrapper](https://github.com/ProsperousHeart/cheatsheets/blob/master/Processes/virtualenvs.md#virtualenvwrapper).

## Installing Appropriate Packages

As per [my cheatsheet](https://github.com/ProsperousHeart/cheatsheets/blob/master/Processes/virtualenvs.md), run these commands in your command prompt:
- `pip install virtual env` - test your installation by running `virtualenv --version`
- `pip install virtualenvwrapper` or if you're on Windows `pip install virtualenvwrapper-win`

## Creating A Virtual Environment With Virtual Project Directory

Once you have virtualenv and virtualenvwrapper (or virtualenvwrapper-win for Windows) installed, you will follow this process.

Bear in mind that your virtual environments are normally located in:  `HOMEDIRECTORY\Envs`

The following steps can be used within an [Anaconda setup](https://github.com/ProsperousHeart/cheatsheets/blob/master/Tools/Anaconda.md), however the process is still the same.

1. Change directory into the main folder that will house all of your projects. (If you don't have on already, create one immediately in your home user folder. I have one called `workspace`.)
2. Make a directory in that folder for your project name:  `mkdir PROJECTNAME`
3. Change directory into that new folder:  `cd PROJECTNAME`
4. Create your virtual environment (I name it the same as my project):  `mkvirtualenv ENVNAME`
5. Create your project directory where PATH is the folder of your project:  `setprojectdir PATH`
6. Deactivate your virtual environment:  `deactivate`

Now, whenever you are ready and no matter what folder you are looking in at the time?

If you run `workon ENVNAME` not only will it start up your virtual environment, but it will also move you into the project folder.

Be sure to deactivate when done:  `deactivate`

# Installation Of Robot Framework Packages

Perform these actions from within your virtual environment. You will need to run:  `workon ENVNAME`

To deactivate, run:  `deactivate`

1. Install Robot Framework:  `pip install robotframework`
2. Install **SeleniumLibrary** (updated version of **Selenium2Library**):  `pip install robotframework-seleniumlibrary`