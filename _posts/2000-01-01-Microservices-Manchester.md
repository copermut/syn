---
layout: post
---
## Talk 1. Microservices Past and Present

- Was _Past, Present, and Future_, we've had to cut off the future
  - for the future, see us at the bar
- London microservices user group
  - `Q` why running a group in London?
    - they have money down in London...

### Perfection

- you all have a mind world
  - particularly if you've a western mindset
- Plato's theory of ideal forms
  - _The real horse is the one in your imagination: that horse is the perfect one_
    - prior to this, people thought about concrete things
    - Plato's idea(l) of perfection has been punishing us ever since.
- Through history you can see people reaching for perfection

### Petra

- Indiana Jones: [Petra](https://en.wikipedia.org/wiki/Petra) was a city on one of the major Roman trade routes
- Carved city into the rock: Monolithic architecture
- Earthquake in the region cracked the aquaduct, destroyed the entire city

### Agile

- All columns in SQL table will be nullable eventually

### SOA

- SOA: [Service Oriented Architecture](https://en.wikipedia.org/wiki/Service-oriented_architecture)
- SOA optimises for _efficiency_
  - reuse not rebuilding

### The Cloud, or “The Cloud”

- Awful way to program
- Deploy to Amazon then your VM disappears
- The cloud is awful ∵ _CAP Theorem_
  - CAP Theorem is nice ∵ one of the few mathematical things you can prove in computing, and is regularly used

### CAP Theorem

- Consistency
- Availability
- Partition Tolerance
  - you need this - this just happens
- The choice before us is _either_ consistency or availability
- __There is no way of guaranteeing the order__
  - cannot know order will be consistent across 2 sides

### Failure of SOA

- CAP/“The Cloud” hates you
- Perfection is a lie

  😭 

- Not just cloud: data goes away, racks go away, data centres go away, ...

### “Micro Web Services”

- Resource oriented computing

### “Cloud Native” at _Netflix_

- Microservices are recognisably the same thing as what Netflix do now
  - all they wanted to do was scale horizontally
  - started to tread on each others toes
  - splitting app up
  - "communicate at runtime, not in code"
    - led them in same direction to those who cared about the cloud

### Containerisation

- Docker, Google core is essentially how microservices were born
  - Google enabled Docker through giving core Google tech
    - argument over if it really was...
- Lots of people had similar ideas at similar time
  - something had to come along: change ready architecture
- "[Microservices architecture]()"

### What is _microservices architecture_ ?

- _Isolation_ and _aspiration_
  - aspiration as in "_we will deploy microservices and the world will become better_"
- [microservices.io/patterns/microservices.html](http://microservices.io/patterns/microservices.html)
- [martinfowler.com/articles/microservices.html](http://martinfowler.com/articles/microservices.html)

### Architecture vs. design

- Not the same: via cardinality check
  - if asked month apart you will get a different design
  - seem to be limitless design decisions
    - ... but limited number of architectures
    - maybe it's dozens, but not limitless: ∴ must be some difference

### _Architecture is philosophy_

- Set of mental tools used to engage with problem
- Set of {biases, constraints, thinking tools}
  - all these things used to engage with problem
  - not the solution (that's design) it's the route to it
- Architecture, in software terms, is more a form of philo. than anything else

### Microservices philosophy

- Microservices is not a design
- When you come down to it, you're buying into distributed system
  - your system is going to explode into lots of pieces
- Kubernetes, Mesos, CoreOS, etc. are all platforms
  - some via _PaaS_, some containerisation, but all converging

### What you need

- Service discov, etc.
  - don't go looking at them, just get a platform
  - they will incorporate most of the things
- Please __don't build your own platform__
- {Cloud Foundry, Mesos, Kubernetes} are top 3
  - favourite: ... not really
    - nicest is Cloud Foundry(?) but also the most expensive

### DevOps

- DevOps is not a tool but a cultural shift
- Idea with microservices is to enable things to change
- Applications must move far faster, so reorient teams to enable that kind of behaviour

- DevOps hype cycle

- Continuous delivery
  - look into if you want to deliver microservices
  - massive overlap with DevOps

- probably need some kind of framework
  - enable lots of other things, [micro]service discovery etc
  - more you use, less you can change runtime you run with
  - using something that sits more at protocol level as standardisation will allow you to change much more easily

### Service communication

- One of things many people don't think about is communication
- Don't think about _services_/applications but data, communication
  - bits in middle far more interesting
  - just trap data flows: tend not to change over sys lifetime
    - language stacks, optimisation, etc.
  - think about service comms first

### Don't assume HTTP

- Can only do certain things, and it's ill-defined
- Probably where you're going to start, don't assume it's the end

### Want to know more?

- [@davidthecoder](https://twitter.com/davidthecoder)





## Talk 2. 7 [More] Deadly Sins of Microservices

- @danielbryantuk
  - Chief scientist at OpenCredo, SpectoLabs, DMs open
- original talk online at QCon NYC 2015
  - on InfoQ
  - updated to cover things seeing at the meoment

### What is a microservice?

- Applications that fit in your head
- Agile promised a lot, but delivered project management
- Next step will be __refinement of [business] process__

### Previously...

- Microservices are __not__ always a best fit
- __Evaluation__
  - new tech is great until it isn't
  - were often assembling a lot of things
    - lots of cargo culting, not understanding core principles
    - principles, practices, not understanding why got to that
- people are building "mini monoliths"
  - enterprise tech with an API is not a microservice

- __Always will be limited by slowest rate of change in the system__

- "Our _mode two_ apps are microservices"

### Evaluation: Situational awareness

- [Wardley mapping]()
  - Simon Wardley
  - value chain mapping
- Soundcloud did so to reduce time...
  - Phil Calcado: [How we ended up with microservices](http://philcalcado.com/2015/09/08/how_we_ended_up_with_microservices.html)

### "Communicate the tech vision"

- Assess per serive what the best tech is

- Lambda: "radical agility", slightly buzzwordy but think about things

- "we may not get REST right but this is what we think..."

### Evaluation: Fitness functions

- Microservices are first crack at fitness functions
- Auditability, configurability, ...
  - count access points, define ideal node on mind map...

- Matches "[your technical documentation should be a graph](https://neo4j.com/blog/technical-documentation-graph/)" by _Structr_ CEO

- Document why you chose things

- Dogmatic: "the spine model" breaks the deadlock
  - e.g. "I like Docker more" - what is valued
    - strong toolchain: Docker
    - security: Docker must run as root, maybe CoreOS more your thing
    - dogmatic about e.g. language, Java, toolchain, _IntelliJ_, etc etc

### Evaluation: It's easy to be tricked_

- Beware of bias and heuristics
  - vendors do this all the time, _bait and switch_
- [_Thinking Fast and Slow_](https://en.wikipedia.org/wiki/Thinking,_Fast_and_Slow) by his colleague Daniel Kahneman
  - find himself doing this, clients doing it

- RPC ([Remote procedure call](https://en.wikipedia.org/wiki/Remote_procedure_call)) is not the devil
- ESB ([Enterprise service bus ](https://en.wikipedia.org/wiki/Enterprise_service_bus)) is dead, long live the ESB
  - tire fire

### ESB is dead, long live the API gateway

- API gateways can morph into ESB if not careful
- Microservices can register for an interesting pattern
  - bidding systems: message comes in, can 'bid' for it

### The soft stuff is the hard stuff

- (People are the hard part)
- [Conway's law](https://en.wikipedia.org/wiki/Conway%27s_law) - systems you build will look a lot like communication structure

- _"We've decided to regorm our teams around squads, chapters and guilds"_
  - ah... you've cargo culted Spotify
  - DRIVE: "autonomy, purpose and mastery" by Daniel Pink
     - [danpink.com/drive-the-summaries/](http://www.danpink.com/drive-the-summaries/)
- tech is merely a symptom of the organisation

### Empathy: The hidden ingredient in good software development

- Craft Conference is almost too good, too many great talks
- Daniel Bryant - [_Empathy - The Hidden Ingredient of Good Software Development_](http://ustream.tv/recorded/86154111)
- systems thinking is really important

### Getting lazy with non-functional requirements

- Need to know some of these things up front

{ See: photo taken 8:28pm } <sup>`TODO:insert photo`</sup>

- It can be costly (or prohibitive) to adapt later
  - Microservices don't make this easier (sometimes more difficult)


### Wrath: blowing up when bad things happen

- _Relase It!_ is an amazing book, Michael Nygard, given to Netflix engineers
  - circuit breakers, bulk heads, ... and timeouts
  - _Chaos monkey_: asserting that you've made the right decisions
    - Simian army, if resilient, pull plug, will work
      - Google have a team dedicated to this: [_Meet Kripa Krishnan, Google's queen of chaos_](http://uk.businessinsider.com/profile-of-google-disaster-recovery-testing-boss-kripa-krishnan-2016-8)

- tech pain point: provide series of pain points, series of rollbacks in case they go wrong

- [devopstopologies.com](http://web.devopstopologies.com/)
- @matthewpskelton, @beerops, @sigje
- Google Site Reliability Engineering, Google's take
  - but don't cargo cult!
- Infrastructure as code, (OReilly)
  - "Continuous delivery book"

### DevOps: the "fullstack engineer" myth

- talk by Charity Majors: bombarded with people claiming "full stack"
  - @mipsytipsy, CraftConf 2016
  - Charity Majors - [DevOps for Developers: Building an Effective Ops Org](http://www.ustream.tv/recorded/86181845)

- bounded contexts: may have some duplication but _contextually relevant_
  - one model of microservices _breaks encapsulation_
- DDD: [Domain driven design](http://domainlanguage.com/ddd/)
  - entities; value objects; aggregates and roots

- Distributed model: worst of both worlds

- "Blue book and red book"
  - blue: (Evans) ?
  > Domain-Driven Design, by Eric Evans, provides a broad framework for making design decisions and a vocabulary for discussing domain design. It is a synthesis of widely accepted best practices along with the author’s own insights and experiences. Projects facing complex domains can use this framework to approach domain-driven design systematically.
  - red: (Vernon) _domain driven design_

### Context mapping

...

### Choose data stores appropriately

{ See: photo taken 8:41pm } <sup>`TODO:insert photo`</sup>

- Kafka, Neo4j, ...
- Use different things appropriately
  - social: graph
  - highly structured data: ...?
- seeing relational DBs kicked to kerb for Mongo etc
- seeing people using Cassanra wrong
- __Don't build a graph with RDBMS
  - use Neo4j, Titan etc

- shard data across instances, run processes on shards
  - parallelise things that otherwise couldn't be

- datagrids, e.g. Hazelcast

- local verification
- end-to-end testing
  - BDD style critical path
- test pyramid
  - don't want 'ice cream cone'

### Service virtualisation / API simulation

- virtualise request / response of services
  - unavailable

- been around for years tbh, but used more in enterprises than smaller dev shops

- Daniel has dzone article, think it's relevant to microservices

- Hoverfly

- Java isn't so good, has to spin up JVM [AWS solves this]

- deterministic testing, _chaos monkey_ middleware [e.g. drop every 5th package]

{ See: photo taken 8:47pm } <sup>`TODO:insert photo`</sup>

###### "Give me 6 hours to chop down a tree, and I will spend the first 4 sharpening the axe"

- basically business is insane and sometimes that's the right way to be but not usually so... chill

### Responsibilities

- Define responsibilities
- Architecture
  - less ivory towers, more _Sim City_ (Sam Newman)
- DevOps
  - not a free for all
  - no fullstack heroes

### Bonus: security

- _AppSec & Microservices_, Sam Newman (Thoughtworks), [OReilly](http://conferences.oreilly.com/software-architecture/engineering-business-us/public/schedule/detail/46889), [Sam's website](http://samnewman.io/talks/appsec-and-microservices/)
  - well worth watching if publishing microservices and want security
- [Docker and High Security Microservices: A Summary of Aaron Grattafiori's DockerCon 2016 Talk](https://www.infoq.com/news/2016/08/secure-docker-microservices)

### Fin

- [@danielbryantuk](https://twitter.com/danielbryantuk)
- [muservicesweekly.com](http://muservicesweekly.com/)

### Q&A

- No app scales indefinitely
- "Monolith in a box", then pull out microservices
- Scaling is not easy

- O'Reilly, _Building Microservices_ has the concepts not the code
  - purple "microservice architecture" after appreciated that one
  - rightward 5 are more general

- service boundaries and interfaces are the hardest things

- DDD book is how to build services