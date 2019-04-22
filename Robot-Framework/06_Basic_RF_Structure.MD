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