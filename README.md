# Univeral Testing Framework

### About UTF
It is a testing framework, where, we run our scripts for automation testing. It is user friendly and easy to handle. Just by writing a single line command we execute the scripts for testing. It has got many features. 
- uploading an excel sheet, 
- record and play back
- script editor

Let's understand the working of the tool and the commands by the example script.
>Example
```bh
open("https://opensource-demo.orangehrmlive.com/");  // opens the URL
click("css=#divUsername > .form-hint");   //clicks on the web element by locating it using the css variable
type("id=txtUsername", "value=Admin");   // types the value "Admin" in the specified text field(located by its id)
type("id=txtPassword", "value=admin123"); // types the value"admin123"  in the specified text field(located by its id)
click("id=btnLogin"); // clicks on the login button using the target locator.
assertTitle("OrangeHRM"); // asserts the title of the page
storeText("css=h1","Dashboard"); // stores the text of an element/page in the variable
echo("$(Dashboard)"); // prints the message or content stored in the variable
click("css=#menu_time_viewTimeModule > b"); //clicks on the web element
click("id=menu_time_Timesheets"); //clicks on the web element
click("id=employee");  //clicks on the text field
type("id=employee","Jay"); // types the text in the text field
sendKeys("id=employee","${KEY_ENTER}"); // send keys does the action of "enter" button.
```



## UTF commands



* **open**
The "Open" command opens the URL in the current selected browser tab. The open command takes a full URL as input (recommended) or a path relative to the baseurl (outdated).

>Syntax
```bsh
open("URL");
```
* **setWindowSize**
The "setWindowSize" will set the size of the browser's window.
>Syntax
```sh
setWindowSize("width X height");
```


* **click** 
"click" command is used to click / select an hyperlink, button, radio option and checkbox option. 

The target locator will be id, css, textLink, Xpath of an element.
>Syntax
```sh
click("target locator");
```
* **clickAt**
"clickAt" will click on the element in a specified location.
>Syntax
```sh
clickAt("target locator", "coords");
```
* **doubleClick**
It will "doubleClick" on the element.
>Syntax
```sh
doubleClick("target locator");
```
* **doubleClickAt**
"doubleClickAt" will double click on an element at specified coordinated location of the element.
>Syntax
```sh
doubleClickAt("target location", "coords");
```
* **type** 
"type" command is one of the commands, mainly used to type text into the text box and text area fields.
>Syntax
```sh
type("target locator", "value to input");
```
* **sendKeys** 
The sendKeys command simulates keystroke events on the specified element, as though you typed the value key-by-key.Sendkeys can send the ${KEY_ENTER} key event. This means it will kind of work same as user pressing ENTER using the keyboard.

>Syntax
```sh
sendKeys("target locator", ${KEY_ENTER});
```
 

* **mouseOut** 
The "mouseOut" command is used for moving the mouse pointer away from the specified element.

>Syntax
```sh
mouseOut("target locator");
```

* **mouseDown**
"mouseDown" simulates the event to press the mouse button.
>Syntax
```sh
mouseDown("target locator");
```

* **mouseDownAt**
"mouseDown" simulates the event to press the  mouse button at specified location.
>Syntax
```sh
mouseDownAt("target locator", "coords"),
```

* **mouseMoveAt**
The "mouseMoveAt" will simulate a user to press the mouse button at specified location.
>Syntax
```sh
mouseMoveAt("target locator", "coords");
```

* **mouseOver**
The "mouseOver" simulates a user to hover on the specified element.
>Syntax
```sh
mouseOver("target locator");
```

* **mouseUp**
"mouseUp" simulates the event of releasing the mouse button, stops holding the button down.
>Syntax
```sh
mouseUp("target locator");
```
* **storeText** 
The "storeText" command is used to store the text value of an element in a variable of the web page for the later use.

>Syntax
```sh	
storeText("target locator","value");
```


* **store** 
The "store" command is used to store some data for later use.

>Syntax
```sh	
store("text", "variable name");
```


* **storeValue** 
The "storevalue" command is used to get the value of an element and is stored in a variable for later use.

>Syntax
```sh
storeValue("target locator", "variable name");
```
 

* **storeTitle** 
The "storeTitle" command gets the title of the current page.

>Syntax
```sh
storeTitle("target locator", "variable name");
```

* **storeAttribute**
"storeAttribute" will get the value of an element attribute. The attribute value may differ depending on the browser.
>Syntax
```sh
storeAttribute("target value", "variable name");
```

* **check**
The "check" command , checks on the checkbox or a radio button. It does the similar action of clicking a button or checkbox in a webpage.


>Syntax
```sh
check("target locator");
```

* **uncheck**
The "uncheck" command , unchecks on the checkbox or a radio button. It does the similar action of clicking a button or checkbox in a webpage for unchecking the element.

>Syntax
```sh
uncheck("target locator");
```

* **assertChecked**
The "assertChecked" command is used to confirm, that the element is checked or not. The test case execution stops if the assert fails.


>Syntax
```sh
assertChecked("target locator");
```

* **assertNotChecked**
The "assertNotChecked" command is used to confirm, that the element is not checked. The test case execution stops if the assert fails.


>Syntax
```sh
assertNotChecked("target locator");
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
assertValue("target locator", "text/value");
```

* **assertEditable**
The "assertEditable" is used to check whether the element is editable. The test execution stops if the assert fails.
>Syntax
```sh
assertEditable("target locator");
```

* **assertNotEditable**
The "assertNotEditable" will check whether the element is not editable. The test execution will stop if the assert fails.
>Syntax
```sh
assertNotEditable("target locator");
```

* **assertNotText**
The "assertNotText" will check, if the text of an element does not contain the provided text.
>Syntax
```sh
assertNotText("target locator", "value/text");
```


* **runScript**
The "runScript" command is used to execute a Javascript code. It creates a new script tag in the current test window and adds the specified text into the body of the command.

>Syntax
```sh	
runScript|("target locator");
```

* **echo**
The "echo" command prints the message specified. It is used for debugging , whether a specific command/value is executed.

>Syntax
```sh
echo("message to print");
```
























# Control Flow





* **if**

The "if" command is the conditional block and terminates with "end". It evaluates the Javascript expression.
>Syntax
```sh
if(condition)
{
statement;
}
```








