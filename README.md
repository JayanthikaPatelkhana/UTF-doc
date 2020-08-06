# Univeral Testing Framework

### About UTF
It is a testing framework, where, we run our scripts for automation testing. It is user friendly and easy to handle. Just by writing a single line command we execute the scripts for testing. It has got many features. 
- uploading an excel sheet, 
- record and play back
- script editor
```sh
#============================================================
# This Test Case is an example to show case the functionality
# It uses an HR Management Demo Website for demonstration
#============================================================

#open website
open("https://opensource-demo.orangehrmlive.com/");

username="Admin";
password="admin123";

#Enter login credentials
type("id=txtUsername",username);
type("id=txtPassword",password);

#click on login
click("id=btnLogin");

#check if login was successfuly by verifying Welcome Message
assertText("id=welcome1","Welcome "+username);

#click on Admin Tab
click("xpath=/html/body/div[1]/div[2]/ul/li[1]/a/b");

#search for user admin
type("id=searchSystemUser_userName", username);

#click on search button
click("id=searchBtn");

#check if user admin is found  
assertText("xpath=/html/body/div[1]/div[3]/div[2]/div/div/form/div[4]/table/tbody/tr/td[2]/a",username);
```

## Element Selector

Element selector is a command used to locate/identify web element in a web page and operate the web element using the UTF commands. To precisely locate/identify a Web element and create an automation script different element selectors are used.


 * "id" is an element selector, which locates/identifies a web element by its "id" and returns value of an element or perform action on an element.
 >format : "id = id of an element"

 * "name" is an element selector, which locates/identifies a web element by its name and returns value of an element or perform action on an element.
 >format : "name = name of an element"

 * "linkText" is an element selector, which locates/identifies a text or link in the web page.
 >format : "linkText = Text_of_Link"

 * "css" is an element selector, which loactes/identifies a web element by its CSS class in the web page.
 >format : "css = tag.(id/class/name)"


 * "Xpath" is an element selector, which locates/identifies a web element by the Xpath in a web page and returns value of an element or perform action on an element.
 >format : "Xpath = //tagname[@attribute='value']"


## UTF commands



* **addSelection**


It adds a selection to the set of options in a multi-select element.
>Syntax
```sh
addSelection("elementSelector","value");
```

* **assert**

It checks whether a variable is an expected value. The variable's value will be converted to a string for comparison. The test will stop if the assert fails.
>Syntax
```sh
assert("elementSelector", "value");
```

* **assertAlert**

It checks for the alert with the provided text. The test will stop if the assert fails.
>Syntax
```sh
assertAlert("value");
```

* **assertConfirmation**

It checks that a confirmation has been rendered. The test fails if the assert fails.
>Syntax
```sh
assertConfirmation("value");
```

* **assertChecked**


The "assertChecked" command is used to confirm, that the element is checked or not. The test case execution stops if the assert fails.
>Syntax
```sh
assertChecked("elementSelector");
```
* **assertNotChecked**


The "assertNotChecked" command is used to confirm, that the element is not checked. The test case execution stops if the assert fails.


>Syntax
```sh
assertNotChecked("elementSelector");
```

* **assertPrompt**

It checks whether a prompt has been rendered. The test case execution stops if the assert fails.

>Syntax
```sh
assertPrompt("value");
```

* **assertSelectedLabel**

It confirms that the label of the selected option in a dropdown element contains the provided value?text. The test will stop if the assert fails.

>Syntax
```sh
assertSelectedLabel("elementSelector", "value/Text");
```

* **assertSelectedValue**

It confirms that the value attribute of the selected option in a dropdown element contains the provided value. The test will stop if the assert fails.

>Syntax
```sh
assertSelectedValue("elementSelector", "value");
```

* **assertText**


The "assertText" command is used to confirm, that the text of an element equals the text provided. The test case execution stops if the assert fails.

>Syntax
```sh
assrtText("elementSelector", "text");
```

* **assertTitle**


The "assertTitle" command is used to confirm, that the title of the current page equals the text provided. The test case execution stops if the assert fails.

>Syntax
```sh
assertTitle("text");
```

* **assertValue**


The "assertValue" command will confirm the value of an input field. For checkbox/radio elements, the value will be "on" or "off" depending on whether the element is checked or not. The test will stop if the assert fails.

>Syntax
```sh
assertValue("elementSelector", "text/value");
```

* **assertElementPresent**

It checks whether the element is present in the page. The test execution will stop if assert fails.
>Syntax
```sh
assertElementPresent("elementSelector", "value");
```

* **assertElementNotPresent**

It checks if the element is not present in the page. The test execution stops if assert fails.
>Syntax
```sh
assertElementNotPresent("elementSelector", "value");
```

* **assertNotSelectedValue**

It checks the value attribute of the selected option in a dropdown element does not contain the provided value. The test will stop if the assert fails.

>Syntax
```sh
assertNotSelectedValue("elementSelector", "value");
```

* **assertEditable**


The "assertEditable" is used to check whether the element is editable. The test execution stops if the assert fails.
>Syntax
```sh
assertEditable("elementSelector");
```

* **assertNotEditable**


The "assertNotEditable" will check whether the element is not editable. The test execution will stop if the assert fails.
>Syntax
```sh
assertNotEditable("elementSelector");
```

* **assertNotText**


The "assertNotText" will check, if the text of an element does not contain the provided text.
>Syntax
```sh
assertNotText("elementSelector", "value/text");
```



* **check**


The "check" command , checks on the checkbox or a radio button. It does the similar action of clicking a button or checkbox in a webpage.


>Syntax
```sh
check("elementSelector");
```

* **click** 


"click" command is used to click / select an hyperlink, button, radio option and checkbox option. 


>Syntax
```sh
click("elementSelector");
```
* **clickAt**


"clickAt" will click / select a hyperlink, button, radio option and checkbox option in a specified location using the coordinates relative to the element.

>Syntax
```sh
clickAt("elementSelector", "coords");
```

* **close**

It closes the current window.
>Syntax
```sh
close;
```

* **doubleClick**


It will "doubleClick" on the element.
>Syntax
```sh
doubleClick("elementSelector");
```
* **doubleClickAt**


"doubleClickAt" will double click on an element at specified coordinated location of the element.
>Syntax
```sh
doubleClickAt("elementSelector", "coords");
```

* **dragAndDropToObject**

It drags an element from a location and drops it on other element location.
>Syntax
```sh
dragAndDropToObject("elementSelector", "value");
```

* **echo**


The "echo" command prints the message specified. It is used for debugging , whether a specific command/value is executed.

>Syntax
```sh
echo("message to print");
```


 

* **mouseOut** 


The "mouseOut" command is used for moving the mouse pointer away from the specified element.

>Syntax
```sh
mouseOut("elementSelector");
```

* **mouseDown**


"mouseDown" simulates the event to press the mouse button.
>Syntax
```sh
mouseDown("elementSelector");
```

* **mouseDownAt**


"mouseDown" simulates the event to press the  mouse button at specified location.
>Syntax
```sh
mouseDownAt("elementSelector", "coords");
```

* **mouseMove**

The "mouseMove" will simulate a user to press the mouse button.
>Syntax
```sh
mouseMove("elementSelector");
```

* **mouseMoveAt**


The "mouseMoveAt" will simulate a user to press the mouse button at specified location.
>Syntax
```sh
mouseMoveAt("elementSelector", "coords");
```

* **mouseOver**


The "mouseOver" simulates a user to hover on the specified element.
>Syntax
```sh
mouseOver("elementSelector");
```

* **mouseUp**


"mouseUp" simulates the event of releasing the mouse button, stops holding the button down.
>Syntax
```sh
mouseUp("elementSelector");
```

* **mouseUpAt**
"mouseUpAt" simulates the event of releasing the mouse button, stops holding the button down at specified location.
>Syntax
```sh
mouseUpAt("elementSelector", "coords");
```


* **open**


The "Open" command opens the URL in the current selected browser tab. The open command takes a full URL as input (recommended) or a path relative to the baseurl (outdated).

>Syntax
```bsh
open("URL");
```
* **pause**


It will hold/wait the test execution for specified time.

>Syntax
```sh
pause("Wait time in milliseconds");
```
* **runScript**


The "runScript" command is used to execute a Javascript code. It creates a new script tag in the current test window and adds the specified text into the body of the command.

>Syntax
```sh	
runScript("elementSelector");
```
* **removeSelection**


It helps to remove a selection from the set of selected options in a multi-select element using a value/locator
>Syntax
```sh
removeSelection("elementSelector", "value");
```
* **select**

It selects an element from the drop-down menu using any of the elementSelector. If elementSelector is not provided, a match can be attempted using the label/Text of the element.
>Syntax
```sh
select("elementSelector", "Text");
```

* **selectFrame**

Selects a frame within the current window. You can select a frame by its 0-based index number (e.g., select the first frame with "index=0", or the third frame with "index=2"). For nested frames you will need to invoke this command multiple times (once for each frame in the tree until you reach your desired frame). You can select the parent frame with "relative=parent". To return to the top of the page use "relative=top".
>Syntax
```sh
selectFrame("elementSelector");
```

* **selectWindow**

It selects a popup window using window locator and later on the required actions will be done on the selected window.
>Syntax
```sh
selectWindow("elementSelector");
```

* **sendKeys** 


The sendKeys command simulates keystroke events on the specified element, as though you typed the value key-by-key.Sendkeys can send the ${KEY_ENTER} key event. This means it will kind of work same as user pressing ENTER using the keyboard.

>Syntax
```sh
sendKeys("elementSelector", ${KEY_ENTER});
```
* **setWindowSize**


The "setWindowSize" will set the size of the browser's window.
>Syntax
```sh
setWindowSize("width X height");
```
* **storeText** 


The "storeText" command is used to store the text value of an element in a variable of the web page for the later use.

>Syntax
```sh	
storeText("elementSelector","value");
```


* **store** 


The "store" command is used to store some data for later use.

>Syntax
```sh	
store("elementSelector", "variable name");
```


* **storeValue** 


The "storevalue" command is used to get the value of an element and is stored in a variable for later use.

>Syntax
```sh
storeValue("elementSelector", "variable name");
```
 

* **storeTitle** 


The "storeTitle" command gets the title of the current page.

>Syntax
```sh
storeTitle("elementSelector", "variable name");
```

* **storeAttribute**


"storeAttribute" will get the value of an element attribute. The attribute value may differ depending on the browser.
>Syntax
```sh
storeAttribute("elementSelector", "variable name");
```

* **storeWindowHandle**

It gets the handle of the window/tab of the current page.

>Syntax
```sh
storeWindowHandle("elementSelector");
```

* **type** 


"type" command is one of the commands, mainly used to type text into the text box and text area fields.
>Syntax
```sh
type("elementSelector", "value to input");
```
* **uncheck**


The "uncheck" command , unchecks on the checkbox or a radio button. It does the similar action of clicking a button or checkbox in a webpage for unchecking the element.

>Syntax
```sh
uncheck("elementSelector");
```

* **verify**

It just verifies a variable is an expected value. The variable's value will be converted to a string for comparison. The test will continue even if the verify fails.
>Syntax
```sh
verify("elementSelector", "value");
```
* **verifyChecked**


It just verifies whether, a radio button/check box is checked. The test execution continues even if the verify fails.
>Syntax
```sh
verifyChecked("elementSelector");
```
* **verifyEditable**


It just verifies, if the specified input(text/value) is editable. The test execution continues even if the verify fails.
>Syntax
```sh
verifyEditable("elementSelector");
```
* **verifyElementPresent**


It will just verify, if the element is present in the page. The test excution continues even if the verify fails.
>Syntax
```sh
verifyElementPresent("elementSelector");
```
* **verifyElementNotPresent**


It will just verify, if the element is not present in the page. The test execution continues even the verify fails.
>Syntax
```sh
verifyElementNotPresent("elementSelector");
```

* **verifyNotSelectedValue**

It just verifies, whether the expected value is not selected from the drop down list. The test will continue even if verify fails.
>Syntax
```sh
verifyNotSelectedValue("elementSelector", "value");
```

* **verifyNotChecked**


It just verifies whether, a radio button/checkbox is not checked. The test execution continues even if the verify fails.
>Syntax
```sh
verifyNotChecked("elementSelector");
```
* **verifyNotEditable**


It just verifies, if the specified input(text/value) is not editable. The test execution continues even if the verify fails.
>Syntax
```sh
verifyNotEditable("elementSelector");
```
* **verifyNotText**


It just verifies, if the text of an element is present. The test execution continues even if the verify fails.
>Syntax
```sh
verifyNotText("text/Value");
```

* **verifySelectedLabel**

It just verifies, whether the label of a selected element in a drop-down menu, matches the provided value/text. The test continues even if the verify fails.
>Syntax
```sh
verifySelectedLabel("elementSelector", "Text");
```

* **verifySelectedValue**

It just verifies, whether the expected element has been chosen in a select menu by its value. The test will continue even if the verify fails.
>Syntax
```sh
verifySelectedValue("elementSelector", "value");
```

* **verifyText**

It just verifies, whether the text provided matches the text of an element in the page. The test continues even if verify fails.

>Syntax
```sh
verifyText("elementSelector","text");
```

* **verifyTitle**


It will just verify whether the title of the current page matches with the provided text. The test execution will continue even if the verify fails.
>Syntax
```sh
verifyTitle("text");
```
* **verifyValue**

It will just verify the value of an input field.For checkbox/radio elements, the value will be "on" or "off" depending on whether the element is checked or not. The test will continue even if the verify fails.

>Syntax
```sh
verifyValue("elementSelector","value");
```

* **waitForElementEditable**


It will wait for some time for the value/text of an element to be editable.
>Syntax
```sh
waitForElementEditable("elementSelector","wait time in ms");
```

* **waitForElementPresent**


It will wait some time for the target element to be present in the page.
>Syntax
```sh
waitForElementPresent("elementSelector", "wait time in ms");
```
 
* **waitForElementNotPresent**


It will wait some time for the target element not to be present in the page.
>Syntax
```sh
waitForElementNotPresent("elementSelector", "wait time in ms");
```

* **waitForElementVisible**


It will wait some time for the target element to be visible in the page.
>Syntax
```sh
waitForElementVisible("elementSelector", "wait time in ms");
```
* **waitForElementNotEditable**

It will wait for an element not to be editable.
>Syntax
```sh
waitForElementNotEditable("elementSelector", "wait time in ms");
```

* **waitForElementNotVisible**


It will wait some time for the target element not to be visible in the page.
>Syntax
```sh
waitForElementNotVisible("elementSelector","wait time in ms");
```




















## Control Flow





* **if**

The "if" command is the conditional block and terminates with "end". It evaluates the Javascript expression.
>Syntax
```sh
if(condition)
{
statement;
}
```











 







