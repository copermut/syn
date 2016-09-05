---
layout: post
---
- at _MancJS_ meetup this week, discussed with [Slice](https://twitter.com/slice_beans) (lead dev at _Retrofuzz_) how, half-intentionally [as thought experiment] I'm observing out-of-memory errors and finding effects equivalent to network latency.
  - _i.e._ "negative design patterns" (?) that give pause to consider edge cases usually only encountered due to network latency [given cloud storage], but actually arise from _local_ out-of-memory when avoiding cloud services
- There's an isomorphism that I thought I could see when studying network [[interconnects]] (/[[permutation interconnects]]), not a "metaphor" so much as something with information theoretic basis.
  - See: [[Liouville's theorem]]

- meeting today with my research advisor clarified some thoughts that lead [_post-hoc_] to [[Liouville's theorem]], on information theoretic microstates ("the microcanonical ensemble" of _instantaneous_ microstate), Linux general mutability, out-of-memory/latency isomorphism

- Twitter is oddly like talking out loud to yourself sometimes: earlier today I tweeted that "I'd never received a satisfactory answer" to my question on _Chemistry StackExchange_, [How can a protein folding transition state have zero lifetime](http://chemistry.stackexchange.com/questions/16792/how-can-a-protein-folding-transition-state-have-zero-lifetime)
  - the answer appeared later today in the book I came across via [total, ridiculously chance encounter] on Quora:
    - Quora: [What are some good free web scrapers / scraping techniques](https://www.quora.com/What-are-some-good-free-web-scrapers-scraping-techniques) (always worth checking back in with the scraper community)
      - curious ∵ Google Spaces is API-less ∴ communication there is siloed (∴ deliberate restrictions imposed in community design, perhaps unlike _Wave_)

- The protein folding transition state is an instantaneous microstate [see 2.2 of Marhev 09]
  - when drafts are lost from offline storage in the event of a memory error, it reminds me of Pascal's Wager.
  - if something is known then it can be stated in a given space and time
    - as biography of Pascal concludes (_spoiler alert_)  

    > "The one thing that no one can mistake is that he made his unalterable choice, paid his price, won his reward."

- The problem with Linux is, it pulls back the curtain, and reveals that information annotation is not so much an action as a property of the data which we waste our efforts in hand-holding.
  - If something can be known, it can be formatted as such
  - 'reactive programming or bust' style of approach, '_The Reasoned Schemer_'
    - see: logical code examples from _The Reasoned Schemer_, [pkrumins/the-reasoned-schemer](https://github.com/pkrumins/the-reasoned-schemer)

- Continuation of this train of thought leads to a separate concept, of spaces not networks, and of a semi-permeable interface of [intrinsically] incomplete [mutual?] information
  - spaces provide/impart structure (niches & [[verticals]], algorithm|data structure morphism discussed at #MatBio2016 conference) <sup>`TODO:find notes`</sup>
    - NB: unsure if note on this are online yet? Git Wiki is unindexed, tag as possibly in existence

- see: (cont.) [[Usufructuary spaces]]
  - Need to decide what form of morphism and/or set relation this represents <sup>`TODO:categorise`</sup>

## Examples

- An example of memory-latency isomorphism can be seen in browser caching of Git Wiki entries
  - if you type `[[an example page]]` then click through in a new tab, leave some content then use the browser back/forward functions the state of the unsaved draft will remain.
  - this seems trivial, and perhaps something thought up flippantly, but _[[Service workers|service worker]]_ will bring this behaviour to entire websites: facilitating their preferential protection from cache clearance on systems in a way that will begin to blur the boundaries of transient sites and persistent apps (indeed some local apps serve little more than a chromeless web interface).
    - NB these are known as [[progressive web apps]]
      - see: Google Spaces, [Assemblages](https://spaces.google.com/space/7481281592871412467)
        - first pair of items:
          1. First headless and chromeless browsers, recently physical web, & next: headless web, [The Headless Web - Tales of a Developer Advocate](https://paul.kinlan.me/the-headless-web/)
          2. [NYLUG Presents: Luke Wagner -on- WebAssembly: A New Compiler Target For The Web](https://www.youtube.com/watch?v=RByPdCN1RQ4)

- - -

- Structuring knowledge is essential, in fact without it new information is a progressive pollutant.
  - expanded on in [[consolidation]]

- - -

Appeared in Cover & Thomas's _Elements of Information Theory text ([notes here](https://github.com/spin-systems/statistical-reads/wiki/Cover-and-Thomas-(2013,-2e)-Elements-of-Information-Theory))

![](https://raw.githubusercontent.com/lmmx/shots/d99beca49491622dab7b948f7356841f6ea4aafb/2016/Aug/comp-comm-isomerism-found.png)