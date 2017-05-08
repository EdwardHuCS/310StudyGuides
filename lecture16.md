# Lecture 16 Design Patterns
__design patterns, what are, what role do they play in design process, classic patterns like MVC, anti patterns, bad smell, what is a bad smell and how does it relate to anti patterns, refactoring, what  are key things during refactoring process__

## Design Patterns
- provide solutions to reocurring problems
- balance sets of opposing concerns
- abstraction above the level of a single component
- means of documentation
- support construction of software with defined properties

## Design Patterns are..
- a way of reusing abstract knowledge about a problem and its solution
- a description of the problem and essence of its solution
- abstract enough to be reused

## Architectural vs Design Patterns
Architectural style is large scale system organization
Design Pattern is localized small scale solutions
## Example of Patterns
- Creational
    - Abstract Factory
- Structural
    - Adapter
    - Bridge
    - Facade
    - Proxy
- Behavorial
-   Observer
-   Mediator
## Model View Controller
Objective: Separation between information, presentation, user interaction
Description: When a model object value changes, a notificaiton is sent to view and to the controller. When handling input from user, event is sent to controller.

## Observer Pattern
### Description:
The Observer pattern lets you vary subjects and observers independently. You can reuse subjects without reusing their observers, and vice versa. It lets you add observers without modifying the subject or other observers.
### Problem Description:
A common side-effect of partitioning a system into a collection of cooperating classes is the need to maintain consistency between related objects. You don't want to achieve consistency by making the classes tightly coupled, because that reduces their reusability.
### Consequences:
- Abstract coupling between subject and observer
- support for broadcast communication
- unexpected updates

## Mediator Pattern
### Description
Object-oriented design encourages the distribution of behavior among objects. Such distribution can result in an object structure with many connections between objects; in the worst case, every object ends up knowing about every other.

### Applicability:
- a set of objects communicate in well defined but complex ways
- reusing an object is difficult because it refers to and communicates with many other objects
- a behavior that's distributed between serveral classes but sould be customizable without a lot of subclassing
### Consequences:
- limits subclassing; localizes behavior that otherwise would be distributed among several objects
- decouples colleagues, promotes loose coupling between colleagues
- simplifies object protocols, makes many to many into one to many between mediator and colleagues
- abstracts how objects cooperate
- centralizes control, but mediator can become monlith that's hard to control
## Facade Pattern
### Description:
- A subsystem has multiple classes, each having functionality needed by other subsystems
- Desire to reduce coupling between this subsystem and others
- Define a single class (*facade* class) to be the high level interface to the subsystem
- all external users of the subsystem will make calls through the facade class, the entry point
### Applicability:
- use when subsystem does not need to know about clients
### Consequences: 
- clients are shielded from the low level classes in subsystem
- simplifies the subsystem usage with a simple interface
## Proxy Pattern
### Description: 
- The proxy pattern is used when you need to represent a complex with a simpler one.
### Applicability: 
- If creation of object is expensive, its creation can be postponed till the very need arises and till then, a simple object can represent it. This simple object is called the “Proxy” for the complex object
## Adapter
### Description:
- Convert the interface of a class into another interface clients expect. Adapter lets classes work together that couldn't otherwise because of incompatible interfaces.

### Applicability:
- you want to use an existing class, and its interface does not match the one you need.
- you want to create a reusable class that cooperates with unrelated or unforeseen classes, that is, classes that don't necessarily have compatible interfaces.
- (object adapter only) you need to use several existing subclasses, but it's impractical to adapt their interface by subclassing every one. An object adapter can adapt the interface of its parent class.
### Consequences:
- adapts Adaptee to Target by committing to a concrete Adapter class. As a consequence, a class adapter won't work when we want to adapt a class and all its subclasses.
- lets Adapter override some of Adaptee's behavior, since Adapter is a subclass of Adaptee.
- introduces only one object, and no additional pointer indirection is needed to get to the adaptee.
## Bridge Pattern
### Description:
- Separate an interface from implementation in a way that different implementations could be substituted
- Similar purpose as the Adapter pattern, except not constrained by existing components
    - Adapter is for filling the gap between different interfaces
    - Bridge is for filling the gap between interface and implementation
### Applicability:
- use when client needs to make a method call with different implementations to similar objects
### Consequences: 
- client is shielded from concrete implementations, client only sees high-level interface
- Different concrete implementations could be substituted, or refined independently from the high-level interface
- Lower level interfaces could also be refined, as long as high-level interface is not changed
## Anti Patterns
- God Object
- Sphagetti code 
- copy and paste programming
## Refactoring Process
1. examine design artifacts
2. search for bad smells
3. evaluate design decisions that lead to bad smells
4. refactor code to improve design



























