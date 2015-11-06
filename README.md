# Anglebrackets Review

![Desk at Anglebrackets](https://cloud.githubusercontent.com/assets/12703711/11003403/1df31516-8467-11e5-9db2-5b6f831a09a2.jpg)

## Zen of Architecture, Juval Lowy

* One day workshop all about "The Method" - [IDesign](http://idesign.net/)'s Method of architecting software
* Juval Lowy, "Software Legend", one of the authors of Programming WCF
* "For the beginning architect there are many options, for the Master architect there are few"
* Functional decomposition is bad, avoid "flow chart" design
* A -> B -> C
  * Very hard to separate
  * A usually has to know about B which knows about C
  * Hard to do error handling, rollback scenarios
* Example of building a house: Kitchen, Bathroom, Bedroom
  * Building architect wouldn't do one and then go back and add others
* "Most architects are quacks" "Inmates are running the asylum"
  * First Law of Thermodynamics: Can't add value without sweating
  * 2% problem / Dunning-Kruger effect
  * Just because something doesn't work doesn't mean people will stop doing it :arrow_right: alchemy
* The Method: decompose based on volatility
* Do not code to requirements, don't blame the customer for changing requirements
  * Your fault for creating a design that can't adapt
  * Do not code to requirements, find the core
* What are the most volatile areas?
  * Resources can be volatile (database, file system)
  * Third-party notifications can be volatile
  * Varies by over time with one customer and between different customers
* Rarely map areas of volatility to services

## Angular2 in 60ish minutes / ES6 today
[Dan Wahlin](https://weblogs.asp.net/dwahlin)

* Use the features of the future, today! :arrow_right: Transpiling
* Traceur from Google, TypeScript from Microsoft, Babel from Some Guy
  * https://google.github.io/traceur-compiler/demo/repl.html#
  * http://www.typescriptlang.org/Playground
  * https://babeljs.io/repl/
