TddInsideOut
============


This repo is to keep the source code from the _SPA event workshop_ on 4th of September 2013 (https://spa275.eventbrite.co.uk/)

**Creating Objects from Inside Out with TDD and Functional Style**


The goal of this session is to use functional programming practices in TDD to grow objects. Or put in another way to explore the borders between functional and OO programming.

The inspiration of this session came from doing "Test Driven Development As If You Mean It" (http://www.infoq.com/presentations/TDD-as-if-You-Meant-It)" at a code retreat.

I really enjoyed the challenge, so I come up with a slightly different set of rules that reflect more closely my daily work on TDD.

First the usual TDD rules apply:

1) Write exactly one new test. It should be the smallest test which seems to point in the direction of a solution. Run the test to make sure it fails

2) Make the test from (1) pass by writing the least amount of implementation code you can in a STATIC method without side effects (no access to anything but the parameters and no output to anything but the function result)

3) Once the tests are green you can (must) refactor to improve the design. 

4) Repeat the process by writing another test (go back to step 1).



During refactoring check all the code for these 3 goals:
 - reduce complexity (less calls or less parameters).
 - reduce any form of duplication. 
 - renaming for clarification.
At the end of every refactoring you should have archived at least one of the above, otherwise you must rollback it.


Moreover refactoring steps should follow these rules:

 - (a) You can extract logic to new static pure methods.
 - (b) You can extract variables and primitives to new immutable objects (Value Object) with only getters and no setters. VO can contains either VO or primitive types but not Entities (see next rule).
 - (c) You can create mutable-state objects (Entity) by combining together existing static methods and local variables. Entities cannot expose directly their inner status, that is they cannot have getters. They can have method that return result of calculation involving their inner state. 
 - (d) Try to use composition over inheritance.
 - (e) Never pass or return null. Use NullObject or TellDontAsk pattern.

In any case each refactoring step should be small and quick. Check often that tests are still green. Remember you are not allowed to do refactoring with red tests!
See also: http://jonjagger.blogspot.co.uk/2009/06/average-time-to-green-game.html



The goal of the exercise is to explore the border between OO and Functional paradigm.
The resulting design should emerge by the need of minimize the size and number of artefacts needed, rather than following the abstractions imagined by participants.
At the end there should remain very few or none static methods.


Participants will pair to complete each TDD kata using Cyber Dojo: http://www.cyber-dojo.com/





