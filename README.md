A curated list of frontend interview questions.

# Table of Contents

  1. [General Questions/Ice Breaker](#general)
  1. [Management Questions](#management)
  1. [JavaScript Questions](#javascript)
  1. [HTML Questions](#html)
  1. [CSS Questions](#css)
  1. [HTTP Questions](#http)
  1. [Problem Solving Questions](#problem-solving)
  1. [Algos, Data Structures, & Computer Science Fundamentals Questions](#algorithms)
  1. [Basic Questions](#basic-questions)

----

## <a name='general'>General/Ice Breaker</a>

>You're looking for passion and enthusiasm when a candidate discusses their previous projects and any projects they're working on in their spare time. If they get excited talking about these things, they show the kind of passion for software development that is a good indicator of whether they're capable of meeting the your bar.
Once you've calmed a nervous candidate's nerves or determined level of passion/enthusiasm, move on to the next set of questions. Try to spend a maximum of 5 minutes on this section.

* Tell us about your most recent project.
* Do you ever do any coding in your personal time (outside of work)?
* Do you have a account on Github?
  * If so, what are some examples of repos you follow?
* Tell us what critical problems you have to handle in your latest projects?
* Walk us through the process of creation of an application or website you've built.
* Why did you get into development?
* How many technical books did you read in the past year?
* What was your favorite technical book in the past year? What did you learn from it?
* What websites do you read regularly, related to development?
* Do you maintain any open-source projects?
* Do you code in your spare-time?
* Do you love programming, or do you do it for the money?
* Have you accomplished anything important in your career yet? Do you want to?
* What would make you feel that you have done something important?
* What's your favorite programming language? Why? 
* If you could add one feature to your favorite language, what would it be? Why?
* If you could remove one feature from it, what would it be? Why?

## <a name='management'>Management</a>

* How to tackle a story/task which is difficult to estimate and with high risk?

> 
  - Investigate as early as possible
  - Assign senior staffs on the problem
  - More frequent update and more communication
  - Report higher level supervisors to be aware of the situation

* How to react to unexpected/frequent requirement changes, considering PoC phase and production phase.

>
  - For PoC: 
    - communicate with team members to let them know things are changing. 
    - Proving the solution is more important than perfect design/implementation. For requirement changes, argue for the reason. If it is business reason, mostly we should follow. If it is technical reason, we should discuss first and then make decision.
  - For production: 
    - Setup a process first. A requirement change should result in following reactions after replan (re-estimation):
         - If it is not so urgent, keep working, change the future plan
         - If it is urgent, either request resource (considering the
ramp-up cost) or cut features
         - If not possible, suggest delay the release date

* How to keep a team stable with limited offer. (How's about if you can't increase the compensation while the competitors can give more)

>Basically, setup a good working environment all the time, making team members work happily, and with good development direction and opportunity. If things really happens, resort to higher-level manager and HR to find out a solution.

## <a name='javascript'>JavaScript</a>

* What is ECMAScript, JScript?
* What is the Document Object Model(DOM)?
* What's the different between undefined and null? It's better to say something about why we need undefined if we have had null.
* What's JavaScript strict mode? What's the intent for it? What does it do? How do you use it?
* What is AJAX? What the work flow for AJAX? How to implement CORS? What's the difference synchronous and asynchronous for JavaScript?
* Say something about JavaScript Encapsulation.
* Say something about JavaScript Inheritance(Classical Versus Modern Inheritance).
* What is Closure? 
* When and why you need to use `this` keyword?
* How to handle cookie using JavaScript?
* DOM manipulation – how to add, remove, move, copy, create, and find nodes.
* As for JavaScript regex, what is greediness, lazy, negated character classes matching? How to write a regex to match `<script>greediness</script>`?
* Events - how to use them and the major differences between IE and the DOM event models?
* XMLHttpRequest – what it is, how to perform a complete GET request, how to detect errors?
* JSON – what it is, why you'd want to use it, how to actually use it, implementation details?
* Promise - what it is, and why we need that? What problems it solve?
* Using only a single event handler on the parent, detect a swipe left and a swipe right and alert() which direction was swiped.
* Write an example of a closure in javascript. It doesn't matter what the code does, as long as it shows a closure being created.
* Difference between `document.write` and `innerHTML`.
* How `delete` operator works in JavaScript? What exactly can and cannot be deleted and why.
* How does prototypal inheritance work?
* What defines a closure?
* How does the meaning of this keyword change?
* How does one use apply/bind/map/filter/call?
* Say how would you describe the flow-control steps of this program?
  ~~~JavaScript
  makeAjaxRequest( url, function(response){ alert( "Response: " + response ); } );
  ~~~

* Write a factorial function.
* Write a function that accepts a string then reverses it. Recursively is better.
  ~~~JavaScript
  function reverseString(str) {
    return str.split("").reverse().join("");
  }

  // With Recursion
  function reverseString(str) {
    return (str === '') ? '' : reverseString(str.substr(1)) + str.charAt(0);
  }

  // In ES6, you have one more option
  [...str].reverse().join('')
  ~~~

* Write a Recursivelye map function.
  ~~~JavaScript
  function map(arr, fn) {
    if (arr.length === 0) {
      return [];
    }

    return [fn(arr[0])].concat(map(arr.slice(1), fn));
  }
  ~~~

* What is the difference between these four promises?
  ~~~JavaScript
  doSomething().then(function () {
    return doSomethingElse();
  }).then(finalHandler);

  doSomething()
    .then(function () {
      doSomethingElse();
    })
    .then(finalHandler);

  doSomething()
    .then(doSomethingElse())
    .then(finalHandler);

  doSomething()
    .then(doSomethingElse)
    .then(finalHandler);
  ~~~

* What's the result of the below JavaScript snippet in the native implementation?
  ~~~JavaScript
  setTimeout(function(){console.log("three");}, 0);

  Promise.resolve().then(function(){ console.log( "two" ); });

  console.log("one");
  ~~~

* Explain the use cases for, and differences between — `bind`, `apply` and `call`.
* Explain event delegation and why it is useful.
* What is the event loop?
* How does hoisting work in JavaScript?
* Which new JavaScript features are you most excited about and why?
* Prototypal inheritance is so cool for JavaScript especially when trying to keep code DRY and maintainable, but do you know what's the output for the code below?
  ~~~JavaScript
  var parent = {
    get: function fn() {
      return this.val;
    },
    val: 42
  };

  var child = Object.create(parent);
  child.val = 3.14159;
  var grandchild = Object.create(child);

  console.log(parent.get());
  console.log(child.get());
  console.log(grandchild.get());
  ~~~
* What is a pure function?

  A pure function is a function which:
    * Given the same input, will always return the same output.
    * Produces no side effects.
    * Relies on no external state.


## <a name='html'>HTML</a>

* What is `<!DOCTYPE>` tag? How to use it?
* What's the difference between childNodes[] and children[]?
* DOM structure – how nodes are related to one another and how to traverse from one to the next.
* DOM manipulation – how to add, remove, move, copy, create, and find nodes.
* Strict vs quirks modes – how to trigger each and why this matters.
* Block vs inline elements – how to manipulate using CSS, how they effect things around them and your ability to style them.
* Floating elements – how to use them, troubles with them, and how to work around the troubles.
* HTML vs. XHTML(1.x&2) – how they're different, why you might want to use one over the other.
* List semantic elements in HTML5 as much as you can and why we need them.
* Write a 'Hello, Word!' html page. (whether get to know the necessary HTML tag for one page, DOCTYPE definition,...).
* What's difference between XHTML 1.x and HTML4?
* What's the difference between h1~h6? How's about difference between ul and ol?
* Have you ever got a chance to use dl, dt, dd? What's the semantic for them?
* What's the common properties used with `form`?
* What's going on if we don't set the `type` property for `input` element?
* What's the use case if we set the `type` property as `image` for `input` element?

## <a name='css'>CSS</a>

* What is CSS?
* List the CSS hacks as much as you can.
* What's the possible values of `display` property? What is block and inline element and what the difference between them? List block and inline tags as much as you can.
* The box model - how margin, padding, and border are related and the difference between border-box (standards mode) and content-box (old Internet Explorer) sizing.
* List CSS Layout.
* What is CSS stack and say something about it?
* List the browser compatibility problems you have ever used or known.
* List the possible values for `position` property and the result for every value.
* List the possible values for `display` property and the result for every value.
* What is the distinguishing feature provided by `display: inline-block`?
* Say something about CSS3, such as transition, animation, transform, etc..
* What's box-sizing and when you need it?
* What's CSS transform?
* Say something about Flexbox: why we need it? how it works? how we use it?
* Why Table are bad for layout?
* What's use case for float property? How to clear float?
* What CSS selector have you ever used?
* What's the difference between `cssRules` and `rules`

## <a name='http'>HTTP</a>

* List HTTP status codes as much as you can.
* What's the meaning for HTTP status of 200, 302, 304, 404, 500, 503.
* Introduce something about Web Cache or HTTP caching, such as what's Conditional GET Requests? Etags? Expires? Cache-Control?
* What's the difference between Get and Post http method?
* What's the difference between HTTP stateless and `Connection:keep-alive`?
* What's the message structure for HTTP Request/Response?
* What's the difference between HTTP status code 301 and 302? How search engines handle them?
* What's the HTTP Header related with cache? What's the usage for them?
* When you're sending a Ajax request, how to judge whether full server response has been received and it's OK for you to continue processing it?
* Why we could avoid local cache when using CTRL+F5 or refresh button to reload the page?
* Why we should put stylesheets at the top and put the scripts at the Bottom?
* What a HTTP request/response message packet includes?

## <a name='problem-solving'>Problem Solving</a>

* Classic beginner programming problem: the guessing game. Here’s how it works: Our program will generate a random integer between one and a hundred. It will then prompt us to enter a guess. Upon entering our guess, it will tell us if we’re too low or too high. Once we guess correctly, it will congratulate us.
* Add a `unique` method for Array in order to produce a duplicate-free version of the array using [Vanilla JS](https://jsfiddle.net/starandtina/87TSF/) or [with ES5 compatiable JS](https://jsfiddle.net/starandtina/b6hbtbhz/).
* Implement deep clone for inheritance by copying properties from object using Vanilla JS.
* Control the max-length of input element using JavaScript, if it extends the max length and then set the border of input element as red.
* Change all elements with className of `test` to yellow background using JavaScript or jQuery.
* Write a marquee program using JavaScript.
* Translate your hexadecimal color value to RGB.
* Generate random numbers that are consecutively unique.
* Find the index of the smallest element in a JavaScript array.
* Check whether a value is an integer in JavaScript.
* [Make it work:](https://jsfiddle.net/starandtina/et7dnge8/)

  ~~~JavaScript
  [1, 2, 3].duplicate(); // [1, 2, 3] => [1, 2, 3, 1, 2, 3]
  ~~~
* Checking whether a value is `NaN` in JavaScript?
* How to load CSS/JavaScript files asynchronously? If you know that, then write `loadCSS` and `loadJS` function in order to load CSS/JavaScript files asynchronously.
* Make the codes below work as expected with a simple template engine.

  ~~~JavaScript
  var tpl = template('<p>hey there {{ name }}</p>');
  var div = document.createElement('div');
  div.innerHTML = tpl({ name: 'Neo' });
  document.body.appendChild(div);
  ~~~
* Define a `spacify` function which takes a string as an argument, and returns the same string but with each character separated by a space, for example: 

  ~~~JavaScript
  spacify('hello world') // => 'h e l l o w o r l d'
  ~~~~
  If it's right, the follow-up question to this, is to place the `spacify` function directly on the String object, for example:

  ~~~JavaScript
  'hello world'.spacify();
  ~~~~
* [Implement collection pivot](https://jsfiddle.net/starandtina/e6n5h/): Pivot means put all the things left of the middle element right, and vice versa,  
  
  ~~~JavaScript
  Eg: Pivot {A, B, C} should give {C, B, A}
        Pivot { 1, 2, 3, 4 } should give { 3, 4, 1, 2 }
        Pivot { 1, 2, 3, 4, 5, 6, 7 } should give { 5, 6, 7, 4, 1, 2, 3 }
        Pivot { 11, 8, 45 } should give { 45, 8, 11 }
     Hint: What type should input/output be? Why?
  ~~~
* Provide a functional version of `each` or `forEach` used to iterates over a list of elements, yielding each in turn to an iteratee function.
* Provide a functional version of `function.apply`.
* Partially apply a function by filling in any number of its arguments, without changing its dynamic this value. 
* Implement _currying_ in which we could pre-fill arguments to a function before it's executed.
* Write your own function composition, returns the composition of a list of functions, where each function consumes the return value of the function that follows. In math terms, composing the functions `f()`, `g()`, and `h()` produces `f(g(h()))`.
* Shuffle an array of numbers using [Fisher-Yates shuffle](http://en.wikipedia.org/wiki/Fisher%E2%80%93Yates_shuffle).
* Provide a polyfill of string trim function.
* Get the max or the min in an array of numbers.
* An HTML escaper function.
* [Find an item by property in an array](https://gist.github.com/starandtina/267f2935c2f3f1553ee5).

## <a name='algorithms'>Algos, Data Structures, & Computer Science Fundamentals</a>
> Algorithm is at the heart of every nontrivial computer application, and algorithmic is a modern and active area of computer science. Every computer scientist and every professional programmer should know about the basic algorithmic toolbox: structures that allow efficient organization and retrieval of data, frequently used algorithms, and basic techniques for modeling, understanding and solving algorithmic problems and our expectation of
event candidates is that they are very strong in this area.

* Merge sort has a complexity of O(n*log n), making it one of the more efficient sorting algorithms available, also it's a stable sort. That's why Firefox and Safari use merge sort for their implementation of `Array.prototype.sort()`. Please implement `Array.prototype.sort()` using merge sort.
* Binary search implementation in JavaScript.
* Define a function that returns n lines of [Pascal’s Triangle](https://en.wikipedia.org/wiki/Pascal%27s_triangle).
* Use recursion to log a fibonacci sequence of n length. (Notice: only need to log instead of calculating the result)

  ~~~JavaScript
  function fib(depth, n1, n2) {
    if (!depth) { return; }
    console.log(n1);
    fib(depth-1, n2, n1 + n2);
  }
  ~~~
* How to find the longest word in a string with JavaScript?

  ~~~JavaScript
  "The quick brown fox jumped over the lazy dog".split(' ').sort(function (a, b) {
    return b.length - a.length;
  })[0].length;
  ~~~

## <a name='basic-questions'>Basic Questions</a>

~~~
function foo(a, b, c) {
  return a + b + c;
}
console.log(foo(1, 2));

// --------------------------------------

function DB() {
  this.read = function () {
    // ...
    console.log('Call read method')
  }
}
var db = new DB();
var aRead = db.read;

db.read();
aRead();

// --------------------------------------

var parent = {
  get: function fn() {
    return this.val;
  },
  val: 1
};

var child = Object.create(parent);
child.val = 3.14159;
var grandchild = Object.create(child);

console.log(parent.get());
console.log(child.get());
console.log(grandchild.get());

// --------------------------------------

for (var i = 1; i <= 5; i++) {
  setTimeout(function timer() {
    console.log(i);
  }, i * 1000);
}

// --------------------------------------

function foo() {
  console.log(a);
}

function bar() {
  var a = 3;

  foo();
}

var a = 2;

bar();
~~~

## License

[![CC0](https://i.creativecommons.org/p/zero/1.0/88x31.png)](https://creativecommons.org/publicdomain/zero/1.0/)
