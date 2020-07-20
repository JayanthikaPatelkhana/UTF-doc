# Univeral Testing Framework

### About UTF
It is a testing framework, where, we run our scripts for automation testing. It is user friendly and easy to handle. Just by writing a single line command we execute the scripts for testing. It has got many features. 
- uploading an excel sheet, 
- record and play back
- script editor

Let's understand the working of the tool and the commandsby the example script.
>Example
```bh
open("https://opensource-demo.orangehrmlive.com/");
click("css=#divUsername > .form-hint");
type("id=txtUsername", "value=Admin");
type("id=txtPassword", "value=admin123");
click("id=btnLogin");
assertTitle("OrangeHRM");
storeText("css=h1","Dashboard");
echo("$(Dashboard)");
click("css=#menu_time_viewTimeModule > b");
click("id=menu_time_Timesheets");
click("id=employee");
type("id=employee","Jay");
sendKeys("id=employee","${KEY_ENTER}");
```



## UTF commands



* **open**


The "Open" command opens the URL in the current selected browser tab. The open command takes a full URL as input (recommended) or a path relative to the baseurl (outdated).



>Syntax
```sh
open("URL");
```

* **click** 


 "click" command is used to click / select an hyperlink, button, radio option and checkbox option. The below syntax illustrates,how the click command is exceuted.

The target locator will be id, css, textLink, Xpath of an element.
>Syntax
```sh
click("target locator");
```
* **type** 
"type" command is one of the commands, mainly used to type text into the text box and text area fields.


>Syntax
```bh
type("target locator", "value to input");
```



* **sendKeys** 

The sendKeys command simulates keystroke events on the specified element, as though you typed the value key-by-key.Sendkeys can send the ${KEY_ENTER} key event. This means it will kind of work same as user pressing ENTER using the keyboard.

>Syntax
```bh
sendKeys("target locator", ${KEY_ENTER});
```
 

* **mouseOut** 

The "mouseOut" command is used for moving the mouse pointer away from the specified element.

>Syntax
```bh
mouseOut("target locator");
```


* **storeText** 

The "storeText" command is used to store the text value of an element in a variable of the web page for the later use.

>Syntax
```bh	
storeText("target locator","value");
```


* **store** 

 The "store" command is used to store some data for later use.

>Syntax
```bh	
store("text", "variable name");
```


* **storeValue** 

 The "storevalue" command is used to get the value of an element and is stored in a variable for later use.

>Syntax
```bh
storeValue("target locator", "variable name");
```
 

* **storeTitle** 

The "storeTitle' command gets the title of the current page.

>Syntax
```bh
storeTitle("title text", "variable name");
```

* **check**

The "check" command , checks on the checkbox or a radio button. It does the similar action of clicking a button or checkbox in a webpage.


>Syntax
```bh
check("target locator");
```

* **uncheck**
The "uncheck" command , unchecks on the checkbox or a radio button. It does the similar action of clicking a button or checkbox in a webpage for unchecking the element.

>Syntax
```bh
uncheck("target locator");
```

* **assertChecked**

The "assertChecked" command is used to confirm, that the element is checked or not. The test case execution stops if the assert fails.


>Syntax
```bh
assertChecked("target locator");
```

* **assertNotChecked**

The "assertNotChecked" command is used to confirm, that the element is not checked. The test case execution stops if the assert fails.


>Syntax
```bh
assertNotChecked("target locator");
```
* **assertTitle**

The "assertTitle" command is used to confirm, that the title of the current page equals the text provided. The test case execution stops if the assert fails.

>Syntax
```bh
assertTitle("text");
```

* **runScript**

The "runScript" command is used to execute a Javascript code. It creates a new script tag in the current test window and adds the specified text into the body of the command.

>Syntax
```bh	
runScript|("target locator");
```

* **echo**

The "echo" command prints the message specified. It is used for debugging , whether a specific command/value is executed.

>Syntax
```bh
echo("message to print");
```
























# Control Flow





* **if**

The "if" command is the conditional block and terminates with "end". It evaluates the Javascript expression.
>Syntax
```bh
if(condition)
{
statement;
}
```








