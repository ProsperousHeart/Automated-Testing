<a href='https://www.learntocodeonline.com/'>![Learn To Code Online By Clicking Here](../Images/learn-to-code-online.png?raw=true "Learn To Code Online")</a>

# Introduction

This section will show a basic structure of the Robot Framework Code. So whenever you wish to automate web-based applications, you will create a basic project structure to create for it.


## Explanation Of Keywords

There are 2 types of keywords:
- built-in (exist in test libraries)
- user defined (created by automation tester)


## Extensions You May See

These files are created with the Robot extension:
- `.robot` file is used for test cases
- `.py` for python files

There may be any other extension you might need (XLSX, txt, etc) but at least the two above.


# Setup Your File Structure

For best practices, here are the folders suggested to have in each automation project's base project directory folder:

1. JsonFiles

2. Resources

    This is where we will have a robot file that will behave as a resource.

    Robot Framework provides a lot of keywords to perform different tasks. This resource file is where you would provide your user-created keywords.

    Keywords can be created by directly writing python files or you can use existing keywords, merge them, and create a new keyword.

3. TestCases


# Steps To Create Robot Framework Code

1. Create a new project in PyCharm, for example:  `RobotAutomation`

2. Setup your folder structure as outlined [above](#Setup-Your-File-Structure)

3. Add new `.robot` files for testing in the `TestCases` folder.


# What Goes In A Test Case File?

Each test case is broken up into multiple sections, with each section having a specific use.

## Settings

This is the area where we will write our configuration. So if you wish to import any library, use any resources, or ANYTHING you want to import or add in settings for the test case? This is where that goes.

The settings section is denoted by a single line:  `*** Settings ***`

## Variables

This section is denoted by a single line:  `*** Variables ***`

The **variables** section is where all variables are declared.

## Test Cases

This section is denoted by a single line:  `*** Test Cases ***`

All test cases are written here.

## Keywords

This section is denoted by a single line:  `*** Keywords ***`

If you wish to create any user-defined keywords you can write it here. It is an option, but provide more value for you to keep all of your keywords in the `Resources` folder.

Therefore this section is optional for Test Case files.

**NOTE:** A resources file will have all but the `*** Test Cases ***` section as a requirement.


# Writing A Test Case

Here are the steps to creating a test case:

1. create a robot file in the `TestCases` folder

2. create sections (as outlined previously with settings, variables, and test cases)

3. define libraries

    You can define these after you have installed them using:
    `Library  LibraryName`
    
    For example:
    
    ``` python
    *** Settings ***
    Library  SeleniumLibrary
    
    *** Variables ***
    
    *** Test Cases ***
    
    *** Keywords ***
    ```

4. define variable
    
    You can define a variable using `${varName}` with 2 spaces and then the value.
    
    For example:
    
    ``` python
    *** Settings ***
    Library  SeleniumLibrary
    
    *** Variables ***
    ${Browser}  Chrome
    ${URL}  http://learntocodeonline.com
    
    *** Test Cases ***
    
    *** Keywords ***
    ```
    
    **NOTE:** you will need to download the [ChromeDriver](http://chromedriver.chromium.org/) if using Chrome to allow for automated testing of webapps across many browsers. Once downloaded:
        - unzip the ZIP file
        - copy the ChromeDriver.exe file
        - put it into your python > scripts folder (as well as within the virtual environment's scripts folder)
    
    Should you wise to use another browser, you will need:
    - [geckodriver.exe](https://github.com/mozilla/geckodriver/releases) for FireFox
    
    You will then follow the same process to put the EXE into the respective Scripts folder. 

5. write test case to start and close browser
    
    You will give a name to the test case.
    
    The test case info will start on the next line and a tab.
    
    Use keyword, 2 spaces and then the arguments:
    - URL variable name to open
    - variable name to affect and 2 spaces
    
    For example:
    
    ``` python
    *** Settings ***
    Library  SeleniumLibrary
    
    *** Variables ***
    ${Browser}  Chrome
    ${URL}  http://learntocodeonline.com
    
    *** Test Cases ***
    TC_001 Browser Start and Close
        Open Browser  ${URL} ${Browser1}
        Close Browser
    
    *** Keywords ***
    ```
    
    You can even add multiple browsers - just need to have different test cases for each.
    
    ``` python
    *** Settings ***
    Library  SeleniumLibrary
    
    *** Variables ***
    ${Browser0}  Chrome
    ${Browser2}  Firefox
    ${URL}  http://learntocodeonline.com
    
    *** Test Cases ***
    TC_001 Browser Start and Close
        Open Browser  ${URL} ${Browser1}
        Close Browser
    
    TC_002 Browser Start and Close
        Open Browser  ${URL} ${Browser2}
        Close Browser
    ```

# Executing a Test Case

1. Right click on the test case ROBOT file then copy the path.
2. Move to the location in command prompt that the file is stored in
3. Run `robot FILENAME.robot`

# Keyword Suggestions For Robot Framework

To get keyword suggestions, you will need to install the `Intellibot with SeleniumLibrary` plugin for PyCharm. (Be sure you have uninstalled the Intellibot one from 2016 and restarted your IDE.)

This should remove any of the red underlines for some of the keywords, as well as provide suggestions.

Once you have installed the new plugin and restarted your PyCharm, go to:  `File > Settings`