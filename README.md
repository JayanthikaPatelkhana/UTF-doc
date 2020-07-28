# Univeral Testing Framework

### About UTF
It is a testing framework, where, we run our scripts for automation testing. It is user friendly and easy to handle. Just by writing a single line command we execute the scripts for testing. It has got many features. 
- uploading an excel sheet, 
- record and play back
- script editor

Let's understand the working of the tool and the commands by the example script.
>Example
```sh
open("https://opensource-demo.orangehrmlive.com/");    # opens the URL
click("css=#divUsername > .form-hint");               #clicks on the web element by locating it using the css variable
type("id=txtUsername", "value=Admin");               #types the value "Admin" in the specified text field(located by its id)
type("id=txtPassword", "value=admin123");           # types the value"admin123"  in the specified text field(located by its id)
click("id=btnLogin");                              # clicks on the login button using the target locator.
assertTitle("OrangeHRM");                         # asserts the title of the page
storeText("css=h1","Dashboard");                 # stores the text of an element/page in the variable
echo("$(Dashboard)");                           # prints the message or content stored in the variable
click("css=#menu_time_viewTimeModule > b");    #clicks on the web element
click("id=menu_time_Timesheets");             #clicks on the web element
click("id=employee");                        #clicks on the text field
type("id=employee","Jay");                  # types the text in the text field
sendKeys("id=employee","${KEY_ENTER}");    # send keys does the action of "enter" button.
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

The target locator will be id, css, textLink, Xpath of an element.
>Syntax
```sh
click("elementSelector");
```
* **clickAt**
"clickAt" will click on the element in a specified location.
>Syntax
```sh
clickAt("elementSelector", "coords");
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
* **verifyChecked**
It verifies whether, a radio button/check box is checked. The test execution continues even if the verify fails.
>Syntax
```sh
verifyChecked("elementSelector");
```
* **verifyEditable**
It verifies, if the specified input(text/value) is editable. The test execution continues even if the verify fails.
>Syntax
```sh
verifyEditable("elementSelector");
```
* **verifyElementPresent**
It will verify, if the element is present in the page. The test excution continues even if the verify fails.
>Syntax
```sh
verifyElementPresent("elementSelector");
```
* **verifyElementNotPresent**
It will verify, if the element is not present in the page. The test execution continues even the verify fails.
>Syntax
```sh
verifyElementNotPresent("elementSelector");
```
* **verifyNotChecked**
It verifies whether, a radio button/checkbox is not checked. The test execution continues even if the verify fails.
>Syntax
```sh
verifyNotChecked("elementSelector");
```
* **verifyNotEditable**
It verifies, if the specified input(text/value) is not editable. The test execution continues even if the verify fails.
>Syntax
```sh
verifyNotEditable("elementSelector");
```
* **verifyNotText**
It verifies, if the text of an element is present. The test execution continues even if the verify fails.
>Syntax
```sh
verifyNotText("text/Value");
```
* **verifyTitle**
It will verify whether the title of the current page matches with the provided text. The test execution will continue even if the verify fails.
>Syntax
```sh
verifyTitle("text");
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











 







