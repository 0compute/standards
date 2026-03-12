# Standards

The first, last, and only standard.

Standards are the work of the Apostles transpiled to Machine.

Whatever the format, the machine understands what the Apostle said, no matter
how they said it: hand/type writing, books, papers, source, mailing lists, audio
and video.

Hard engineering standards are a prerequisite to quality code.

Case study: [The Fuck You NVIDIA
Standard](./apostles/torvalds/FUN-1.case-study.md).

## Lineage of Ideas

> If I have seen further it is by standing on the shoulders of giants.
>
> — Isaac Newton, letter to Robert Hooke, 5 February 1676

The canon records the lineage of ideas that form the foundation of modern
computation and systems engineering.

The lineage of ideas ultimately converges on a single purpose: the protection
and empowerment of **Humanz**.

The structure below is not a chronology of history but a **logical lineage**:
the chain of ideas required to move from fundamental theory to systems used by
**Humanz**.

Solid edges represent the **source-to-User lineage** of systems.

Dashed edges represent **intellectual dependency**.

``` mermaid
graph TD

Lovelace["Lovelace — symbolic machines"]

Turing["Turing — computation"]
Church["Church — lambda calculus"]
Shannon["Shannon — information theory"]

vonNeumann["von Neumann — stored-program architecture"]

Thompson["Thompson — Unix philosophy"]
KR["Kernighan & Ritchie — C and Unix practice"]
McIlroy["McIlroy — composable tools"]
Pike["Pike — systems elegance"]

Backus["Backus — programming languages"]
Hopper["Hopper — compilers"]

Dijkstra["Dijkstra — rigor"]
Hoare["Hoare — correctness"]
Lamport["Lamport — distributed reasoning"]

Parnas["Parnas — modularity"]
Liskov["Liskov — abstraction"]
Milner["Milner — type systems"]

Codd["Codd — relational data"]

CerfKahn["Cerf & Kahn — internetworking"]
Postel["Postel — robustness"]

StallmanTorvalds["Stallman / Torvalds — open systems"]

Dolstra["Dolstra — reproducible builds"]

Merkle["Merkle — cryptographic proofs"]

Humanz["Humanz"]

Lovelace --> Turing
Church -.-> Turing
Shannon -.-> Turing

Turing --> vonNeumann

vonNeumann --> Thompson
Thompson --> KR
KR --> McIlroy
McIlroy --> Pike

Backus -.-> KR
Hopper -.-> KR

KR --> StallmanTorvalds

Parnas -.-> Pike
Liskov -.-> Pike
Milner -.-> Pike

Dijkstra -.-> Lamport
Hoare -.-> Lamport

Codd -.-> CerfKahn
Postel -.-> CerfKahn

CerfKahn --> StallmanTorvalds

Pike --> Dolstra
StallmanTorvalds --> Dolstra

Merkle -.-> Dolstra
Dolstra --> Humanz
```

**We stand** on the shoulders of giants.

## The Apostles

### Ada Lovelace

Saw the machine before it existed. Working from Babbage's plans, she understood
that a general-purpose engine could manipulate symbols, not just numbers —
writing the first algorithm a century before hardware could run it. She named
the possibility.

### Alan Turing

Defined what it means to compute. The Universal Machine — a theoretical device
that could simulate any other machine given a description of it — is the
conceptual bedrock of every computer ever built. He also proved the limits:
problems no machine can solve, no matter how powerful.

### Alonzo Church

Independently arrived at the same limits through lambda calculus: a formal
system of function abstraction and application that is computationally
equivalent to the Turing machine. Every functional programming language descends
from it.

### Barbara Liskov

Formalised substitutability. The Liskov Substitution Principle states that
objects of a subtype must behave as their supertype promises. It is the
precision behind every sane inheritance hierarchy and the foundation of
type-safe abstraction.

### Brian Kernighan & Dennis Ritchie

Wrote the practice. C gave the Unix philosophy a portable implementation
language; *The C Programming Language* set the standard for technical writing in
engineering. They made the machine speakable.

### C.A.R. Hoare

Gave us the tools to reason about programs before running them. Hoare logic —
preconditions, postconditions, invariants — is the foundation of formal
verification and the basis for every assertion framework. Also: Quicksort.

### Claude Shannon

Quantified information itself. His 1948 paper established that information can
be measured in bits, that noise is the enemy, and that redundancy is the weapon
against noise. Without information theory there is no compression, no error
correction, no reliable communication.

### David Parnas

Named modularity. His 1972 paper on information hiding established that systems
should be decomposed by what they conceal, not by what they do — that the
interface is the contract, and the implementation is nobody else's business.

### Doug McIlroy

Invented the pipe. The idea that the output of one program is the input of the
next — and that programs should do one thing well — is the architectural DNA of
every shell, every data pipeline, every composable system built since.

### Edgar Codd

Invented the relational model. Twelve rules, first-order predicate logic applied
to data, and SQL as its surface language. Every database that enforces
referential integrity is running on his ideas.

### Edsger Dijkstra

Enforced rigour. He killed the `goto`, demanded formal proofs of correctness,
and wrote with a precision that treated sloppy thinking as a moral failing. If
your code is structured, Dijkstra is why.

### Eelco Dolstra

Solved reproducibility. Nix — his doctoral research made real — treats software
builds as pure functions: same inputs, guaranteed same outputs, forever.
Bit-for-bit reproducibility is the end of "works on my machine."

### Grace Hopper

Built the first compiler and then convinced a sceptical world it was possible.
She understood that programming languages are for humans, and that the machine's
job is translation. She coined the term "bug" from an actual moth in a relay.

### John Backus

Proved that humans need not write machine code. BNF notation — invented to
describe ALGOL — became the universal language for defining programming
languages. Every parser, every compiler, every grammar descends from his
formalism.

### John von Neumann

Turned theory into architecture. The stored-program computer — where
instructions and data share the same memory — is his design. Every
general-purpose machine since 1945 is a von Neumann machine.

### Jon Postel

Wrote the robustness principle: be conservative in what you send, liberal in
what you accept. He authored or co-authored the RFCs for TCP, UDP, SMTP, DNS,
and FTP. The internet's tolerance for heterogeneous implementations is his
design decision.

### Ken Thompson

Built Unix. Not just an operating system but a philosophy: small tools, plain
text, composable pieces, a kernel that trusts the programmer. Unix is the
substrate on which the modern world runs.

### Leslie Lamport

Made distributed systems thinkable. Lamport clocks, the Paxos consensus
algorithm, and TLA+ are his instruments for reasoning about systems where there
is no shared clock and no single source of truth. Distributed computing without
Lamport is guesswork.

### Ralph Merkle

Invented the cryptographic proof of integrity. The Merkle tree — a hash of
hashes forming a tamper-evident structure — underlies Git commits, Bitcoin
blocks, certificate transparency logs, and every system that must prove it has
not been altered.

### Richard Stallman & Linus Torvalds

Made the machine open. Stallman's GNU project and GPL licence established that
software freedom is a political position; Torvalds's Linux kernel provided the
free Unix the movement needed. Together they built the commons that the modern
internet runs on.

### Rob Pike

Distilled elegance. From Plan 9 to Go, Pike pushed relentlessly toward
simplicity: fewer concepts, cleaner interfaces, less ceremony. His rules of
programming are the shortest path from complexity to clarity.

### Robin Milner

Gave type systems their rigour. The Hindley–Milner type inference algorithm, the
ML family of languages, and the pi-calculus for reasoning about concurrent
processes are his contributions. If a language catches your error before you run
it, Milner is behind it.

### Vint Cerf & Bob Kahn

Invented TCP/IP. The protocol suite that connects every networked device on
earth — packet switching, addressing, routing, error recovery — is their
architecture. The internet is their machine.

