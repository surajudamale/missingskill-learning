# JavaScript

### Beginning of JavaScript
- JavaCript is created by **Brendan Eich** in 1995 during his time at Netscape Communication.
- JavaScript is most Loving as well as most hated language for companies.
- JavaScipt orginally named as **Mocha**, later renamed to **LiveScript** and then **JavaScript**.
- The language was thensubmitted for standardization to the **ECMA International Organization**.
- JavaScript is high-level often just-in-time comppiled language.
- JavaScript is one of the core technologies of the WWW (World Wibe Web).

### ECMA Script
**Introduction**
- ECMA Script is trademarked scripting language specification that is defined by ECMA International.
- **ES5** is an abbrivation of **ECMA Script 5** and also known as **ECMA Script 2009**.
- The sixth edition is **ES6** known as **ECMA Script 6** also known as **ECMA Script 2015**.
- ES6 is a major enhancement in JavaScript that allows us to write programs for complex application.

**What is ES5**

- ES5 is ECMA Script 5.
- ES5 is also known as JAvaScript 5.
- ES5 was released in 2009.
- Varios Browser supports ES5.
    - Ex. 
    - Chrome.
    - Firefox 21.
    - Safari 6.
    - Opera 15.
    - Internet Explorer.
- 80% Websites are still run on ES5.

**ES5 and ES6 Difference**.
- In **ES5** we use **var** keyword.
- Where in **ES6** we use **let** and **const** keyword.
- **ES5** has Functional Scope.
- **ES6** has Lexical Scope.

**var keyword**
- **ES5** is a Dynamic type, which gets Hoisted.
- In **ES5** we can use var keyword with ame name it wil just overwrite and allows it to print.
    ```js
    var user = "suraj";     //Declaration and assignment
    console.log(user);      //prints : suraj
    var user = "udamale";
    console.log(user);      //prints : udamale
    ```
**let keyword**
- In **ES6** when we use **let** keyword with same name it throws error Identifier : 'user' has been already declared".
    ```js
    let user = "Suraj";
    let user = "Udamale";
    console.log(user);      //thows error - identifier : 'user' has already declared
    ```
- **let** keyword we declared it only once but assigned it multiple times.
- **let** has only block scope.
- If we use **var** keyword it becomes global variable and gets hoisted.
- If we use **let** keyword it becomes local variable and not get hoisted.

**const keyword**
- in **const** keyword if it gets decalaerd and assign it do only once. **const** did not allow you to assign variable again.
- In JavaScript const value does not overwrite.
- We can't change the location of const varibale.
- but we can change and add new values in it.
    ```js
    const addname = {
        name = "suraj";
    };
    addname.name = "other";        //overwrite 'name = other' in addname.
    addname.city = "pune";      //append city after name.
    console.log(addname);       //prints : {name : 'other', city : 'pune'}
    ```
    => **Difference between var, let and const keyword**
    | var | let | const |
    |-----|-----|-------|
    | Can be Redeclared  | As per ES6 std. it cannot be Redeclared  | As per ES6 std. it cannot be Redeclared |
    | Can be Re-initialized | Can be Re-initialized | Can't be Re-initialized but non-primitive values can be updated |
    | It has a Functional Scope | It has a Lexical Scope | It has a Lexical Scope |
    | ES5 | ES6 | ES6 |
    | Hoisted | It can't be Hoisted | It can't be Hoisted |



### JavaScript Variables
- JavaScript variables are containers for storing data values.
- We use variables to hold values.
- We use variables in expressions.
- JavaScript variables are dynamic type this means that same variable can be used to hold different vata types.

### Identifiers
- All JavaScript variables must be identified with unique names.
- These uniwue names are called identifiers.
- Identifiers can be short names(like x and y) or more decriptive names (age,name.total etc..).

### Classification of Variable Data Types
- JavaScript provides different data type to hold different data types of values.
    - There are two types in JavaScript.
        1. Primitive Datatype
        2. Non-primitive data type

**1. Primitive data type**
- Primitive data type can be hold a specific type of a data.
- There are Five types of primitive data types.
    **1. String**
    - Can be accept string values only..
        ```js
        var name = "Suraj Udamale";
        var name = 100;
        ```
    **2. Number**
    - Can be accept number value only.
        ```js
        var a = 100;
        ```
    **3. Boolean***
    - It can be only True or False
        ```js
        var a = true;
        var b = false;
        ```
    ***4. Undefined**
    - It typically means a variable has been declared but not defined yet.
        ```js
        var user;       //this wll shoe undefined.
        ```
    **5. null**
    - Null means an empty or non-existing value.
        ```js
        var item = null;
        console.log(item);      //this code will print null.
        ```
**2. Non-primitive data type**

1. **Array**
 - An array is a special variable, which can hold more than one value at a time.
 - Arrays can be primitive as well as non-primitive data.
 - If you defined an array in browser but when you check **(typeof array)** internally shows **object**.
    ```js
    var arr1 = [1,2,3,4,5,6,7,8,9];
    var arr2 = ["One", "Two", "Three", "Four", "Five", "Six","Seven"];
    var arr3 = [1, "One", null, true, false];   //It can hold it bcus this is loosely coupled.
    var arr4 = [1, "Two", true, null, [1, 2, 3, 4], {}];    // Primitive + Non-primitive.
    ```

2. **Object**
- In JavaScript there is nothing like Arrays it is also one type of object.
- Object can hold anything.
- Object in JavaScript may be defined as an unordered collection of related data or reference type in type in the type of **"Key : value"** pair.
    ```js
    var person = {
        name : "Suraj",
        dob : "08-03-1995"
    };  //type of person will be object.
    ```
**Note :** Everything in JavaScript is an **Object** means everyting in JavaScript will be **"key : value"** pair.

### Copy by Value and Copy by Reference 
**1. Copy by Value**
- In JavaScript all function arguments are always passed by value. It means that javascript copiesvalue of that variables that you pass to a fucntion into local variable.
- JavaScript has 5 data types which are passed by value : Boolean, Number, String, null and  Undefined. These are primitives.
    ```js
    var x = 10;
    var y = "abc";
    
    //when we assign  these variables to other variable using (=) operator, we copy the value to the new variable. They are copied by value.
    
    var x = 10;
    var y = "abc";
    
    var a = x;
    var b = y;
    
    console.log("x : "x, "y : "y, "a : "a, "b : "b);  //print x : 10, y : abc, a : 10, b : abc
    
    // Both "a" and "x" now conatains "10". Bothe "b" and "y" now contains "abc". They are basically saperate a value are themselves were copied.
    ```
    
**2. Copy by Reference**
 - Javascript has three types that are passed by reference : Array, Function and Object. These are all techinically Object.
 - Variables that are assigned a **Non-primitive** value are given a reference to that value. That reference points to the subject point to the object location in memory. ***The variable don't actually contain the value***.
- In Reference it copies the reference of location from one variable/Object to other.
    - Real life Ex. 
        - Credit/Debit card.
        - Account money is debited or credited from an account not from your debit card is just like ***pass by reference***.
    ```js
    // Objects are created at some location in your computer memory.
        
    var reference = [1];
    var refcopy = reference;//Objects are copied by reference. Reference is copied into refcopy.
        
    // Each varibale now contain reference of the same array. It means changes will be alter in both varibale.
        
    reference.push(2); // push 2 into reference array at location 1st.
    console.log(reference, refcopy);    //prints : [1,2], [1,2] 
        
    // These means we are pointing to the same array.
    ```

    
    
    
    
    
    
