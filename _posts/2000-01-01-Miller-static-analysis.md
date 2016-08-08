---
layout: post
---
- Manc JS: [Redux and Typing Deep Dive](http://mancjs.com/#redux-and-typing)
  - Talk 1: _[[Miller static analysis]]_, [Jack Wearden](https://www.jackwearden.co.uk/)
  - Talk 2: _[[Redux state container]]_, [Sam Marshall](https://twitter.com/sjmarshy)

- Jack Wearden on [Miller](https://github.com/NotBobTheBuilder/miller)

> Miller is a static analysis tool for JavaScript.

> It infers the types of expressions and looks for contradictions where it can.

> Take a look at the test scripts for some examples of what kinds of type errors can be checked at compile time.

> ### Usage

>  `sbt assembly` will generate a JAR that you can run.

> `./miller.jar` filename.js will run miller on a file, alternatively just `miller.jar` will open a REPL (close with ctrl-D)

- Miller named after Arthur (playwright) not George
- Jean Claude Van $Lambda$

...

- as programmers we're most effective when thinking about domain meanings
  - thinking about errors etc not helpful, hence FP
- "FP composes smaller components", takes well-defined behaviour, lets other libraries etc. handle implementation
  - compose big sections
- in JS "we know what types are intuitively", not statically checked
  - certain behaviours defined in different types and in terms of other types

### Let's go back to the land of types

- gif from [_Italian Spiderman_](https://en.wikipedia.org/wiki/Italian_Spiderman)
- instructions don't have meaning on their own
  - in assembly land, there's just stuff and pointers to stuff
    - pointers to stuff are just stuff
    - just 1s and 0s, "quite terrifying"
- more Zen-like, in level of the domain
  - no type checking in assembly, no unit testing (well... maybe in NASA)
- __order of instructions in assembly doesn't matter__ (!)

- "type checkers reject incorrect programs"
  - incorrect "at the plumbing level"
    - no domain meaning: 

- fork in C works by giving process ID to call
  - if 0, you're the fork, if not you're the parent (with the PID)
    - you've been "teleported"
    - parent process kills the child `</3`

> If pid is -1, _sig_ shall send kill to all processes: __kills machine__

- good types <- feed -> good design <- feed -> good error handling
  - "imagine a circle"
    - (torus?)
- when you have a really good set of type designs you have to model your problem domain
  - "really, what entity am I handling, what circumstances is this process running?"

#### Service example

- _i.e._ demon etc.
- can't stop a stopped service / start a started service
- better to die upfront and let programmer investigate cf. meander along in error case
  - (e.g. 'already started' error)
- services have states
- Scala: implicit param: says "need to find something of this type"
  - if can't find it, unproved assertion stops compilation
  - `// error: cCannot prove that Started =:= Stopped.`
  - JS would treat as runtime thing, Scala says impossible

- The [[Curry-Howard isomorphism]] (Curry-Howard correspondence) is the direct relationship between __computer programs__ and __mathematical proofs 

- Now saying: types model problem domain, can only work with data in ways that are meaningful, not meaningless

- Agda is superset of Haskell
  - binary tree, sum of tree [i.e. leaves], flip a tree is "put in other order, do same for children"
  - extreme of "how do we only write code that always works"
  - weird Unicode script: not a 3 bar `=` sign, not a `<`
  - __have to use emacs to edit__

1. Define the data at your endpoints
2. Design around uncertainty _monadically_
3. Compose larger systems together from smaller, defensively designed ones
  - e.g. small JS modules saying "I was expecting a user ID here"
  - makes easier to test, reason about, and clearer expectations
  - also less unexpected outcomes will happen
  - projects with stateless-y things, e.g. traditional DOM
    - all of a sudden, break of 2 seemingly-not-connected elements fail
    - circumstances rarely obvious
    - logging everything makes it even harder to see wood from the trees

#### <strike>Do not</strike> fear the monad

- take something where there's uncertainty about state, take it away (abstract it)
- some traits of types can be certain, others less so
  - type of array elements
  - callback param types  
  vs.
  - size of array
  - when a calback will be called
  
- separate implementation behaviour from domain-level meaning
  - easier to write stuff that won't "trip over own shoelaces"
  - worse in JS: may just give undef and you never notice
