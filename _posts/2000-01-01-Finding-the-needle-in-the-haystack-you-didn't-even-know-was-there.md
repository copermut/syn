---
layout: post
---
# Sophia Ananiadou - Cafe Sci: Text Mining - Finding the needle in the haystack you didn't even know was there

- 28th July
- [Facebook event](https://www.facebook.com/events/508939032650720/)

- TDM is very interdisciplinary area
- First step is to find documents of interest (e.g. discussion of alcohol)
- Then zoom in, find what type of people, or other 'nuggets of information'
- Going a step further, building the applied systems for TDM
  - 'Finding a needle in haystack you didn't know was there' is actually finding unanticipated connections
  - e.g. medics looking at different associations in the brain, by chance can find lack of magnesium
    - something more associated than 'in the same sentence', inferred from unseen connections
    - powerful tool not just for scientists but people, gives a different understanding on things seemingly unassociated
  - can also use to think about the social web, social media.
  - lots of assoc'ns again, must define causality not only of disease but of social events
    - very difficult due to _Big Data_ (big textual data, unstructured)
      - structuring the meaning, semantics
    - going from big [text] data to _Big Semantics_, helps again when looking for associations
      - e.g. looking for diseases or events in social media
      - just having the data is just lots of volume, only semantics can start finding needles in the haystack we didn't know were there

## (Big) Semantics

- Sentences to give a general example: 3 years ago mined the NYT, for sociological study of social unrest
  - can mine blogs, Twitter, news {different newspapers, look at how they report differently}
- When reading sentence, we can read _grammar_: who, when, which circumstances
  - not only grammar (syntactic, whom, what, when), can automatically define entities (news about loss, killing, etc.)
  - automatically extracting this info and structuring
- Douglas Kell, interested in biological text: chemical cpd's, how these things relate, as a biochemist wants to read millions of documents but cannot as he's human
- Humans cannot read this big textual data but machines can!
- Systems methods: make sense out of things which are not necessarily related
  - e.g. if you're an archaeologist, may be lots of interesting things but use a query [keyword], gives back lots of noise
  - keywords don't necessarily have semantics: could be a disease: if you don't have this sort of association, cannot find the needle in the haystack as have to read millions of documents, have to go to places you never thought you'd have to be reading
  - can find _automatically_ grouped documents that cluster semantically
    - have to mine lots of data from different domains
    - e.g. may be something interdisciplinary, look in historical document
    - ways of doing _distant reading_
      - see: NYT, [What Is Distant Reading?](http://www.nytimes.com/2011/06/26/books/review/the-mechanic-muse-what-is-distant-reading.html?_r=0)
    - Look at how different sources [e.g. newspapers] report topics
      - e.g. how different newspapers framed strikes in Britain

## Discourse

- Current discourse is wider than Sophia's field, so makes it more broad than in internal communications
- Political discourse: argumentation (arguments)
  - Text mining picks up automatically the argumentation, discover that it's a discourse
  - Argumentation can lead reader to believe it's actually a good idea to go to war
    - use of words that suggests, displays facts in such a way to lead to an interpretation
  - not only to extract sentences and who does what to whom, but how we interpret events that we're extracting
  - what is the motivation, sentiment, positive/neg./neutral/lukewarm, and how different people talk about it
  - ...we can also find if something is contradictory, or contradicted in another source, or is negated, or if there's a lot of uncertainty
  - all of these things are found in data: _data never lie_
    - linguistic cues: may, perhaps, somewhere there's a negation, adjectives that cause a kind of negative or positive address
    - discourse political or scientific

## Applications

- Take the text 'raw', just words, and keep adding layers of meaning
- Have to do that in millions of pages and documents
  - "find me all organisations or people"
  - we express this in different ways: different words share meaning (isomorphisms)
- Look temporally, look at 'surges'
- Diversity data, in different languages
- Applications are creating meaningful search systems beyond just Google
  - creating queries which are meaningful responses, rather than just documents

## About

- NaCTeM created in 2004 initially just for biologists, who were interested in these tools
- Expanded to different domains
- Searching for _NaCTeM_, will find all the applications (for users not researchers)

---

( Break )

---

## Question session

- Can find intention of text, but cannot determine intention to mislead (∵ cannot know awareness of sources)

#### Q: lies vs. opinions?
  - Conflicting, negating, corroborating _sources_
  - same for science as politics
  - so much data (information) but we can actually find it: we can find if someone is contradicting themself

#### Q: a lot of data analytics is probabilistic (statistical) cf. logical
  - exactly: basically ranking from most to least probable, depends very much on common features used to come up with probabilities
  - using text, but also using other sources (non-textual)
    - can use different weights for certain figures, how many times person cited, and who has published etc.
    - don't just throw stuff, rank how probable it is

#### Q: Machine learning...
  - we use a lot of ML ([_confirmed everyone knows what that is_] - decomposing features into elements that make a child learn
  - in text mining, observing how people express something: ask a scientist what it means [supervised annotation]
  - looking at elements that can replicate automatically an understanding without specification
  - if we change a ML model, can very easily retrain
  - Machine translation was big in the 80s, lots of funding (lots of _European_ funding!), but had to write many rules, this is a different kind of understanding

#### Q: could you contrast with IBM Watson?
  - What IBM did at the time used a huge database, like a brute force analysis, extracting named entity relations, but a lot of whatthey have done was to create a mega database ("we don't have the capacity...")
  - Scale, but also specificity, we call 'sublanguages' harking back to early days of computational linguistics
    - Levels of analysis: lexicon, dictionary, semantics, but most important part [interested in the 80s] was specific domains
    - e.g. clinical, biological, news
    - Frames of knowledge was specified by queries
    - Meteorological translation in Canada (bilingual)

#### Q: how generic could this be made?
  - it's hard: "[domain adaptation](https://en.wikipedia.org/wiki/Domain_adaptation)"
  - early efforts without this had very bad performance
  - tuning, and that's something we do a lot

#### Q: in terms of tools, what sort of tools would you use for a 100 page document?
  - depends... needs and requirements
- ...Q: pattern would emerge, wouldn't know what you were looking for
  - you'd know what level: build a database for instance, topics
  - you have to think about what you want to find, putting tools together

#### Q: what languages?
  - A: doesn't matter, C, C++, Python, Java (use a lot of Java, but initially C)
  - very early days used Prolog
  - PL on lower level of your ability - doesn't matter, whatever makes you comfortable

#### Q: these domains, e.g. cultural, used both to exclude and include people in particular domain. If I came from outside I could learn or they would use that to manipulate my understanding, and what would you do - try and make peace?
  - what you're saying is, if we can use TDM to exclude people... it's not a tool of doing that... it's a method to find information to eliminate or include
  - not responsible for that, just providing information and just provide or exclude
  - not a fight but a choice, systems are making recommendations

#### Q: saying in 80s working on inference systems, lot of knowledge capture, is that still a large part?
  - we do, when training ML, to build systems that are precise and respond to users' requirements
  - we use ontologies a lot, and other resources, dictionaries [databases] sources of wisdom from domain experts
  - first step: ontologies mostly manually constructed, then we talk to researchers, interact with them to improve tools
  - first step of unsupervised knowledge

#### Q: Why biological sciences particularly receptive?
  - semantic stuff that Google bag of words
  - "vector", "cut", mean different things
  - didn't ask how they do it: HTML marked up with special things that tell text miners for instance parts of speech
  - _REFINE_: Representing Evidence for Interacting Network Elements, let us make networks and mark up with evidence
  - comes down to efficiency
  - system reducing the workload, and looking at systematic links to start making assumptions, mine past systematically

#### Q: if we don't have time to read, why write? Why not just enter data in a systematic way?
  - data could be interpreted in different ways is one thing
  - if you just put in data, words, you need to be able to extract 'how you generate a story'
    - man eats dog, or dog eats man. needs orientation [direction] in text to generate what kind of narrative to create
    - how narratives created is important. massive db still need to know... can generate an enormous amount of possible stories

#### Q: [from me] institutional repositories are limited, and if insight from aforementioned 'big datasets', 'big semantics' comes from full corpora then aren't we missing out on inter/national texts? Casey Bergman just left the university, and IIRC did one of the very few studies of full body of literature in Pubmed Central, noted that few people did this. Full texts are inaccessible due to OA concerns, publishers restrictions on mining - do you find this?
  - open to whom, other scientists, text miners can mine them
  - UK is in a very good position
  - conscientious effort to allow the right to mine - just institutional repositories
    - can derive, but cannot share to friends in Netherlands
    - must share within UK
    - intense fight continues
    - NaCTeM were lobbying for full text
    - e.g. mining clinical trials, most important things were missing
    - cannot develop drugs because don't have information on clinical trials
    - companies do have them but costs millions in deals with pharma and publishers

#### Q: when a researcher comes to you and says 'do this search', what do you go back with?
  - it depends on needs, can provide systems or big databases, or even a combination of tools that can run on the documents they're interested in
  - very rarely we come and give a script: it's difficult to run a text mining process, most of the time people are interested in the output
  - most time consuming part is the learning process, building resources with the knowledge of the scientist
  - end result, the data associated to generate something

#### Q: Copyright, AMD IP was on legs, notebooks walked out the door. Only have public knowledge, what's above the guy's necks. I may let on knowledge into the public domain.
  - Ontologies and public domain is one source. In chemistry and other areas, people are mining labs' notebooks, depending if they're available, if they're machine readable. If hand-written [most probably] other systems transmit to a form that can be text mined [NaCTeM don't do that]

#### Q: Working with people to go into their understanding: their mind: to learn from them

#### Q: Shannon entropy can give additional signals alongside linguistic signals. Do you do anything similar to that?
  - Not really
  - Douglas Kell: yes you do, [mutual information](https://en.wikipedia.org/wiki/Mutual_information)

## Questions (unasked)

- Can we look at search as an isomorphism (or automorphism) problem?
- What is the status of text mining in the academic literature,  online there's a lot of noise about "right to read is right to mine"
- Frames of knowledge specified by queries: what if rather than 'sub'-languages looked at general attentional systems...

## Resources

- NYT, [What Is Distant Reading?](http://www.nytimes.com/2011/06/26/books/review/the-mechanic-muse-what-is-distant-reading.html?_r=0)

## Footnotes, deviations and linkbacks

- [[Attentional verticals]], concept written up following the talk relating to direction and dimensions of mental attention, considered as an inference process using terminology from marketing/business management ("[[verticals]]").