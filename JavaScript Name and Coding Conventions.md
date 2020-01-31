# JavaScript Coding Conventions

| Object Name        | Notation   | Length | Plural | Prefix | Suffix | Abbreviation | Char Mask  | Underscores |
|--------------------|------------|--------|--------|--------|--------|--------------|------------|-------------|
| Function name      | PascalCase |     50 | Yes    | No     | Yes    | Yes          | [A-z][0-9] | No          |
| Function arguments | camelCase  |     50 | Yes    | No     | No     | Yes          | [A-z][0-9] | No          |
| Local variables    | camelCase  |     50 | Yes    | No     | No     | Yes          | [A-z][0-9] | No          |
| Constants name     | PascalCase |     50 | Yes    | No     | No     | Yes          | [A-z][0-9] | No          |
| Field name         | camelCase  |     50 | Yes    | No     | No     | Yes          | [A-z][0-9] | No          |


## Coding conventions are style guidelines for programming. They typically cover:

1. Naming and declaration rules for variables and functions.
1. Rules for the use of white space, indentation, and comments.

Coding conventions secure quality:

1. Improves code readability
1. Make code maintenance easier

Always use the same naming convention for all your code. For example:
1. Do use camelCasing for variable and function arguments names;
2. Do use PascalCasing for function names and global variable;
3. Constants (like PI) written in UPPERCASE;
4. Do not use under_scores in variable, constants, function arguments or function names;
5. Do not use hyphens in JavaScript names.


### Naming Conventions

Do use PascalCasing for function names:

```javascript
    function HelloWorld()	
    {
    }
```

Do use camelCasing for function arguments and local variables: 

```javascript
    function Hello(isShow)	
    {
    }

    firstName = "John";
    lastName = "Doe";
    
    price = 19.90;
    discount = 0.10;
    
    fullPrice = price * 100 / discount;
```

*Note: Don't start names with a $ sign. It will put you in conflict with many JavaScript library names.*

### Spaces Around Operators

Always put spaces around operators ( = + / * ), and after commas:

Examples:

	var x = y + z;
	var values = ["Volvo", "Saab", "Fiat"];

### Code Indentation

Always use 4 spaces for indentation of code blocks:

Functions:

```javascript
    function ToCelsius(fahrenheit) 
    {
         return (5/9) * (fahrenheit-32);
    }
```

*Note: Do not use tabs (tabulators) for indentation. Text editors interpret tabs differently.* 

### Statement Rules

*General rules for simple statements: Always end simple statement with a semicolon.*

Examples:

```javascript	
    var values = ["Volvo", "Saab", "Fiat"];
    
    var person = {
        firstName: "John",
        lastName: "Doe",
        age: 50,
        eyeColor: "blue"
    };
```

### General rules for complex (compound) statements:

1. Put the opening bracket at the end of the first line.
2. Use one space before the opening bracket.
3. Put the closing bracket on a new line, without leading spaces.
4. Do not end complex statement with a semicolon.

Functions:

```javascript
    function toCelsius(fahrenheit) {
         return (5/9) * (fahrenheit-32);
    }
```

Loops:

```javascript
	for (i = 0; i < 5; i++) {
	    x += i;
	}
```

Conditionals:

```javascript
    if (time < 20) {
        greeting = "Good day";
    } else {
        greeting = "Good evening";
    }
```


### Object Rules

General rules for object definitions:

1. Place the opening bracket on the same line as the object name.
2. Use colon plus one space between each property and it's value.
3. Use quotes around string values, not around numeric values.
4. Do not add a comma after the last property-value pair.
5. Place the closing bracket, on a new line, without leading spaces.
6. Always end  an object definition with a semicolon.

Example:

```javascript
    var person = {
        firstName: "John",
        lastName: "Doe",
        age: 50,
        eyeColor: "blue"
    };
```

Short objects can be written compressed, on one line, like this:

```javascript
    var person = {firstName:"John", lastName:"Doe", age:50, eyeColor:"blue"};
```

### Line Length < 80

For readability, avoid lines longer than 80 characters. If a JavaScript statement does not fit on one line, the best place to break it, is after an operator or a comma.

Example:

```javascript
    document.getElementById("demo").innerHTML = "Hello World.";
```

### Loading JavaScript in HTML

Use simple syntax for loading external scripts (the type attribute is not necessary):

```html	
	<script src="myscript.js">
```

### Accessing HTML Elements

A consequence of using "untidy" HTML styles, might result in JavaScript errors. These two JavaScript statements will produce different results:

```javascript
    var obj = getElementById("Demo")
    var obj = getElementById("demo")
```

*If possible, use it naming convention (as JavaScript) in HTML.* 

### File Extensions

1. HTML files should have a .html extension (not .htm); 
2. CSS files should have a .css extension;
3. JavaScript files should have a .js extension.

## Offical Reference

1. [Google JavaScript Style Guide](http://google-styleguide.googlecode.com/svn/trunk/javascriptguide.xml)
2. [JavaScript Style Guide and Coding Conventions](http://www.w3schools.com/js/js_conventions.asp) 
