# Anglebrackets Review

## Zen of Architecture, Juval Lowy

* One day workshop all about "The Method" - IDesign's Method of architecting software
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
