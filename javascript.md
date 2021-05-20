# JavaScript

#### Beginning of JavaScript

- JavaCript is created by **Brendan Eich** in 1995 during his time at Netscape Communication.
- JavaScript is most Loving as well as most hated language for companies.
- JavaScipt orginally named as **Mocha**, later renamed to **LiveScript** and then **JavaScript**.
- The language was thensubmitted for standardization to the **ECMA International Organization**.
- JavaScript is high-level often just-in-time comppiled language.
- JavaScript is one of the core technologies of the WWW (World Wibe Web).

#### ECMA Script

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
  `js var user = "suraj"; //Declaration and assignment console.log(user); //prints : suraj var user = "udamale"; console.log(user); //prints : udamale `
  **let keyword**
- In **ES6** when we use **let** keyword with same name it throws error Identifier : 'user' has been already declared".
  ```js
  let user = 'Suraj';
  let user = 'Udamale';
  console.log(user); //thows error - identifier : 'user' has already declared
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
