#Front-end Job Interview Questions with my answers

**The answers are mine or found. I don't claim to know them perfectly, just that I researched them.**

This file contains a number of front-end interview questions that can be used when vetting potential candidates. It is by no means recommended to use every single question here on the same candidate (that would take hours). Choosing a few items from this list should help you vet the intended skills you require.

**Note:** Keep in mind that many of these questions are open-ended and could lead to interesting discussions that tell you more about the person's capabilities than a straight answer would.

## Table of Contents

  1. [General Questions](#general-questions)
  1. [HTML Questions](#html-questions)
  1. [CSS Questions](#css-questions)
  1. [JS Questions](#js-questions)
  1. [Testing Questions](#testing-questions)
  1. [Performance Questions](#performance-questions)
  1. [Network Questions](#network-questions)
  1. [Coding Questions](#coding-questions)
  1. [Fun Questions](#fun-questions)

## Getting Involved

  1. [Contributors](#contributors)
  1. [How to Contribute](https://github.com/h5bp/Front-end-Developer-Interview-Questions/blob/master/CONTRIBUTING.md)
  1. [License](https://github.com/h5bp/Front-end-Developer-Interview-Questions/blob/master/LICENSE.md)

#### General Questions:

* What did you learn yesterday/this week?
    * _I learned that $.data() receives either camelCase or dashed properties._
* What excites or interests you about coding?
* What is a recent technical challenge you experienced and how did you solve it?
* What UI, Security, Performance, SEO, Maintainability or Technology considerations do you make while building a web application or site?
* Talk about your preferred development environment.
    * _I like the IDEs from JetBrains_
* Which version control systems are you familiar with?
    * _Although I worked 4 years with SVN, I prefer git._
* Can you describe your workflow when you create a web page?
* If you have 5 different stylesheets, how would you best integrate them into the site?
    * _I would most likely use SASS or other CSS compiler and I would import them into one file and I would minify that file._
* Can you describe the difference between progressive enhancement and graceful degradation?
* How would you optimize a website's assets/resources?
    * _As I said two questions up, I would compile all my css into one css file, I would put all my small images into one sprite and I would optimize it for the web, I would minify the js, css._
* How many resources will a browser download from a given domain at a time?
  * What are the exceptions?
* Name 3 ways to decrease page load (perceived or actual load time).
* If you jumped on a project and they used tabs and you used spaces, what would you do?
* Describe how you would create a simple slideshow page.
* If you could master one technology this year, what would it be?
    * _React_
* Explain the importance of standards and standards bodies.
* What is Flash of Unstyled Content? How do you avoid FOUC?
    * _When a site appears, for a moment, with text without styling, and after that it applies the styling._
* Explain what ARIA and screenreaders are, and how to make a website accessible.
* Explain some of the pros and cons for CSS animations versus JavaScript animations.
* What does CORS stand for and what issue does it address?

#### HTML Questions:

* What does a `doctype` do?
    * _It's a way to tell the browser what type of document do you use. If it's omitted, browsers tend to guess and you may end up with some issues. It's also used for validating the document according to the mentioned doctype._
    * _example `<!DOCTYPE html>`_
* What's the difference between full standards mode, almost standards mode and quirks mode?
    * _As far as I know, at first developers wrote two version of a page: one for IE and another for Netscape. After the introduction of web standards they couldn't enforce those standards because they could brake a lot of pages, so the browsers implemented quirks mode (when a browsers emulates the another browsers to support that page), almost standard mode (when browsers emulate only some of the quirks) and full standards (where the page is interpreted as the developer wanted it)._
* What's the difference between HTML and XHTML?
    * _In HTML things are way more permissive over the correctness of the writing. Start tags don't necessarily have to end, attributes don't have to have quotes, only <br/>, <img/> and <link/> are permitted as self enclosed._
* Are there any problems with serving pages as `application/xhtml+xml`?
* How do you serve a page with content in multiple languages?
* What kind of things must you be wary of when design or developing for multilingual sites?
* What are `data-` attributes good for?
    * _They are good for storing necessary data and at the same time to be valid HTML._
* Consider HTML5 as an open web platform. What are the building blocks of HTML5?
    * _section, article, video, canvas, audio, new form elements (email, telephone), SVG, web workers_
* Describe the difference between a `cookie`, `sessionStorage` and `localStorage`.
* Describe the difference between `<script>`, `<script async>` and `<script defer>`.
* Why is it generally a good idea to position CSS `<link>`s between `<head></head>` and JS `<script>`s just before `</body>`? Do you know any exceptions?
* What is progressive rendering?
* Have you used different HTML templating languages before?
    * _Yes, I used underscore templates and handlebars templates._

#### CSS Questions:

* What is the difference between classes and IDs in CSS?
* What's the difference between "resetting" and "normalizing" CSS? Which would you choose, and why?
* Describe Floats and how they work.
* Describe z-index and how stacking context is formed.
    * _In DOM you have a tree and every element is a leaf/branch. According to their position, they also are more up front or in the back and they receive an index. The z-index property overrides that hierarchy, but it also has to have `position: relative`._ 
* Describe BFC(Block Formatting Context) and how it works.
* What are the various clearing techniques and which is appropriate for what context?
* Explain CSS sprites, and how you would implement them on a page or site.
    * _CSS sprites are a composite of multiple images. Although you can create sprites manually, I would use grunt (or a similar tool) to automate the process and instead of using coordinates for that image, I would use a unique name._
* What are your favourite image replacement techniques and which do you use when?
* How would you approach fixing browser-specific styling issues?
    * _I would start with a normalizing css._
* How do you serve your pages for feature-constrained browsers?
  * What techniques/processes do you use?
* What are the different ways to visually hide content (and make it available only for screen readers)?
* Have you ever used a grid system, and if so, what do you prefer?
    * _I've used the grid system from Foundation and Bootstrap. I don't have a favourite because they both are very similar, but I worked more with Foundation._
* Have you used or implemented media queries or mobile specific layouts/CSS?
    * _Yes. `@media (max-device-width: 480px) {}`_
* Are you familiar with styling SVG?
    * _No. What I know about SVG is that it a vectorial way to create images and it has XML syntax._
* How do you optimize your webpages for print?
    * _I wrote an article about this. [http://codethatcounts.com/making-your-page-printable/]_
* What are some of the "gotchas" for writing efficient CSS?
    * _One part of the answer I've given three questions down._
* What are the advantages/disadvantages of using CSS preprocessors?
  * Describe what you like and dislike about the CSS preprocessors you have used.
    * _Preprocessors help you organize your css code better. You can have multiple files and after compilation have only one. Also for writing inside those files it's easier to write because you can add children's properties inside a parent._
    * ```scss
        /* SCSS */
        .parent {
            color: blue;
      
            .child {
                color: red;
            }
        }
  
    * ```css
        /* CSS */
        .parent {
            color: blue;
        }
        .parent .child {
            color: red;
        }
    
* How would you implement a web design comp that uses non-standard fonts?
* Explain how a browser determines what elements match a CSS selector.
    * _Let's say we have `#test .class-test ul li`. The CSS engine will find at first all the li's, then all the ul's that have li, then the elements that have a class-test that have an ul and then the id test that has a class-test. That's why it's more efficient to have a unique selector because the engine will find it much faster._
* Describe pseudo-elements and discuss what they are used for.
    * _`::after, ::before, ::first-letter, ::first-line` etc. You will find them sometimes with double colons (::) instead of just one, because this is CSS3 attempt to distinguish between pseudo-classes and pseudo-elements. Most browsers support both values._
    * _`::after, ::before` are used to match a virtual child of the selected elements. It is typically  used to add cosmetic content to an element by using the content CSS property._
* Explain your understanding of the box model and how you would tell the browser in CSS to render your layout in different box models.
    * _Every element on a page is a rectangular. The box model refers to the way that rectangular is formed and how its size is calculated._
    * _What gives a div the ability to implement the box model is the css property `box-sizing`. It can have three values:_ 
        * _`content-box`: the default value. width = content_
        * _`border-box`: width = content + padding + border_
        * _`padding-box`: width = content + padding_
* What does ```* { box-sizing: border-box; }``` do? What are its advantages?
    * _I know that it was the default value of IE and the most popular option because it makes it easier to create responsive layouts._
* List as many values for the display property that you can remember.
    * _none, block, inline-block, inline, table, table-cell, flex_
* What's the difference between inline and inline-block?
    * _Inline can't have width and height set, but inline-block can._
* What's the difference between a relative, fixed, absolute and statically positioned element?
    * _Static is the default value. The left, top etc. values don't work._
    * _The fixed element is positioned fixed regarding to the viewport. Even when the user scrolls the page, the element remain in the same spot._
    * _Relative is used if you like the static position but you want it changed a little._
    * _Absolute is used to position an element to a specified position according to the closest parent that has the position set to fixed or absolute, or the original container._
* The 'C' in CSS stands for Cascading.  How is priority determined in assigning styles (a few examples)?  How can you use this system to your advantage?
    * _The CSS priority (or specificity) from down to up:_
        * _type selector: `div, h1`, pseudo-elements: `:before`_
        * _class selector: `.class-example`, attribute selector: `[type="radio"]`, pseudo-classes: `:hover`_
        * _id selector: `#myId`_
        * _inline CSS_
        * _the `!important` exception_
* What existing CSS frameworks have you used locally, or in production? How would you change/improve them?
    * _Foundation Zurb with SASS._
* Have you played around with the new CSS Flexbox or Grid specs?
    * _No, I just read about it. I know they are useful for responsive design._
* How is responsive design different from adaptive design?
    * _Responsive is when elements are moved and changed according to the screen in real time, and adaptive design is when they change on specific sizes (they snap)._
* Have you ever worked with retina graphics? If so, when and what techniques did you use?
* Is there any reason you'd want to use `translate()` instead of *absolute positioning*, or vice-versa? And why?

##### My CSS Questions
* Types of positions and how they affect the flow of the page

#### JS Questions:

* Explain event delegation
    * _Event delegation is based on event bubbling. Let's say that you have a div with a span inside. You add an event listener on the div and you click the span. The click event happens on the span and then notifies his parent and bubbles up the event. That is event bubbling. In combination with the `target` property of the event, you can use event delegation._
    * _Event delegation is useful because you can have only one event listener and you can find out if a specific element inside your page was clicked. This is also useful if you add elements dynamically and you can have only one event listener on the parent._
* Explain how `this` works in JavaScript !!!__complete this answer__!!!
    * _`this` is changed based on how a function is called._
    * _The this object is bound at runtime based on the context in which a function is executed:_
      * _when used inside global functions,this is equal to window in nostrict mode and undefined in strict mode._
      * _whereas this is equal to the object when called as an object method._
      * _as a constructor_
      * _call and apply_
      * _bound functions_
      * _as dom event handler_
* Explain how prototypal inheritance works !!!__complete this answer__!!!
    * _When an object rabbit inherits from another object animal, in JavaScript that means that there is a special property rabbit.`__proto__ = animal`._

        ![alt](http://javascript.info/files/tutorial/intro/object/prototype.png)
    * _When a rabbit property is accessed, and the interpreter can’t find it in rabbit, it follows the `__proto__` link and searches in animal._
    * _It's not a good practice to modify the `__proto__` property because in Opera (I don't know if it still applies) and IE < 9 you don't have access to this property. It's also good to know that the `__proto__` property was implemented by Firefox/Chrome without being standardized first. Instead you should use `Object.create`_
    ```javascript
        var animal = { eats: true };
        rabbit = Object.create(animal);
        alert(rabbit.eats); // true
    ```
    * _Another way to the above:_
    ```javascript
    var animal = { eats: true };
    
    function Rabbit(name) { 
      this.name = name
    }
    
    Rabbit.prototype = animal;
    
    var rabbit = new Rabbit('John');
    
    alert( rabbit.eats );// true, because rabbit.__proto__ == animal
    ```
    * _More info [here](http://javascript.info/tutorial/inheritance)_
* What do you think of AMD vs CommonJS?
    * _CommonJS is a project to define a common API and ecosystem for JavaScript. One part of CommonJS is the Module specification. Node.js and RingoJS are server-side JavaScript runtimes, and yes, both of them implement modules based on the CommonJS Module spec._
    * _AMD (Asynchronous Module Definition) is another specification for modules. RequireJS is probably the most popular implementation of AMD. One major difference from CommonJS is that AMD specifies that modules are loaded asynchronously - that means modules are loaded in parallel, as opposed to blocking the execution by waiting for a load to finish._
    * _AMD is generally more used in client-side (in-browser) JavaScript development due to this, and CommonJS Modules are generally used server-side. However, you can use either module spec in either environment - for example, RequireJS offers directions for running in Node.js and browserify is a CommonJS Module implementation that can run in the browser._
    * _My opinion ... !!!__complete this answer__!!!_ (also give code examples)
* Explain why the following doesn't work as an IIFE: `function foo(){ }();`.
  * What needs to be changed to properly make it an IIFE?
    * _If you don't wrap the function with parentheses, the JS parser will treat it as a function declaration, not a function expression. A function expression can be called immediately, but a function declaration cannot._
    * _Function Expression - `var test = function() {};`_
    * _Function Declaration - `function test() {};`_
    * _To be an IIFE you only have to do `(function (){ })();` or `(function (){ }())`_
* What's the difference between a variable that is: `null`, `undefined` or undeclared?
  * How would you go about checking for any of these states?
    * _A variable is undeclared if it isn't declared with a `var/let/const`. `console.log(a) => Uncaught ReferenceError: a is not defined`_
    * _It's undefined if it doesn't have a value attributed to it. `var a;` and if you do `console.log(a) => undefined`_
    * _A variable is attributed this value to specifically tell that this variable is empty. `var a = null; console.log(a) => null`_
* What is a closure, and how/why would you use one?
    * _In short, a closure is a way to keep access to variables in a function after that function has returned._
    * Or
    * _Closures are functions that have access to variables from anthor function's scope. This is often accomplished by creating a function inside a function._
    * _Found a very good explanation [here](http://lucybain.com/blog/2014/closures/)._
    ```javascript
    function stillAClosure(anotherLongLivedVariable) {
          var innerFunction = function inner() {
              return anotherLongLivedVariable;
          };
          return innerFunction;
      }
      var closure = stillAClosure("The same string");
      closure(); // returns "The same string"
      closure(); // returns "The same string"
      closure(); // returns "The same string"
      //And here’s even more proof:
      
      var closure1 = stillAClosure("String 1");
      closure1(); // returns "String 1"
      closure1(); // returns "String 1"
      
      var closure2 = stillAClosure("String 2");
      closure2(); // returns "String 2"
      closure2(); // returns "String 2"
      
      // And here's the kicker
      closure1(); // returns "String 1"  
    ```
    * _A closure is good to keep state in an application, to keep private things private (separation of concern)._
* What's a typical use case for anonymous functions?
    * _IIFE_
    * _event handler_
* How do you organize your code? (module pattern, classical inheritance?)
    * _I prefer using babel so I would use classes and inheritance based on ES2015. (Not a complete answer, bring in the design patters used)_
* What's the difference between host objects and native objects?
    * _Native objects are those objects supplied by JavaScript. Examples of these are String, Number, Array, Image, Date, Math, etc._
    * _Host objects are objects that are supplied to JavaScript by the browser environment. Examples of these are window, document, forms, etc._
* Difference between: `function Person(){}`, `var person = Person()`, and `var person = new Person()`?
    * _The first is a function declaration._
    * _The second is a declaration of a variable with an invocation of a function `Person` and sets the value to its returned value._
    * _The third creates a new instance of an object based on the Person function. The variable `person` in now an object with its prototype having the constructor the declared function._
* What's the difference between `.call` and `.apply`?
    * _With both you call a function in a scope (you bind a scope to the function). The difference is when you send parameters. With `foo.call(scope, param1, param2)` and with `foo.apply(scope, [param1, param2])`_
* Explain `Function.prototype.bind`.
    * _When `bind()` is called, it creates a new function that has its `this` keyword set to the provided value and it can receive also a sequence of arguments._
* When would you use `document.write()`?
    * _If you write `document.write("<h1>JS is awesome!</h1>");` it will replace the entire content of the document with that header._
    * _It seems that the only “approved” time to use document.write() is for third party code to be included (such as ads or Google Analytics). Since document.write() is always available (mostly) it is a good choice for third party vendors to use it to add their scripts. They don’t know what environment you're using, if jQuery is or isn’t available, or what your onload events are. And with document.write() they don’t have to._
* What's the difference between feature detection, feature inference, and using the UA string?
    * _Feature detection checks a feature for existence, e.g.:_
    ```javascript
    if (window.XMLHttpRequest) {
        new XMLHttpRequest();
    }
    ```
    * _Feature inference checks for a feature just like feature detection, but uses another function because it assumes it will also exist, e.g.:_
    ```javascript
    if (document.getElementsByTagName) {
        element = document.getElementById(id);
    }
    ```
    * _Checking the UA string is an old practice and should not be used anymore. You keep changing the UA checks and never benefit from newly implemented features, e.g.:_
    ```javascript
    if (navigator.userAgent.indexOf("MSIE 7") > -1){
        //do something
    }
    ```
* Explain Ajax in as much detail as possible.
    * _AJAX is short for Asynchronous Javascript + XML. The technique consisted of making server requests for additional data without unloading the page,resulting in a better user experience._
* What are the advantages and disadvantages of using Ajax?
    * _Advantages:_
        * _Easier navigation inside a application._
        * _You don't have to reload the whole page._
        * _You can have a only one page with all the interactions on it (SPA) without the need for other pages_
    * _Disadvantages:_
        * _If you don't have a way to update your routes (urls), the back and refresh button become useless, also there will be no way to have deep linking._
        * _If someone has JS disabled on their browser, your page is not accessible by that user._
* Explain how JSONP works (and how it's not really Ajax).
    * _Say you're on domain example.com, and you want to make a request to domain example.net. To do so, you need to cross domain boundaries, a no-no in most of browserland._
      
      _The one item that bypasses this limitation is `<script>` tags. When you use a script tag, the domain limitation is ignored, but under normal circumstances, you can't really do anything with the results, the script just gets evaluated._
      
      _Enter JSONP. When you make your request to a server that is JSONP enabled, you pass a special parameter that tells the server a little bit about your page. That way, the server is able to nicely wrap up its response in a way that your page can handle._
      
      _For example, say the server expects a parameter called "callback" to enable its JSONP capabilities. Then your request would look like:_
      
      `http://www.example.net/sample.aspx?callback=mycallback`
      
      _Without JSONP, this might return some basic JavaScript object, like so:_
      
      `{ foo: 'bar' }`
      
      _However, with JSONP, when the server receives the "callback" parameter, it wraps up the result a little differently, returning something like this:_
      
      `mycallback({ foo: 'bar' });`
      
      _As you can see, it will now invoke the method you specified. So, in your page, you define the callback function:_
      
      ```javascript
      mycallback = function(data){
        alert(data.foo);
      };
      ```
      _And now, when the script is loaded, it'll be evaluated, and your function will be executed. Voila, cross-domain requests!_
      
      _It's also worth noting the one major issue with JSONP: you lose a lot of control of the request. For example, there is no "nice" way to get proper failure codes back. As a result, you end up using timers to monitor the request, etc, which is always a bit suspect. The proposition for JSONRequest is a great solution to allowing cross domain scripting, maintaining security, and allowing proper control of the request._
      
      _These days (2015), CORS is the recommended approach vs. JSONRequest. JSONP is still useful for older browser support, but given the security implications, unless you have no choice CORS is the better choice._
* Have you ever used JavaScript templating?
  * If so, what libraries have you used?
    * _Is this the same as "Have you used different HTML templating languages before?"?_
* Explain "hoisting".
    * _If you have:_
    ```javascript
    (function() { 
      alert(myVar); // undefined 
      var myVar = 'local value'; 
    })();
    ```
    * _it will show undefined because only the `var myvar` is lifted (hoisted) on top, without the initialization._
* Describe event bubbling.
    * _Event bubbling_ 
    * ![alt text](https://javascript.info/files/tutorial/browser/events/event-order-bubbling.gif "Event bubbling")
    * _Event capturing_
    * ![alt text](http://www.senocular.com/flash/tutorials/buttoncapturing/images/capture.png "Event capturing")
    * _In all browsers, except IE<9, there are two stages of event processing. The event first goes down - that’s called capturing, and then bubbles up. This behavior is standartized in W3C specification. You can use capturing if you do this `element.addEventListener(type, handler, phase)` where `phase` can be true or false, where true means that the handler is set to capturing mode._
* What's the difference between an "attribute" and a "property"?
* Why is extending built-in JavaScript objects not a good idea?
* Difference between document load event and document DOMContentLoaded event?
    * _The DOMContentLoaded event is fired when the document has been completely loaded and parsed, without waiting for stylesheets, images, and subframes to finish loading (the load event can be used to detect a fully-loaded page)._
* What is the difference between `==` and `===`?
    * _JavaScript has both strict and type-converting equality comparison. For strict equality the objects being compared must have the same type and:_
       * _Two strings are strictly equal when they have the same sequence of characters, same length, and same characters in corresponding positions._
       * _Two numbers are strictly equal when they are numerically equal (have the same number value). NaN is not equal to anything, including NaN. Positive and negative zeros are equal to one another._
       * _Two Boolean operands are strictly equal if both are true or both are false._
       * _Two objects are strictly equal if they refer to the same Object._
       * _Null and Undefined types are == (but not ===). [I.e. (Null==Undefined) is true but (Null===Undefined) is false]_
* Explain the same-origin policy with regards to JavaScript.
    * _The same-origin policy restricts how a document or script loaded from one origin can interact with a resource from another origin. It is a critical security mechanism for isolating potentially malicious documents._
    * _Two pages have the same origin if the protocol, port (if one is specified), and host are the same for both pages. The following table gives examples of origin comparisons to the URL http://store.company.com/dir/page.html:_
    
    | URL        | Outcome           | Reason  |
    | ------------- |:-------------:| -----:|
    | http://store.company.com/dir2/other.html | Success |	 
    | http://store.company.com/dir/inner/another.html | Success|	 
    | https://store.company.com/secure.html |Failure | Different protocol|
    | http://store.company.com:81/dir/etc.html |Failure |Different port|
    | http://news.company.com/dir/other.html |Failure |Different host|
* Make this work:
```javascript
duplicate([1,2,3,4,5]); // [1,2,3,4,5,1,2,3,4,5]
```
    
        function duplicate(arr) {
            return arr.concat(arr);
        }
    
* Why is it called a Ternary expression, what does the word "Ternary" indicate?
    * _A unary operand accepts one parameter, e.g. -1, where - is the operand, and 1 is the parameter._
    
      _A binary operand accepts two parameters, e.g. 2 + 3, where + is the operand, and 2 and 3 are the parameters._
       
      _So a ternary operand accepts three parameters._
    * _In programming the ternary operand we use is a rewrite of an if statement. `condition ? true_block : false_block`_
* What is `"use strict";`? what are the advantages and disadvantages to using it?
    * _This enables Strict Mode that allows you to place a program or a function in a strict operating context. This prevents certain actions to be taken and throws more exceptions._
    * _It catches some common coding bloopers, throwing exceptions. (ex. assigning `foo = 'bar';` without first defining `foo` will throw an exception)_
    * _It prevents, or throws errors, when relatively "unsafe" actions are taken (such as gaining access to the global object)._
    * _It disables features that are confusing or poorly thought out._
    * _More about Strict Mode [here](http://ejohn.org/blog/ecmascript-5-strict-mode-json-and-more/)._
* Create a for loop that iterates up to `100` while outputting **"fizz"** at multiples of `3`, **"buzz"** at multiples of `5` and **"fizzbuzz"** at multiples of `3` and `5`
* Why is it, in general, a good idea to leave the global scope of a website as-is and never touch it?
    * _It’s harder to read the code and reason about it when variables seem to appear out of thin air (but really from the global scope)._
    * _Anyone can update a global variable from any point in the program at any time (and from any thread if there’s more than one going)._
    * _General code smell - if you're too lazy to put the variable only where it needs to be then what other corners are you cutting?_
    * _It’s probable that you'll encounter global variable name clashes. Since there’s only one namespace you're more likely to double up on a variable name._
* Why would you use something like the `load` event? Does this event have disadvantages? Do you know any alternatives, and why would you use those?
* Explain what a single page app is and how to make one SEO-friendly.
    * _I consider a SPA a web application that is built on JS MVC frameworks. I don't consider a SPA a infinity scrolling page (pinterest) or a single page theme on wordpress._
    * _A problem might be with the router of your web app. If it's not configured to use true urls (using the new HTML5 History API), the robots parsing your site will have trouble interpreting pages with `url/#/my/page`, because they will consider it to be the same page as before the `#`._
* What is the extent of your experience with Promises and/or their polyfills?
* What are the pros and cons of using Promises instead of callbacks?
* What are some of the advantages/disadvantages of writing JavaScript code in a language that compiles to JavaScript?
* What tools and techniques do you use debugging JavaScript code?
* What language constructions do you use for iterating over object properties and array items?
* Explain the difference between mutable and immutable objects.
  * _Answer: A mutable object can have its values and keys changed, where as a immutable object can't be changed whatsoever._
  * What is an example of an immutable object in JavaScript?
    * _Strings and numbers are immutable but they're not considered objects. You can obtain an immutable object using `Object.freeze()`._
    * ```javascript
        var o = {a: 1, b:2};
    
        o.a = 3;
        //nothing happens, o remains the same (this will fail silently or by throwing a TypeError (most commonly, but not exclusively, when in strict mode)
    * But the freeze only works one level. 
  * What are the pros and cons of immutability?
    * _Pros:_
        * _If you keep your application state in an immutable object, you can track down your object history more easily_
        * _(add more)_
    * _Cons:_
        * _It needs more attention when working with it, because mutability comes to us more naturally_
        * _(add more)_
  * How can you achieve immutability in your own code?
    * _You can use Immutable.js. If you don't want to use this, you can also use (for Objects) `Object.assign({}, obj)` or (if not in ES2015) `_.extend({}, obj)` or `$.extend({}, obj)`
    * For arrays `[].contact(list)`
* Explain the difference between synchronous and asynchronous functions.
* What is event loop?
  * What is the difference between call stack and task queue?
* Explain the differences on the usage of `foo` between `function foo() {}` and `var foo = function() {}`

##### My JS Questions:
* What is the difference between `target` and `currentTarget` in an event?
    * `target` is the clicked element and `currentTarget` is the element on which the handler is bound.
* Why would you use an IIFE?
    * _You can easily create a scope._
* What is `eval`?
    * _It evaluates JS code represented as a string. It returns a string containing the response of the code given or undefined if the response is empty._
    * _If you use the eval function indirectly, by invoking it via a reference other than eval, as of ECMAScript 5 it works at global scope rather than local scope; this means, for instance, that function declarations create global functions, and that the code being evaluated doesn't have access to local variables within the scope where it's being called._
    ```javascript
    function test() {
      var x = 2, y = 4;
      console.log(eval("x + y"));  // Direct call, uses local scope, result is 6
      var geval = eval;
      console.log(geval("x + y")); // Indirect call, uses global scope, throws ReferenceError because `x` is undefined
    }
    ```
* What are the pitfalls of using `eval`?
    * _If you run `eval()` with a string that could be affected by a malicious party, you may end up running malicious code._
    * _It's also slower because it needs to invoke the JS interpreter. (it needs compilation)_
* What is `__proto__` vs `prototype`?
* What does the `new` keyword do?
    * _When the code new Foo(...) is executed, the following things happen:_
       * _A new object is created, inheriting from Foo.prototype._
       * _The constructor function Foo is called with the specified arguments, and with this bound to the newly created object. new Foo is equivalent to new Foo(), i.e. if no argument list is specified, Foo is called without arguments._
       * _The object returned by the constructor function becomes the result of the whole new expression. If the constructor function doesn't explicitly return an object, the object created in step 1 is used instead. (Normally constructors don't return a value, but they can choose to do so if they want to override the normal object creation process.)_
* Difference between typeof and instanceOf.
* How do you create a new class using es5? How do you extend using es5?
    ```javascript
    //creation of a class a.k.a. a function
    function Hello(name) {
      this.name = name;
    }
    
    //adding a method to a prototype - there are two advantages: every other class that extends this one
    //will have this method and this method will not be recreated for each instance of the Hello class
    Hello.prototype.hello = function hello() {
      return 'Hello ' + this.name + '!';
    };
    
    //adding a method only to the Hello class. Every other class that extends this one, will not have this method.
    Hello.sayHelloAll = function () {
      return 'Hello everyone!';
    };
    
    //(1) extending the Hello class
    function HelloWorld() {
      Hello.call(this, 'World');
    }
    
    //(2) extending the Hello class. Setting the Hello prototype to the HelloWorld prototype. (setting the prototype chain)
    HelloWorld.prototype = Object.create(Hello.prototype);
    
    //While not strictly necessary, it's there to preserve some useful invariants. Since the assignment to HelloWorld.prototype 
    //kills the existing Hello.prototype.constructor (which was set to HelloWorld when the HelloWorld constructor was created), we restore it.
    HelloWorld.prototype.constructor = HelloWorld;
    
    //(3) using the same method for HelloWorld
    HelloWorld.sayHelloAll = Hello.sayHelloAll;
    
    //Instead of (1), (2) and (3) couldn't you just make the following?????
    var HelloWorld2 = Object.create(Hello, {name: 'World2'});
    
    HelloWorld.prototype.echo = function echo() {
      alert(Hello.prototype.hello.call(this));
    };
    
    var hw = new HelloWorld();
    hw.echo();
    ```
    * _Detailed explanation [here](http://eli.thegreenplace.net/2013/10/22/classical-inheritance-in-javascript-es5)_
* Is string an object in JS?
    * _"Everything is an object"... that's one of the big misconceptions that exist all around the language. Not everything is an object, there are what we call primitive values, which are string, number, boolean, null, and undefined. That's true, a string is a primitive value, but you can access all the methods inherited from String.prototype as if it were an object. The property accessor operators (the dot and the bracket notation), temporarily convert the string value to a String object (__coercion__), for being able to access those methods._
* What do you know about functional programming? What are the ups and downs?
* Give examples of some functional programming concepts.
* What JS design patterns do you know?
    * _Singleton: _
    * _Factory: _

#### Testing Questions:

* What are some advantages/disadvantages to testing your code?
    * _Advantages:_
        * _If someone changes something in the code, it can be caught at unit testing (refactoring made easy with a safety net)_
        * _For a new-comer, reading the unit tests could shed light on the written code_
    * _Disadvantages:_
        * _It takes time_
        * _It takes time to maintain the tests if the logic changes_
* What tools would you use to test your code's functionality?
    * _I used mocha and chai for asserting and now I'm using Enzyme for testing React components. I also fiddled around with Jest._
* What is the difference between a unit test and a functional/integration test?
    * _A unit test tests the functionality of the code and an integration test test how something works in the bigger picture (sometimes with interaction, databases and it's much more complex)_
* What is the purpose of a code style linting tool?
    * _It's good to use a linting tool because it helps you be more constant in your writing and if someone reads your code, the chances that he could understand your code increase._

#### Performance Questions:

* What tools would you use to find a performance bug in your code?
* What are some ways you may improve your website's scrolling performance?
* Explain the difference between layout, painting and compositing.

#### Network Questions:

* Traditionally, why has it been better to serve site assets from multiple domains?
* Do your best to describe the process from the time you type in a website's URL to it finishing loading on your screen.
* What are the differences between Long-Polling, Websockets and Server-Sent Events?
* Explain the following request and response headers:
  * Diff. between Expires, Date, Age and If-Modified-...
  * Do Not Track
  * Cache-Control
  * Transfer-Encoding
  * ETag
  * X-Frame-Options
* What are HTTP methods? List all HTTP methods that you know, and explain them.

#### Coding Questions:

*Question: What is the value of `foo`?*
```javascript
var foo = 10 + '20';

'1020';
```

*Question: How would you make this work?*
```javascript
add(2, 5); // 7
add(2)(5); // 7

var add = function(x) {
    return function(y) { return x + y; };
}
```

*Question: What value is returned from the following statement?*
```javascript
"i'm a lasagna hog".split("").reverse().join("");

"goh angasal a m'i"
```

*Question: What is the value of `window.foo`?*
```javascript
( window.foo || ( window.foo = "bar" ) );

"bar"
```

*Question: What is the outcome of the two alerts below?*
```javascript
var foo = "Hello";
(function() {
  var bar = " World";
  alert(foo + bar);
})();
alert(foo + bar);

"Hello World"

and 

Uncaught ReferenceError: bar is not defined
```

*Question: What is the value of `foo.length`?*
```javascript
var foo = [];
foo.push(1);
foo.push(2);

2
```

*Question: What is the value of `foo.x`?*
```javascript
var foo = {n: 1};
var bar = foo;
foo.x = foo = {n: 2};

//--THIS IS KIND OF TRICKY--//
foo.x == undefined;
//why?
/* Because bar now keeps the reference from the first declaration of foo, that is
  bar == {n: 1}
  Now foo.x is {n: 2}, but then foo is overwritten by {n: 2}. That's why
  foo == {n: 2}
  bar == {n: 1, x: {n: 2}}
 */
```

*Question: What does the following code print?*
```javascript
console.log('one');
setTimeout(function() {
  console.log('two');
}, 0);
console.log('three');

'one'
'three'
'two'

/* Although timeout of 0 would mean that it should be run immediatelly, in JS priority have the operations that are on the top level */
```

#### Fun Questions:

* What's a cool project that you've recently worked on?
* What are some things you like about the developer tools you use?
    * _In PHP Storm I like the git, eslint, testing integrations_
* Who inspires you in the front-end community?
    * _The dynamic of this field can be exhausting and thrilling. The fact that as time goes by, JS reaches new and new frontiers (React Native/Node/Electron) ... makes me think, where will it end?_
* Do you have any pet projects? What kind?
    * _I have a project that I work on for a humanitarian non-profit. It's built with Laravel, Backbone and SCSS._
* What's your favorite feature of Internet Explorer?
* How do you like your coffee?
    * _I don't drink coffee :)_


#### Contributors:

This document started in 2009 as a collaboration of [@paul_irish](https://twitter.com/paul_irish) [@bentruyman](https://twitter.com/bentruyman) [@cowboy](https://twitter.com/cowboy) [@ajpiano](https://twitter.com/ajpiano)  [@SlexAxton](https://twitter.com/slexaxton) [@boazsender](https://twitter.com/boazsender) [@miketaylr](https://twitter.com/miketaylr) [@vladikoff](https://twitter.com/vladikoff) [@gf3](https://twitter.com/gf3) [@jon_neal](https://twitter.com/jon_neal) [@sambreed](https://twitter.com/sambreed) and [@iansym](https://twitter.com/iansym).

It has since received contributions from over [100 developers](https://github.com/h5bp/Front-end-Developer-Interview-Questions/graphs/contributors).
