---
layout: post
---
- Manc JS: [Redux and Typing Deep Dive](http://mancjs.com/#redux-and-typing)
  - Talk 1: _[[Miller static analysis]]_, [Jack Wearden](https://www.jackwearden.co.uk/)
  - Talk 2: _[[Redux state container]]_, [Sam Marshall](https://twitter.com/sjmarshy)

- Subscribe: by the time you get to the action it's too late to intervene
- Monkeypatching is bad: not appropriate for a logger, as described in "a whole story" of why middleware is a good idea
  - see: redux website

Middleware is a func returning a func which we could use to store

- content of the logger is straightforward

- people use middleware for all sorts of things
- "time travel debugging" is showy name for going backward and forwards through state transitions
  - middleware collects states and triggers, goes back and forward through those states by hijacking how redux works
  - interesting way to __decouple__ effects and actions
    - including how the 'outside world' affects us
    - could extrapolate that out: there's a library called [redux-saga]() that does just that using generators
      - basically makes redux entirely functional
      - side effects return effect objects which describe the call you want to make
      - ...middleware takes care of how that operates

## Q&A

- `Q` (?)
  - documentation states it's read only, says "almost an annoying amount of times" not to mess around with state another way
  - it's recommended to use immutable JS to prevent people doing that
    - you get structural benefits
  - anything that goes on inside a reducer <strike>needs to return...</strike> should be entirely pure
    - need to create an entirely new object:
    - modify deep state without thinking "How am I going to make this into an entirely new object" each time
- `Q` what's the difference between async and ...(?)
  - separation of concerns: ...
  - ...doing a call to the net are about getting a value back from that
  - if you know actions are entirely about state, helps keep them in one place
  - entirely functional: interesting approach, all actions are just actions, just affect state
    - output description of what you want to happen
  - also might be useful to hunt down why your application is slow
    - if you don't have side effect-y things, you know you're looking in just one place
      - takes away that property, makes it easy to reason about ([[Blackboard]])

- `Q` would you recommend everyone use this?
  - there's a lot of boilerplate, starting difficulty
  - once that's done, doesn't take any more time from implementation POV
  - if you were making an application that counted up and down, wouldn't do it with redux
  - generally use it for web apps, generally complex enough to warrant some sort of state management
    - comes to a point of diminishing returns, but don't know where that point is

## Further reading

- [Building the UI -- pure-functionality and side-effects with redux](https://blog.hivejs.org/building-the-ui-2/)