# Lecture 15 Architectural Styles
__Lecture 15:advanced design, architectural styles, 10 different variations of lunar lander using different styles, what is an architectural style vs design patterns, why, what are common architectural styles__
1. What is an architectural style
    - A set of constraints you put on your development to elicit desirable properties from your software architecture
2. Why do we have architectural styles
    - Design reuse, code reuse, understandability of sys org
    - interoperatibilty, style specific analyses, visualizations
# Difference between architectural style and design patterns
Architectural style is large scale system organization
Design Pattern is localized small scale solutions
# Common styles
1. Object Oriented Style
    - Components are objects
    - Connectors are messages and method invocations
    - objects are responsbile for their internal representation, hidden from other objects
    - __Pro__: infinite maleability of object internals, system decomp into sets of interacting agents
    - __Con__: side effects in object method invocations
2. Layered 
    - each layer acts as a server (service provider) to layers above
    - acts as a client (consumer) to layers below
    - __Pro__: increasing abstraction levels, evolvability, changes in a layer only affect up and down, different implementations of layers are allowed as long as interface is the same
    - __Con__: not universally applicable, not performant, determining correct abstraction level
3. Client Server
    - components are clients and servers
    - connectors are RPC based network interaction protocols
    - clients know server's identity, server does not know clients
4. Batch Sequential
    - separate programs are executed in order, data is passed as aggregate from one program to next
    - connectors: human hand, carrying tapes between programs
5. Batch Sequential
6. Pipe Filter
    - components are filters, transform input data streams to output data streams
    - connectors are pipes, conduits for data streams
    - style invariants: filters are independent, no knowledge of other filters
    - __Pros__: system behavior is a succession of component behaviors, concurrency, ease of filter addition, replacement, reuse
    - __Cons__: batch organization of processing, interactive apps, bounded by lowest data transmission filter
7. Blackboard
    - components: central store (blackboard), components operating on blackboard
    - connectors: blackboard
    - __Pros__: only one connector that everybody uses, new commponents can be easily added
    - __Cons__: blackboard becomes bottleneck with too many clients
8. Publish Subscribe
    - components: publishers, subscribers
    - connectors: typically a network protocol
    - highly efficient one way dissemination of info, low coupling
9. Event Based
    - components: independent, concurrent event generators / consumers
    - connectors: event buses
    - Events are sent over event bus, components communicate with event buses, not each other
10. Peer to Peer
    - state and behavior distributed among peers
    - components: peers, having own state and control thread
    - connectors: network protocols