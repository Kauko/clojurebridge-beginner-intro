#Welcome to ClojureBridge!

##What did we do yesterday?
- Terminal, command line, console
    -  Just a way to run programs without a graphical user interface (GUI)
    -  Basically just makes your life easier :)
- Git
    - "Version control tool". We'll talk about these later today!
    - Basically, a way to share code
- Java
    - Java is one of the most used programming languages
    - Clojure runs "on top of" Java
- Leiningen
    - The first thing that is actually related to Clojure
    - A tool to "start Clojure", or "run your project"
- Light Table, Nightcode
    - Code editors
    - Both do *exactly* the same thing
    - Code editors are just text editors, that are designed to help you write code
    - You could write Clojure with notepad!
    - Maybe even something like MS Word, but I don't know why you would!


##What is programming?
**Code** = set of instructions

**Programming language** = Something the computer and humans understand

![Musical notes](https://upload.wikimedia.org/wikipedia/commons/thumb/8/8e/Chopin_Prelude_7.svg/2041px-Chopin_Prelude_7.svg.png)

Musical notes are not natural language, but we can read and understand them.

Notes have a set of rules they follow (*syntax*) to convey a meaning (*semantics*)

###The computer doesn't understand us if we're not clear

**Let's eat grandma!**

**Let's eat, grandma!**

We understand what is meant in either case, but the computer wouldn't.

We understand the *semantics*, even if the *syntax* is different.

A computer doesn't!

###Let's imagine your friend has a dog that can do all kinds of tricks.

![](https://s-media-cache-ak0.pinimg.com/236x/09/b4/a1/09b4a157e2ce4f0acc76a52d0f69c467.jpg)

You get a dog of your own.

Turns out, your dog is actually really dumb.

![](http://orig14.deviantart.net/7503/f/2011/111/0/b/stupid_dog_by_jejator-d3eixpa.jpg)

Your dog doesn't do any tricks if you don't train it first!

You have to give it very explicit commands, or it will do something wrong without realising it.

![](http://www.funnyzozo.com/wp-content/uploads/2014/06/01975_117-576x377.jpg)

Again, you have to make sure to use the *correct syntax* so that your dog can understand.

##Building blocks of programs

```
Microwave food recipe
1. Remove wrapping
2. Put food in microwave
3. Turn on microwave for 3 minutes
4. Wait for 3 minutes
5. Remove food from microwave
6. Eat!
```
This is actually a program. All of these steps are *functions*.

Function is a piece of code, that does something.

Let's rewrite some functions to take *parameters!*

```
...
3. Turn on microwave for N minutes
4. Wait for N minutes
...
```
`N` is now a *parameter* or an *argument* to the function.

In truth, some of our functions are calling other functions..

```
2. Put food in microwave
    a. Open door
    b. Place food in microwave
    c. Close door
```

Sometimes we don't even really care about the implementation details.

```
3. Turn on microwave for 3 minutes
    a. Turn on the thingy
    b. Expose the food to microwave radiation in the electromagnetic spectrum
    c. Induce polar molecules in the food to rotate and produce thermal energy
``` 

**You do not need to know how everything works!**

## Towards actual code

```
5 + 10
10x + 16
```

This may look familiar to some of you:

```
var result = 5 + 10;

function doSomething(x) {
    return 10 * x + 16;
}

var anotherResult = doSomething(7);
```

With Clojure, this would look something like this

```
(def result (+ 5 10))

(defn doSomething [x]
    (+ (* 10 x) 16))
    
(def anotherResult (doSomething 7));
```