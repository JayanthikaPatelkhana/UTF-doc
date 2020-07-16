# Univeral Testing Framework
## UTF Sidescript commands

### About UTF
It is a testing framework, where, we run our scripts for automation testing. It is user friendly and easy to handle. Just by writing a single line command we execute the scripts for testing. It has got many features. 
- uploading an excel sheet, 
- record and play back
- script editor

## UTF commands
* **Open**


The "Open" command opens the URL in the current selected browser tab. The open command takes a full URL as input (recommended) or a path relative to the baseurl (outdated).


In syntax example, the "open" command navigates us the URL "http://localhost:8087/index.html". The "open" command is the first step to start an execution.
>Syntax
```sh
open|http://localhost:8087/index.html
echo|opens url
```

* **Click** 


 "Click" command is used to click / select an hyperlink, button, radio option and checkbox option. The below syntax illustrates,how the click command is exceuted.


 In syntax example, first we are navigating to the web site "http://localhost:8087/index.html" using open command and performing an action to click  on the element "Add New Test Suite" by using the "Click" command. Here we are specifying the target of the element by its "id".

In few cases we use Xpath, CSS, LinkText to identify the target of an element.
>Syntax
```sh
open|http://localhost:8087/index.html
click|id=button.btn btn-primary|Add New Test Suite
```
* **Type** 


 "Type" command is one of the commands, mainly used to type text into the text box and text area fields.


 In the syntax example, open command, opens the url "http://localhost:8087/index.html" and the "Type" command, types the value "name" in the specified input field which is located with the target "id=name".

>Syntax

```bh
open|http://localhost:8087/index.html
Type|id=name|name
```



* **Sendkeys** 

The sendKeys command simulates keystroke events on the specified element, as though you typed the value key-by-key.Sendkeys can send the ${KEY_ENTER} key event. This means it will kind of work same as user pressing ENTER using the keyboard.


In this syntax example, open command, opens the given URL and in the types the value in the target(id=lst-ib) element and using the sendkeys command it does the action of hitting the enter key to start the search.
>Syntax
```bh
open|http://localhost:8087/index.html	
Type|id=name|name
sendkeys|id=name|${KEY_ENTER}
```
 

* **mouseOut** 

The "mouseOut" command is used for moving the mouse pointer away from the specified element.

In this syntax example, the cursor pointer is moved away from the web element using the "mouseOut" command.
>Syntax
```bh
open|http://localhost:8087/index.html	
mouseOver|id=button.btn btn-primary sumit-btn	
mouseOut|id=button.btn btn-primary sumit-btn
```


* **storeText** 

The "storeText" command is used to store the text value of an element in a variable of the web page for the later use.

In the syntax example, the text value of the id=button.btn btn-primary is stored in the variable "Y". In the later use, we are echoing variable "Y".
>Syntax
```bh
open|http://localhost:8087/index.html	
storeText|id=button.btn btn-primary|Y
echo|{Y}
```


* **Store** 

 The "store" command is used to store some data for later use.

 In the syntax example, using store command, we are storing the value of "name" in variable "myvar" and in later it is typed in the target element "id=name"
>Syntax
```bh
open|http://localhost:8087/index.html/	
store|name|myvar
echo|${myvar}	
type|id=name|${myvar}
```


* **storeValue** 

 The "storevalue" command is used to get the value of an element and is stored in a variable for later use.

In the syntax example, using the storeValue command , the value of the element is stored in the variable "Y".
>Syntax
```bh
open|http://localhost:8087/index.html	
storeValue|id=button.btn btn-primary|Y
echo|Extracted Text = ${Y}
```
 

* **storeTitle** 

The "storeTitle' command gets the title of the current page.

In the syntax example, using the storeTitle command we are the storing the title of the current page and in later step echoing the title.
>Syntax
```bh
open|http://localhost:8087/index.html	
storeTitle|Universal Testing Framework|mytitle
echo|The title of my page is ${mytitle}
```

* **check**

The "check" command , checks on the checkbox or a radio button. It does the similar action of clicking a button or checkbox in a webpage.

In the syntax example, using the check command a macro checkbox is clicked and checked.

>Syntax
```bh
open|/demo.html
check|id=macro
pause|2500
uncheck|id=macro
```

* **uncheck**
The "uncheck" command , unchecks on the checkbox or a radio button. It does the similar action of clicking a button or checkbox in a webpage for unchecking the element.

In the syntax example, using the uncheck command a macro checkbox is clicked and unchecked.
>Syntax
```bh
open|/demo.html
check|id=macro
pause|2500
uncheck|id=macro
```

* **assertChecked**

The "assertChecked" command is used to confirm, that the element is checked or not. The test case execution stops if the assert fails.

In the syntax example, using assertChecked command, you are asseting whether the element macro is checked or not

>Syntax
```bh
open|/demo.html
check|id=macro
pause|2500
assertChecked|id=macro
```

* **assertNotChecked**

The "assertNotChecked" command is used to confirm, that the element is not checked. The test case execution stops if the assert fails.

In the syntax example, using assertNotChecked command, you are asserting whether the element macro is not checked.

>Syntax
```bh
open|/demo.html
uncheck|id=macro
pause|2500
assertNotChecked|id=macro
```
* **assertTitle**

The "assertTitle" command is used to confirm, that the title of the current page equals the text provided. The test case execution stops if the assert fails.

In the syntax example, using assertTitle command, you are asserting whether the text provided is same as the title of the current page.
>Syntax
```bh
open|http://localhost:8087/index.html	
storeTitle|Universal Testing Framework|mytitle
asserTitle|${mytitle}
```

* **runScript**

The "runScript" command is used to execute a Javascript code. It creates a new script tag in the current test window and adds the specified text into the body of the command.

In the syntax example, the run script command executes the javascript code snippet of alert and creates an alert in the current test window.
>Syntax
```bh
open|http://localhost:8087/index.html	
run script|alert("Hello tester")
```

* **echo**

The "echo" command prints the message specified. It is used for debugging , whether a specific command/value is executed.

In the syntax example, the echo command prints the value in ${myTitle}, if the storeTitle command is executed.
>Syntax
```bh
open|http://localhost:8087/index.html	
storeTitle|Universal Testing Framework|mytitle
echo|The title of my page is ${mytitle}
```

* **if**

The "if" command is the conditional block and terminates with "end". It evaluates the Javascript expression.
>Syntax
```bh
oopen|http://localhost:8087/index.html	
excuteScript|return"a"|myVar
if|${myVar}==a
excuteScript|return "a"
end
assert|output|a
```








