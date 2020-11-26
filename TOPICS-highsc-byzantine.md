layout: true
.footer[
Stage at Bluewind: currently available topics
]

???
---

.left-column[
## Experiments on Fault Tolerance
]

.right-column[
### Background on Byzantine Fault (1/6)

Byzantine Fault relates to a special way for replicated processes
to exhibit faults.
]

???
---

.left-column[
## Experiments on Fault Tolerance
]

.right-column[
### Background on Byzantine Fault (2/6)

A replicated process is a process that is due to be executed in a set of
replicas, or nodes, all behaving in a consistent way.

The process can be anything useful like:

* saving some data in a memory
* performing calculations
* changing status for some physical machine
]

???
---

.left-column[
## Experiments on Fault Tolerance
]

.right-column[
### Background on Byzantine Fault (3/6)

In other words a replicated process is a process where given inputs
will result in determined outputs, and the same transition is performed
on a number of nodes coordinated by means of an exhange of messages.
]

???
---

.left-column[
## Experiments on Fault Tolerance
]

.right-column[
### Background on Byzantine Fault (4/6)

The reason for a replicated process to exist is that executing the
same transition on a set of different nodes enhance the robustness
of the system: in case of a failure of one of the nodes, well
designed protocols make it possible for the system to react and identify
the fault.
]

???
---

.left-column[
## Experiments on Fault Tolerance
]

.right-column[
### Background on Byzantine Fault (5/6)

Byzantine fault is a special situation in this scenario: it is
the situation where a certain amount of nodes start behaving in 
a totally arbitrary way, and yet (given some limitations) the system
is able to react and identify the fault.

This is what happens when the nodes are distributed at the edges of
an open network (the Internet) and subject to be taken under control
of adversary actors.

This is in other words the foundation of a Blockchain, or chain of trust.
]

???
---

.left-column[
## Experiments on Fault Tolerance
]

.right-column[
### Background on Byzantine Fault (6/6)

Papers describing tolerant algorithms as examples:

* [Miguel Castro et al.](http://pmg.csail.mit.edu/papers/osdi99.pdf)
* [Wembing Zaho et al.](https://academic.csuohio.edu/zhao_w/papers/zhaow-dasc07-bftdc.pdf)


]

???
---

.left-column[
## Experiments on Fault Tolerance
]


.right-column[
### Summary of the stage

The students will have a chance of:
 
 - studying the theory behind the topic
 - install, learn and play with the highly secure ADA programming language either on Linux or Windows hosts
 - learn the basics of Inter Process Communication (IPC) between separate applications
 - simulating a real set of replicated nodes as a Byzantine Fault system after having determined a protocol to be implemented

]

???
---

.left-column[
## Experiments on Fault Tolerance
]

.right-column[
### Some useful prerequisites (1/3)

Teachers have the opportunity to assist students during the lessons 
with topics and links suggested here.

]

???
---

.left-column[
## Experiments on Fault Tolerance
]

.right-column[
### Some useful prerequisites (2/3)

## ADA Programming language

![:scale 150px](assets/442px-Ada_Mascot_with_slogan.png)

* https://en.wikipedia.org/wiki/Ada_%28programming_language%29
* https://www.adaic.org/
* https://www.adacore.com/
* https://www.adacore.com/gems

]

???
---

.left-column[
## Experiments on Fault Tolerance
]

.right-column[
### Some useful prerequisites (3/3)

## Inter Process Communication in theory

* https://en.wikipedia.org/wiki/Inter-process_communication

]
???
---

.left-column[
## People
]

.right-column[
* *stefano.costa@bluewind.it*
* Partner and Director of Engineering
* https://www.bluewind.it

[Back to index](index.html)
]
