<a href='https://www.learntocodeonline.com/'>![Learn To Code Online By Clicking Here](../Images/learn-to-code-online.png?raw=true "Learn To Code Online")</a>

# Table Of Contents

1. ???
    - [What Is An Element Locator?](#what-is-an-element-locator)
    - [Understanding HTML Basics](#understanding-html-basics)
    - [Locate Element By Id](#locate-element-by-id)
    - [Locate Element By Name](#locate-element-by-name)
    - [Locate Element By Link Text](#locate-element-by-link-text)
    - [Locate Element Using CSS](#locate-element-using-css)
    - [Locate Element by Xpath](#locate-element-by-xpath)

# What is an Element Locator?

You use **element locators** when you are looking to locate an element uniquely on a page.

There are 5 different element locators:
1. [Id](#locate-element-by-id)
2. [Name](#locate-element-by-name)
3. [Class name](#locate-element-by-link)
4. [CSS](#locate-element-using-css)
5. [Xpath](#locate-element-by-xpath)

Process:
- check for HTML element of the item you wish to automate
    - right click on object
    - choose `Inspect` on Chrome, `Inspect Element` on FireFox
- install following extensions:
    - Chrome:  [`CSS and XPath checker`](https://chrome.google.com/webstore/detail/css-and-xpath-checker/aoinfihhckpkkcpholfhmkeplbhddipe?hl=en)
    - FireFox:  [selenium ide](https://www.google.com/url?sa=t&rct=j&q=&esrc=s&source=web&cd=3&cad=rja&uact=8&ved=2ahUKEwjGpL34qrfiAhUM7qwKHf44DDMQFjACegQIAhAB&url=https%3A%2F%2Faddons.mozilla.org%2Fen-US%2Ffirefox%2Faddon%2Fselenium-ide%2F&usg=AOvVaw11tnO5HvZa79irtqKUspLY)
    
The reason why these extensions were added was because whenever you use any automation tool (not just Selenium), you need these locators.

# Understanding HTML Basics

## Understand HTML Basics

Example of a site:  http://thetestingworld.com/testings

1. right click on an element and `inspect`
2. copy the HTML

HTML is written in tags. Each piece starts with it's own tag, and then has multiple attributes, such as:
- class
- name
- required
- type
- placeholder
- value

Text between starting and end tags is called:  `inner text`

## Use Of Plugins

### CSS and XPAth Checker

When on the page you wish to find elements for, click on the extension button.
Choose the radio button that matches what you're looking for (CSS or XPath), such as:
    
    label[for="tab2"]

This will higlight the element with which you are seeking to check or work on.

### Selenium IDE

1. Click on the extension on Firefox.
2. Choose `Record new test in a new project`
3. Give it a name
4. Cancel for recording
5. Click on first line and give command (not used right now)
6. In `Target` run:  `css=label[for='tab2']`
7. Click on magnifying glass for it to search and locate on the page

# Locate Element By Id

`id` is an HTML attribute. You want to ensure it's unique - whether as a developer or as a tester.

To ensure this is unique, run the following example (with the `id` you're looking for):
- **CSS & XPath Checker**:  ?
- **Selenium IDE**:  `id=email`

# Locate Element By Name

Same process as [by ID](#locate-element-by-id)

# Locate Element By Link Text

Same process as [by ID](#locate-element-by-id) - just use:
- Chrome
- **Selenium IDE**:  `link=some_text`

# Locate Element Using CSS

## Syntax 1

This section will cover use of `id` of the element, and `tag` with `id`.

## Locating by ID

`css=#email` since the `#` indicates it is an ID. This will work on **Selenium IDE**.

The `#email` will also work in the Chrome browser extension.

## Locating By TAG With ID

`css=TAGTYPE#ID` such as `css=input#email` on the Facebook login page.

## Syntax 

## Syntax 

## Syntax 

## Syntax 

# Locate Element by Xpath

## Syntax 
## Syntax 
## Syntax 
## Syntax 
## Syntax 
## Syntax 
## Syntax 
## Syntax 
## Syntax 
## Syntax 
## Syntax 