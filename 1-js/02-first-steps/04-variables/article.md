# চলক [Variables]

অধিকাংশ সময়, একটি জাভাস্ক্রিপ্ট অ্যাপ্লিকেশনে উপাত্ত (Data) নিয়ে কাজ করার প্রয়োজন হয় । এখানে ২টি উদাহরন দেয়া হলঃ 

​	১। একটি অনলাইন শপ -- বিক্রিত পণ্য এবং একটি শপিং কার্টের উপাত্তগুলো থাকতে পারে । 

​	২। একটি চ্যাট অ্যাপ্লিকেশন -- ব্যবহারকারীদের (Users), বার্তাসমূহের (Messages), এবং আরো অনেক কিছুর উপাত্ত থাকতে পারে ।

এই উপাত্তগুলো জমা (Store) করতে চলক (Variable)  ব্যবহৃত হয় ।

## একটি চলক: কেন, কিভাবে

একটি [চলক](https://en.wikipedia.org/wiki/Variable_(computer_science)) হল উপাত্ত ধারন করার জন্য "সংরক্ষণের জায়গায় নাম" । আমরা চলক (Variables) ব্যাবহার করে জিনিসপত্র, ক্রেতা, এবং অন্য কোন উপাত্ত সংরক্ষণ করে রাখতে পারি । 

জাভাস্ক্রিপ্টে একটি চলক তৈরি করতে, `let` কি-ওয়ার্ড‌ ব্যবহার করবে । 

নিচের স্টেটমেন্ট-টি "message" নামক একটি চলক তৈরি (অন্যকথায়ঃ *declare*) করেঃ 

```js
let message;
```

এখন, আমরা এটিতে কিছু উপাত্ত রাখতে পারি নির্দেশক (*assignment*) অপারেটরের মাধ্যমে `=`:

```js
let message;

*!*
message = 'হ্যালো'; // অক্ষরগুলো জমা থাকছে
*/!*
```

এই অক্ষরগুলো এখন মেমোরিতে চলকটির দ্বারা জমা হল । যা আমরা চলকটির নাম দ্বারা অ্যাক্সেস করতে পারিঃ 

```js run
let message;
message = 'হ্যালো!';

*!*
alert(message); // চলক-এ সংরক্ষিত জিনিস প্রদর্শন করবে
*/!*
```

সংক্ষেপে, আমরা চলক তৈরি এবং এসাইনমেন্ট একযোগে একটি লাইনে করতে পারিঃ 

```js run
let message = 'হ্যালো!'; // চলক তৈরি এবং এর মান নির্দেশ করা হয়েছে

alert(message); // হ্যালো!!
```

We can also declare multiple variables in one line:

 এছাড়াও আমরা একটি লাইনে একাধিক চলক নির্দেশ করতে পারিঃ 

```js no-beautify
let user = 'আসিফ', age = 20, message = 'হ্যালো';
```

এটা হয়ত মনে হবে ছোট, কিন্তু এই পদ্ধতি আমরা উপযোগী বলে মনে করি না । দেখার সুবিধা বিবেচনায়, অনুগ্রহ করে প্রতি চলকের জন্য একটি মাত্র লাইন ব্যবহার করবে । 

একাধিক লাইনের পদ্ধতি একটু বড়, তবে পড়তে সহজঃ 

```js
let user = 'আসিফ';
let age = 20;
let message = 'হ্যালো';
```

কেউ কেউ আবার এই পদ্ধতিতে একাধিক চলক নির্দেশ করেঃ

```js no-beautify
let user = 'আসিফ',
  age = 20,
  message = 'হ্যালো';
```

...Or even in the "comma-first" style:

...অথবা এমনকি "কমা-প্রথমে" দিয়েঃ 

```js no-beautify
let user = 'আসিফ'
  , age = 20
  , message = 'হ্যালো';
```

টেকনিক্যালি, এই সবগুলো পদ্ধতি একই কাজ করবে । সুতরাং, এটা ব্যক্তিগত পছন্দ এবং নান্দনিকতার বেপার । 

 ````smart header="`let` এর পরিবর্তে `var`"
পুরানো স্ক্রিপ্টে, তুমি অন্য একটি কি-ওয়ার্ড‌ও পেতে পারঃ `let` এর পরিবর্তে `var`:

```js
*!*var*/!* message = 'হ্যালো';
```

`var` কি-ওয়ার্ড‌ হল `let` এর *প্রায়*  একই । এটিও (var) চলক নির্দেশ করে, কিন্তু কিছুটা আলাদা, "মান্ধাতার আমলের" পদ্ধতি এটি । 

`let` এবং `var` এর মধ্যে সূক্ষ্ম পার্থক্য আছে, কিন্তু সেগুলো এই মুহূর্তে আমাদের জন্য গুরুত্বপূর্ণ নয় । আমরা এগুলো <info:var> অধ্যায়ে বিস্তারিত আলোচনা করব । 
````

## একটি বাস্তব জীবনের উদাহরন

We can easily grasp the concept of a "variable" if we imagine it as a "box" for data, with a uniquely-named sticker on it.
আমরা যদি এটির জন্য অনন্য-নামযুক্ত স্টিকার সহ ডেটার জন্য একটি "বাক্স" হিসাবে কল্পনা করি তবে আমরা সহজেই একটি "variable" ধারণাটি উপলব্ধি করতে পারি ।

উদাহরণস্বরূপ, একটি চলক `message` যার মান `"Hello!"` যা একটি `"message" লেবেলযুক্ত বাক্স হিসাবে কল্পনা করা যায়:

![](variable.svg)

আমরা বাক্সে যেকোনো মান রাখতে পারি ।

এছাড়াও আমরা এটি যতবার চাই পরিবর্তন করতে পারি:
​```js run
let message;

message = 'Hello!';

message = 'World!'; // value changed

alert(message);
```

যখন মান পরিবর্তন করা হয়, পুরানো ডেটা ভেরিয়েবল থেকে সরানো হয়:

![](variable-change.svg)

আমরা দুটি ভেরিয়েবল ডিক্লেয়ার করতে পারি এবং এক থেকে অন্যটিতে ডেটা কপি করতে পারি।

```js run
let hello = 'Hello world!';

let message;

*!*
// hello থেকে 'Hello world' কপি করে message এ রাখছে
message = hello;
*/!*

// এখন দুটি ভেরিয়েবলে একই ডেটা আছে
alert(hello); // Hello world!
alert(message); // Hello world!
```

```smart header="Functional languages"
It's interesting to note that there exist [functional](https://en.wikipedia.org/wiki/Functional_programming) programming languages, like [Scala](http://www.scala-lang.org/) or [Erlang](http://www.erlang.org/) that forbid changing variable values.

In such languages, once the value is stored "in the box", it's there forever. If we need to store something else, the language forces us to create a new box (declare a new variable). We can't reuse the old one.

Though it may seem a little odd at first sight, these languages are quite capable of serious development. More than that, there are areas like parallel computations where this limitation confers certain benefits. Studying such a language (even if you're not planning to use it soon) is recommended to broaden the mind.
```

## Variable naming [#variable-naming]

There are two limitations on variable names in JavaScript:

1. The name must contain only letters, digits, or the symbols `$` and `_`.
2. The first character must not be a digit.

Examples of valid names:

```js
let userName;
let test123;
```

When the name contains multiple words, [camelCase](https://en.wikipedia.org/wiki/CamelCase) is commonly used. That is: words go one after another, each word except first starting with a capital letter: `myVeryLongName`.

What's interesting -- the dollar sign `'$'` and the underscore `'_'` can also be used in names. They are regular symbols, just like letters, without any special meaning.

These names are valid:

```js run untrusted
let $ = 1; // declared a variable with the name "$"
let _ = 2; // and now a variable with the name "_"

alert($ + _); // 3
```

Examples of incorrect variable names:

```js no-beautify
let 1a; // cannot start with a digit

let my-name; // hyphens '-' aren't allowed in the name
```

```smart header="Case matters"
Variables named `apple` and `AppLE` are two different variables.
```

````smart header="Non-Latin letters are allowed, but not recommended"
It is possible to use any language, including cyrillic letters or even hieroglyphs, like this:

​```js
let имя = '...';
let 我 = '...';
```

Technically, there is no error here, such names are allowed, but there is an international tradition to use English in variable names. Even if we're writing a small script, it may have a long life ahead. People from other countries may need to read it some time.
````

​````warn header="Reserved names"
There is a [list of reserved words](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Lexical_grammar#Keywords), which cannot be used as variable names because they are used by the language itself.

For example: `let`, `class`, `return`, and `function` are reserved.

The code below gives a syntax error:

​```js run no-beautify
let let = 5; // can't name a variable "let", error!
let return = 5; // also can't name it "return", error!
```
````

​````warn header="An assignment without `use strict`"

Normally, we need to define a variable before using it. But in the old times, it was technically possible to create a variable by a mere assignment of the value without using `let`. This still works now if we don't put `use strict` in our scripts to maintain compatibility with old scripts.

​```js run no-strict
// note: no "use strict" in this example

num = 5; // the variable "num" is created if it didn't exist

alert(num); // 5
```

This is a bad practice and would cause an error in strict mode:

```js
"use strict";

*!*
num = 5; // error: num is not defined
*/!*
```
````

## Constants

To declare a constant (unchanging) variable, use `const` instead of `let`:

​```js
const myBirthday = '18.04.1982';
```

Variables declared using `const` are called "constants". They cannot be reassigned. An attempt to do so would cause an error:

```js run
const myBirthday = '18.04.1982';

myBirthday = '01.01.2001'; // error, can't reassign the constant!
```

When a programmer is sure that a variable will never change, they can declare it with `const` to guarantee and clearly communicate that fact to everyone.


### Uppercase constants

There is a widespread practice to use constants as aliases for difficult-to-remember values that are known prior to execution.

Such constants are named using capital letters and underscores.

For instance, let's make constants for colors in so-called "web" (hexadecimal) format:

```js run
const COLOR_RED = "#F00";
const COLOR_GREEN = "#0F0";
const COLOR_BLUE = "#00F";
const COLOR_ORANGE = "#FF7F00";

// ...when we need to pick a color
let color = COLOR_ORANGE;
alert(color); // #FF7F00
```

Benefits:

- `COLOR_ORANGE` is much easier to remember than `"#FF7F00"`.
- It is much easier to mistype `"#FF7F00"` than `COLOR_ORANGE`.
- When reading the code, `COLOR_ORANGE` is much more meaningful than `#FF7F00`.

When should we use capitals for a constant and when should we name it normally? Let's make that clear.

Being a "constant" just means that a variable's value never changes. But there are constants that are known prior to execution (like a hexadecimal value for red) and there are constants that are *calculated* in run-time, during the execution, but do not change after their initial assignment.

For instance:
```js
const pageLoadTime = /* time taken by a webpage to load */;
```

The value of `pageLoadTime` is not known prior to the page load, so it's named normally. But it's still a constant because it doesn't change after assignment.

In other words, capital-named constants are only used as aliases for "hard-coded" values.  

## Name things right

Talking about variables, there's one more extremely important thing.

A variable name should have a clean, obvious meaning, describing the data that it stores.

Variable naming is one of the most important and complex skills in programming. A quick glance at variable names can reveal which code was written by a beginner versus an experienced developer.

In a real project, most of the time is spent modifying and extending an existing code base rather than writing something completely separate from scratch. When we return to some code after doing something else for a while, it's much easier to find information that is well-labeled. Or, in other words, when the variables have good names.

Please spend time thinking about the right name for a variable before declaring it. Doing so will repay you handsomely.

Some good-to-follow rules are:

- Use human-readable names like `userName` or `shoppingCart`.
- Stay away from abbreviations or short names like `a`, `b`, `c`, unless you really know what you're doing.
- Make names maximally descriptive and concise. Examples of bad names are `data` and `value`. Such names say nothing. It's only okay to use them if the context of the code makes it exceptionally obvious which data or value the variable is referencing.
- Agree on terms within your team and in your own mind. If a site visitor is called a "user" then we should name related variables `currentUser` or `newUser` instead of `currentVisitor` or `newManInTown`.

Sounds simple? Indeed it is, but creating descriptive and concise variable names in practice is not. Go for it.

```smart header="Reuse or create?"
And the last note. There are some lazy programmers who, instead of declaring new variables, tend to reuse existing ones.

As a result, their variables are like boxes into which people throw different things without changing their stickers. What's inside the box now? Who knows? We need to come closer and check.

Such programmers save a little bit on variable declaration but lose ten times more on debugging.

An extra variable is good, not evil.

Modern JavaScript minifiers and browsers optimize code well enough, so it won't create performance issues. Using different variables for different values can even help the engine optimize your code.
```

## Summary

We can declare variables to store data by using the `var`, `let`, or `const` keywords.

- `let` -- is a modern variable declaration.
- `var` -- is an old-school variable declaration. Normally we don't use it at all, but we'll cover subtle differences from `let` in the chapter <info:var>, just in case you need them.
- `const` -- is like `let`, but the value of the variable can't be changed.

Variables should be named in a way that allows us to easily understand what's inside them.
