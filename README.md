# Anglebrackets Review

![Desk at Anglebrackets](https://cloud.githubusercontent.com/assets/12703711/11003403/1df31516-8467-11e5-9db2-5b6f831a09a2.jpg)

![MGM Grand](https://cloud.githubusercontent.com/assets/12703711/11026517/e14514f2-865f-11e5-9f97-dd784a47895c.jpg)

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

http://tinyurl.com/Angular2Jumpstart

* Use the features of the future, today! :arrow_right: Transpiling
* Traceur from Google, TypeScript from Microsoft, Babel from Some Guy
  * https://google.github.io/traceur-compiler/demo/repl.html#
  * http://www.typescriptlang.org/Playground
  * https://babeljs.io/repl/
* Angular2 uses TS, but you don't have to use it
 * Transpiling lets you use the latest and greatest but still support older browsers
 * ES6 features are a lot of C#-ish features
  * Arrow syntax for anonymous methods
* Full-time documentation team for the first time: angular.io
  * Still in progress
* No more factory vs. provider vs. service
  * It's a component (reusable object)
* Big changes but necessary
  * Different syntax
  * One way binding
  * ng-for instead of ng-repeat
  * Pipes instead of filters
  * Routing by annotation
  * No more ng-show/hide :arrow_right: [hidden] = "method"
<figure>
![Slide -- What's in a Component Class?](https://cloud.githubusercontent.com/assets/12703711/11004075/f8ebf680-846a-11e5-92b9-02bb6e66098a.png)
<figcaption>from https://docs.google.com/presentation/d/1uLlx-pidFzXpFF3VDbhva-qAhDvQMipE9rHMg7fd5js/edit#slide=id.ge42647124_0_45</figcaption>
</figure>

## How to go on the cyber-offence
[Troy Hunt](http://troyhunt.com)

* Know how to break things yourself before someone else does
* http://twitter.com/needadebitcard
* Hackers only need to get it right once, we have to get it right every time
* https://www.google.com/webhp?sourceid=chrome-instant&ion=1&espv=2&ie=UTF-8#q=inurl%3Aftp%20inurl%3Aweb.config
* Proxy your phone through Fiddler, see what data shows up in plaintext
  * Major bank in AU that turned off TLS validation
* Dangerous to assume that users will use software as intended
* Hashing - don't use Base64, MD5, or encrypt 
  * http://hashcat.net/oclhashcat/
  * Billions of attempts possible per second
  * Use hashing algorithm to make it hardeer
    * https://www.owasp.org/index.php/Password_Storage_Cheat_Sheet
* Teenagers hacking major companies with easy to use tools
  * Talktalk via SQL injection
* Content Security Policy (CSP) - prevent unwanted scripts from loading
  * https://developer.mozilla.org/en-US/docs/Web/Security/CSP
  * https://report-uri.io/ - report violations
* Wifi pineapple - https://www.wifipineapple.com/
  * Spoofs public wifi SSID, can see unencrypted traffic
  * Use VPN (Freedome)
* strict-transport-security
 * https://www.owasp.org/index.php/HTTP_Strict_Transport_Security
 * Prevent subsequent requests from going through unencrypted
 * Trust on First Use - https://hstspreload.appspot.com/

## What does an open source Microsoft Web Platform look like?
Keynote by [Scott Hanselman](http://www.hanselman.com/blog/)

* Microsoft has a very mixed/confusing record on open source
 * Shared source
 * Reference source
   * http://www.sourceof.net
 * Github Microsoft repositories: 20% non-Microsoft contributors
   * Everything still goes through Microsoft QA process, they stand behind it
 * Regular .NET framework and .NET core
   * Only things that make sense in .NET core
 * ASP.NET 5 is unified reboot, runs on .NET 4.6
 * Dot Net Execution (DNX) builds against both environments
   * Warns if feature / library won't work in both
   * Can do ifdef if you want
* Past focus has been on dev productivity, making a run at top 10
  * https://www.techempower.com/benchmarks/#section=data-r10&hw=peak&test=plaintext
  * https://github.com/aspnet/benchmarks
* Omnisharp, intellisense everywhere
  * http://www.omnisharp.net/
  * Runs as node server on local machine, MacOS, Linux, Windows
* Windows selling Office, Windows, Azure
* Reality is a hybrid of devices, OSes
* Different ways of consuming framework
 * Well done: wait till VS, get at nuget.org
 * Medium well: CTPs, Betas 
 * Medium: CI drops, feed on myget.org
 * Medium-rare: build from source, grabbing from dev branches
 * Rare: Build from source on feature branches
 * Blue: build from source from third party forks
* Help out with documentation: https://docs.asp.net
* Become a social developer: getinvolvedintech.com
 * Microsoft learning from good stuff and bad stuff in open source projects

## ASP.NET 5

Javier Lozano - lzno.tk/aspnet5-unleashed

* Out of band releases now embraced, not just VS releases
* Opting in for features, don't have to shut features off
* Dependency injection outside of the box
* POCO controller, follow conventions
* TagHelpers

## Improving the quality of existing code

Steve Smith - http://ardalis.com/

* Software rots :arrow_right: technical debt
  * Low quality code and shortcuts cost you in the long run
  * If you do nothing, it gets worse, and replacing it entirely has enormous risk and cost
  * Refactor as you go
* Preventive maintenance
* Don't have seperate refactor tasks, make things a little better
 * Follow Boy Scouts mantra of leaving things in better condition than when you got there
 * "You don't need permission to practice basic hygiene when you write software"
 * Characterization test
  * What does the code do now?
  * Unit test if possible to confirm existing behavior is preserved
* Duplication in logic calls for abstraction
* Duplication in process calls for automation
* Favor privileges over role checks
* Visual Studio Code Clones - https://msdn.microsoft.com/en-us/library/hh205279.aspx
* Look at cyclomatic complexity
  * Try to keep under 10, not always a problem
* Regions are a code smell - so complex you have to hide parts of it
* Instead of null, have static intance of "not found" object
* Structure solution so dependencies flow towards core (onion architecture)
* Develop skills and tools to write good code more quickly
  * Muscle memory for code smells
  * New is glue
* http://deviq.com/

## Node.js and Angular.js Security

Sam Artioli - github.com/samartioli/webapp-security

* Always sanitize data
* Authorize API
* eval() is evil
* requireSafe, nsp, and retire in workflow
* 'use strict'
* Use CSPs
* Never run as root - use docker
* CHrome blocks XSS in URL, but Firefox doesn't 
* DOS attacks - watch out for regexes that will kill server
* Preventing CSRF
  * CSURF
  * Don't use eval(), especially on user-generated data
* Node Security Project - https://nodesecurity.io/
* https://liftsecurity.io/
* Shrinkwrap locks down dependencies, pjup asks you about each ugprade
* lusca, helmet
* Removed X-Powered-By

## Productivity improvements in VS2015

Robert Green - Tech Evangelist, Microsoft
https://channel9.msdn.com/Niners/rogreen

* Sign in to VS account to persist settings across computers
* Better touch support, pinch to zoom
* Save window layouts, switch using hotkeys, saves to profile
* Lightbulbs, ctrl-. to do refactors
* Warnings with variable names conflicting
* TODO in JS, Intellisense for JS methods
* Code Analyzers made possible by Roslyn, Microsoft and third parties, write yuor own
* Debug :arrow_right: Show diagnostics tools
* Pin variables, filter using LINQ in Immediate or Watch windows
* Create Unit Tests
  * Supports different frameworks
  * Intellitest
* Codecracker analyzer

test
