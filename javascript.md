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

**1. Array**
 - An array is a special variable, which can hold more than one value at a time.
 - Arrays can be primitive as well as non-primitive data.
 - If you defined an array in browser but when you check **(typeof array)** internally shows **object**.
    ```js
    var arr1 = [1,2,3,4,5,6,7,8,9];
    var arr2 = ["One", "Two", "Three", "Four", "Five", "Six","Seven"];
    var arr3 = [1, "One", null, true, false];   //It can hold it bcus this is loosely coupled.
    var arr4 = [1, "Two", true, null, [1, 2, 3, 4], {}];    // Primitive + Non-primitive.
    ```
**2. Object**
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
    
    console.log("x: ", x, " y: ", y, " a: ", a, " b: ",b); //print x : 10, y : abc, a : 10, b : abc
    
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
### Operators in JavaScript
- In these we learn about some basic operators and their functions.
    1. **Arithmatic Operator**
        - **+** : Addition
        - **-** : Subtraction
        -  **.*** : Multiplication
        - **/** : Division
        - **%** : Modulus (Division Reminder)

    2. **Logical Operator**
        - **&&** :  Logical AND
        - **||** : Logical OR
        - **!** : Logical NOT
    
    | **X** | **Y** | **AND** | **OR** |
    |-------|-------|--------|--------|
    | 0 (false) | 0 (false) | 0 (false) | 0 (false)|
    | 0 (false) | 1 (true)  | 0 (false) | 1 (true) |   
    | 1 (true)  | 0 (false) | 0 (false) | 1 (true) |
    | 1 (true)  | 1 (true)  | 1 (true)  | 1 (true) |

    3. **comparison operator**
        - **==** : Equal to
        - **===** : Equal Value or Equal Type
        - **!=** : Not Equal
        - **>** : Greater than
        - **<** : Less than
        - **>=** : Greater than equal to
        - **<=** : Less than equal to
    - There is bug in only Addition oerator **(+)**.
    - We want to be very carefull when we use **+** operator, we typecast the values before we use addition **( + )** operator.
        ```js
        var a = "100"; //typeof a will be string.
        var a = +"100"; // typeof a will be number.
        ```
- **SomeConcatination Example which are due to bug in (+) addition operator.**
    
    1. number + null    =   number
        ```js
        1 + null
        output: 1    //number
        ```
    2. number + boolean =   number
        ```js
        1 + true
        output: 2    //number
        ```
    3. number + undefined   =   NaN
        ```js
        1 + undefined
        output : NaN    //NaN
        ```
    4. number + string  =   string
        ```js
        1 + "11"
        output : "111"  //string
        ```
    5. number + array   =   string
        ```js
        1 + [1,2,3]
        output : "11,2,3"   //string
        ```
    6. number + object  =   string
        ```js
        1 + {}
        output : "1[object Object]" //string
        ```
    7. null + null  =   0
        ```js
        null + null
        output : 0  //number
        ```
    8. undefined + undefined    =   NaN
        ```js
        undefined + undefined
        output : NaN    //NaN
        ```
    9. undefined + null =   NaN
        ```js
        undefined + null
        output : NaN    //NaN
        ```
    10. boolean + null  =   number
        ```js
        true + null    
        output : 1  //number
        ```
    11. boolean + array =   string
        ```js
        true + []
        output : "true" //string "bcus non-primitives converts into string by concatination"
        ```
    12. array + array   =   string
        ```js
        [1,2,3] + [1,2,3]
        output : "1,2,31,2,3"   //string
        ```

#### == and === Difference
- **==** is loose comparison
    - **==** operator compaired number with a string with numerical literals it allows and return true flag.
        ```js
        100 == "100" //true, bcus string converts into number and only checks the value not type.
        0 == false    // true, because false is equivalant of 0.
        ```
- **===** is strict comparison
    - bcus it just not check the value but also checks the type of variable, if two variables are not same type it simply returns false   
        ```js
        100 === "100"   //false, because both operands are not same type
        0 == false  // //false, because both operands are not same type
        ```
#### Tech Debt in JavaScript
- Tech Debt in Javascript is a bug which never gets salved. There are various type of tech debts.
    - Ex. **null, +, ==**
    

#### Boolean Check in JavaScript
- In JavaScript there are some things like **truthy value** and **falsy value**.
- primitives are **truthy values** as well as falsy values
- Non-primitives are always **truthy values**.
- Empty objects and arrays are always **truthy in JS.
- The moment you add negation **( ! )** it becomes the boolean value and reverese the boolean result of the operands or condtion.
    ```js
    var name = "suraj"; 
    Boolean(name)   // Truthy value
    
    var name = "";      
    Boolean(name)   //blank string is Falsy value
    
    var marks = 0;  
    Boolean(marks)  // Falsy value
    //**anything which is non zero is Truthy value.
    
    var one = null;   
    Boolean(marks)  // Falsy value
    
    var one = !null;
    Boolean(marks)  // Truthy value
    ```
    ```js
    //Non-primitives are always truthy values.
    Boolean({})
    => true     // Truthy
    
    Boolean(!{})
    => false     // Falsy
    
    Boolean([])
    => true     // Truthy
    
    Boolean(![])
    => false     // Falsy
    ```

#### Hoisting in JavaScript
- In Javascript It doesn't matter in functional scope where you define the variable it always get hoisted on top.
- In these variable declaration gets Hoisted, assignment doesen't get hoisted.
- Variable get hoisted at the functional scope.
    ```js
    var a = 100;
    
    function hoist(){
        a = 10; //assign to a global var a
        var b = 100;
    };
    hoist();
    
    console.log(a); //Accissible as a global variable hoist() function.
    => prints : 10
    
    console.log(b);
    // Uncaught ReferenceError: b is not defined
    ```
    ```js
    //extra
    var a = 100;

    function hoist(){
        a = 200;    //assigned to global var a;
        var b = 300;
        console.log(a,b);
    };

    hoist();
    => prints : 200 300

    console.log(a);
    => prints : 200

    console.log(b);
    => Prints : Uncaught ReferenceError: b is not defined
    ```
    
#### Local Scope and Global scope in JavaScript
- In JavaScript there has two scope.
    1. Global Scope
    2. Local Scope
- A **Global variable** has a global scope which means it can be define anywhere in your JavaScript code.
- A **local variable** will be visible only within a function where it is defined. Function paranthisys are always local to that function.
    ```js
    var one = "present"; // varibale one created in global scope.
    
    function foo(){
        var one = "future"; //var doo created in local scope of function "foo.
        console.log(doo);   // print : future   // nearest variable present in local scope.
    }
    foo();
    
    console.log(one);   // print : present  // varibale one of global scope
    ```
    
### JacaScript Function
- In JavaScript Function is used to write the code within a block,  basically designed to perform a perticular task.
- In JavaScript Function is invoked when it gets called otherwise not gets called.
- Function has a Functional scope.
- Function is a container which stores all premitive as well as non pritive values.
- According to ES5 function gets hoisted.
    ```js
    function myFun(val1, val2){
        return val1 * val2;
    }
    var result = myFun(20,2);
    console.log(result);    // print : 40
    ```
    
#### First class Citizen in JavaScript
- In Javascript Function are called as **First class citizen** it means that we can do anything with function.
- Function can be perform in any way.
- We can assign function to a variable.
- Function can be return from another function.
- Function can be **key : value** pair.
- Function can be declare as well assign to a variable.
    ```js
    const print = function(value) {
        console.log("value : ", value); //function exression assign to variable.
    };
    
    const task = function(param) {
        const a = "200";
        const b = a * 5;
    =>  param(b);   //param is pointing to print function means referenece to a function
        //we add a check condition to know where param is a function or not
        param && (typeof param === "function" && param(b)
    };
    task(print);
    ```

#### Function Hoisting
- In this case Function assignent doesn't get hoisted only function declaration get hoisted.
    ```js
    user("present");
    var user = function(param) {
        console.log(param);
    };
    // It will throw error user is not a function.
    ```
    
    ```js
     var user = function(param) {
        console.log(param);
    };
    user("present");
    ```
    
#### Function Declaration and Function Exrpession
- **Function Declaration(Normal Function)**
    - A Function Declaration defines a named function variable.
    - Function declaration must be begin with "Function".
    - Function gets Hoisted means function can be called before it is defined.
        ```js
        function firstFunction(){
            console.log("present"); //print : present
        }
        firstFunction(); //Function call
        ```
        - In this function call is in excecution phase not returning any value. It is a function declaration.
        
- **Function Expression(Assignment)**
    - Main difference between **Function Declaration** and ** Function Expression** is the **Function name**,
    - Function is basically assign to a variable.
    - It doesn't get hoisted, it means it can't be called before it is defined.
    - It is a **Anonymous Function** means **un-named** function.
        ```js
       // # Anonymous Function Expression
        
        var namedFun = function(a,b) {
            console.log("present", a, b);   //print : present hello 100
        }
        namedFun("hello", 100); // function call with 2 parameters
        ```



- In JavaScript Function Declaration are rarelly used, because function is  First Class Citizen so it can do all things in JavaScript.
- var keyword gets hoisted, let and const not get hoisted.


#### Higher Order Function
- In JavaScript Function is a **First Class Citizen** and function is also an **Object**.
- In JS function can be assigned to a variable or passed as a variable.
- **Higher Order Function** is a function that recieves a function as a parameter and returns the same or another function.
    

- We can : 
        - Store them as a Variable.
        - Use them as a Array.
        - Assign them as an Object.
        - Return them from another Function.
    - Thats why JavaScript Function is **First class Citizen** it can do all the things.

    ```js
    // With Higher Order Function
    function fnOne(arg) {
        let name = "Suraj";

        function shName(arg) {
            console.log("name : ", name, arg);  // print : suraj 100
        }
        return shName(arg);
    }
    fnOne(100); // function call with 1 parameter
    ```

#### IIFE (Immedialtelly Invoked Function Expression)
- **IIFE** stands for **Immedialtelly Invoked Function Expression** also called as self Excecuting Function.
- IIFE only called once.
- Function is called right after it is defined.
- IIFE can be called as soon as it is defined. 
    ```js
    // some example with IIFE and its scope
    
    (function () {
    var name = "present"; //var name is not accissible outside the scope.
    })();
    console.log(name); //throws error : name is not defined.
    // The var name within the exression can't be accessed from outside
    ```
    ```js
    // function expression assigned to a const result.
    
    const result = (function() {
        var name = "present";
        return name;
    })();   //Immidialtely invoked the function
    console.log(result);    // prints : present       
    ```
    ```js
    // Immediate calling function and passing argument as function.
    function sqFun(n) {
        return n * n;   //return 9 to a result
    }
    
    (function(paramFun) { //paramFun => function
        const result = paramFun(sqFun);//call inline function with sqfun function as a parameter
        console.log("Result : ", result);//print : 25
    })(function(cb) {  //cb is reference to sqFun function
        return cb(5);   //calling sbFun function with param 5.
    })
    ```
    
#### Inline Function
- Function which is defined within a function and accessible ouside the function.
- Inline function is also a higher order function.
- In JavaScript inline function is Anonymous function which is assign to a variable.
- It is a callable function.
    ```js
    (function(data, paramFun) {  
        const main = data +30;  //20 + 30 = 59
        paramFun(function(final) {
            final(main);
        });
    })(29, function(cbr) {
        cbr(function(value) {
            console.log("value : ", value);
        })
    });
    ```

**Explanation** 
- This is basically a IIFE Function.
- It is taking two parameter. Recives 1st as a **data = number** and 2nd as a **paramFun = function**.
- so main = 59.
- when it is excecuting there is another function which is passed in a **paramFun** function and taking parameter as **final**.
- cdr is taking another function which is **inline function**.
- **final** is pointing to **inline function**.
- so value will be 59.

#### Arrow Function in ES6
- Arrow function is introduced in ES6.
- It is basically salve the problems which is related to "this" keyword.
- Arrow Function is used for shorter the function.
- Example.
    ```js
    // const arrow = function() { //function keyword is used here
    // let item = [1,2,3]
    // return item;
    // }
       
    const arrow = () => {    //here we uses the arrow 
        let item = [1,2,3]
        return item;
    }
    const value = arrow();
    console.log("item", value);
    ```
### Object in JavaScript
#### Introduction
- In JS Everything is an Object so function is also an Object.
- Object is also hold a function.
- In object when we write function it is always expression(key : value pair) key should be always string and value can be anything.
- To define object inside function insteed of  (**=**) operator (**:**) colon will get used.
- Object can hold function bcus it is First class citizen it means it can take function and return a function.

#### How function is Object
- We know all about Object and how object related to everything in JavaScript, but we understand that how object is also hold a function.
- When you write a function inside object you use a Expression(Key : Value) Pair just say
    - **Key** : is someone (**Key** should be alwyas be **string**)
    - **Value** : function(){...}; Anonymous function (Value can be anything including function)
- Object can hold Function
    - In this function can take function and return a function.

### Prototype in JavaScript
- Javascript is a prototype based language.
- Prototype of an object is one type of object.
- We can also attach properties and methods to prototype object.
- In Function prototype it use to create a object of similar type.
- In initialized wirh **new** keyword. Just like **new Object() or {}**.
- **Properties** of prototype object can be refered using **this** keyword.
    
#### Build in prototype in JavaScript.
- **Object Prototype**
    - When dot (**.**) is used in JavaScript engine converts it into Object prototype which make methods on which key can operate   
- **Arrow Prototype**
    - Whenever dot(**.**) used in array JavaScript intarnally converts it into array prototype which has all methods
    - It holds several build in methods like **sort, push, pop, join, split, map, join, keys, alice, forEach, indexOf, filter, concat etc...
- **Function Prototype**
    - To create object of similar type.
    - Initialize using new keyword.
    - properties are refered using **this** keyword.
- **String Prototype**
    - it overrides **toString()** method. 
- **Boolean Prototype**
    - the **valueOf()** method returns the primitive value of boolean object
- **Number Prototyp**
- **Math Prototype**
**note : -** Except **null** and **undefined** all primitives have there prototype.

### Object Lookup
- here we can do object lookup using two ways : - 
    1. Dot notation
    2. Bracket notation
1. Dot notation
    ```js
    let obj = {
        cat : "meow",
        dog : "woof"
    };
    let sound1 = obj.cat;
    console.log(sound); //prints : meow
    
    let sound2 = obj.dog;
    console.log(sound); //prints : woof
    ```
- this is the example which is used to access the properties of an object by specifying the name of an object and when you andd **dot (.)** you can access the properties.
- **syntex : objectName.propertyName**
2. Bracket notation
     ```js
    let obj = {
        cat : "meow",
        dog : "woof"
    };
    let sound1 = obj["cat"];
    console.log(sound); //prints : meow
    
    let sound2 = obj["dog"];
    console.log(sound); //prints : woof
    ```
- this is the example of bracket notation. You can access properties on an **object** by specifying the name of object followed by the specific **property name in bracket**.

### JSON
    
    
    
    
    
    
    
    
    
    
    
    
    
