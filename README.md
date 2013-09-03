TddInsideOut
============


This repo is to keep the source code from the _SPA event workshop_ on 4th of September 2013 (https://spa275.eventbrite.co.uk/)

**Creating Objects from Inside Out with TDD and Functional Style**


The goal of this session is to use functional programming practices in TDD to grow objects. Or put in another way to explore the borders between functional and OO programming.

During this practical session, participants will try "Test Driven Development As If You Mean It" with a slightly different set of rules. 


1) Write exactly one new test. It should be the smallest test which seems to point in the direction of a solution. Run the test to make sure it fails

2) Make the test from (1) pass by writing the least amount of implementation code you can in a STATIC method without side effects (no access to anything but the parameters and no output to anything but the function result)

3) Once the tests are green you can (must) refactor to improve the design. 

4) Repeat the process by writing another test (go back to step 1).


During refactoring check all the code for these 3 goals:
 - reduce complexity (less calls or less parameters)
 - reduce any form of duplication. 
 - renaming for clarification.


Refactoring should follow these rules:
a. You can extract logic to new static pure methods.
b. You can extract variables and primitives to new immutable objects (Value Object) with only getters and no setters. VO can contains other VO but not Entities.
c. You can create mutable objects (Entity) by combining together existing static methods and local variables in a new mutable entity. Entities cannot expose directly their inner status, that is they cannot have getters. They can have method that return result of calculation involving their inner state. 
d. Try to use composition over inheritance.
e. Never pass or return null. Use NullObject pattern or TellDontCall





At the end there should remain very few or none static methods.

The goal of the exercise is to explore the border between OO and Functional paradigm.
The resulting design should emerge by the need of minimize the size and number of artefacts needed, rather than following the abstractions imagined by participants.


Participants will pair to complete each TDD kata using Cyber Dojo in their language of choice http://www.cyber-dojo.com/


.



