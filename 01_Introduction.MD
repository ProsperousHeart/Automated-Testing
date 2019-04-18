# What Is Robot Framework?

[Robot Framework](https://robotframework.org/) is a generic test automation framework for acceptance testing.

What is **acceptance testing**? According to [Agile Alliance](https://www.agilealliance.org/glossary/acceptance/), it is the formal description of a software product's behavior, generally expressed as an example or usage scenario. Or [as per Wikipedia](https://en.wikipedia.org/wiki/Acceptance_testing), it is testing conducted to determine if requirements of a contract or specification are met.

This acceptance testing is used as mostly business users are involved, therefore not necessarily aware about the underlying code. This tool is therefore used to allow for them to not need many programming skills. 

**Robot Framework** has an easy to use tabular syntax, which uses a keywords-driven testing approach. And generally it's libraries are implemented either with Python or Java. We drive our test case with the rows and columns. You use these keywords to perform different tasks.

## Example Framework Code

Here not writing actual programming. Simply using predefined keywords input by the user.

```
*** Test Cases ***
Valid Login
    Open Browser To Login Page
    Input Username  demo
    Input Password  mode
    Submit Credentials
    Welcome PAge Should Be Open
    (Teardown)      Close Bowser
```

## Example Selenium Code

To do the same in Selenium, you must look at the element and then **send_keys**.

```python
From selenium.webdriver import Firefox
executable_file = 'Filepath'
browser = Firefox(execurable_file)
browser.get('https://duckduckgo.com')
browser.find_element_by_id("user").send_keys("abcd")
browser.find_element_by_id("pass").send_keys("abcd")
browser.find_element_by_id("button").click()
browser.close()
```

# How Are Keywords Determined?

Keywords are determined from different libraries.

If you have a task where the keyword is not available or predefined, then you can use Python or Java to write your own.

**Example:** Instead of using multiple keywords to do multiple things, you can write a single one to do multiple. They are also called **user-defined keywords**.

# Advantages & Disadvantages To Robot Framework

## Advantages

Here are just a few of the afvantages for using Robot Framework:

- free (no licensing)
- simple tabular syntax (easy - columns)
- fast development with minimal coding effort
- default reports with detailed information
    - every time a new test is done, a new report is generated
- detailed logs
- generic testing libraries (a lot of them and able to extend)
- supports web testing, Swing, SWT, Windows GUIs, databases, SSH, Telnet, etc
- distributed structure: different sections for test cases, variables, keywords, etc

## Disadvantages

Here are a few disadvantages for using Robot Framework:

- less flexibility (no features like author tag, skip test, no nested loops, etc)

# Test Libraries

Test libraries can be either standard or external, and thus a lot are available with a rich set of keywords.

## Standard Libraries

Libraries that are [standard libraries](http://robotframework.org/robotframework/#standard-libraries) are a "default" set of libraries you can use upon installation.

## External Libraries

Libraries that need to be downloaded & installed to use are called **external libraries**. Here are a few you can find on the [Robot Framework site](https://robotframework.org/):
- [AppiumLibrary](https://github.com/jollychang/robotframework-appiumlibrary): automate mobile application
- [Database Library (Python)](http://franz-see.github.com/Robotframework-Database-Library/):  (also one for Java) this connects to a database
- [HTTP Library (Requests)](https://github.com/bulkan/robotframework-requests/#readme):  library for HTTP level testing to automate REST API
- [SeleniumLibrary](http://github.com/robotframework/SeleniumLibrary/):  automate web based application
- [ExtendedSelenium2Library](https://github.com/rickypc/robotframework-extendedselenium2library): automate an angularJS application
- [SikuliLibrary](https://github.com/rainmanwy/robotframework-SikuliLibrary#readme): automate anything that displays on your screen (UI testing - supports python 2.x and 3.x) 

## Extending Libraries

With **Robot Framework**, you are also able to extend libraries through python programming.

This is used for when there is no built-in keyword nor predefined process.