---
layout: post
---
- Trying to develop a graph database-modelled website (for research-assistive purposes)
  - ...without outmoded metaphors, see: [[Skeuomorphic computing environment (discussion)]]
- model flow of traffic through concepts on a Wiki to say something semantic? not controversial that pageview = attention (metrics get a bad rap)
  - pageviews tied to user give a path of interest
  - Not trying to market or sell: find imaginative patterns
- model attentional processes: capture reader's imaginative approach rather than that of the writer (see: [[verticals - tech note|verticals#technology-design-notes]] and interpretation as "[[imaginative verticals]]")
- capturing learning process isn't exploitative/surveilled, afforded [[differential privacy]]
  - very small pages such that the (dominant) path of users exerts a structuring effect
    - pages linked: semantically, temporally (git wiki), imaginatively (user vectors)
    - pages sideloaded 1-link deep: external resources too?
    - modelled on Pascal's section divisions in the _Pensées_ <sup>`TODO:terminology`</sup>
      - see: description of _liasses_ ('bundles') in [[Permutation graphs and copermutations]]
  - classify paths rather than aggregate (i.e. using dominant reader path), rearranging the presented path according to some measure of similarity to known path classifications as reader progresses?
    - similar to recommender systems: key is how you instantiate a new user (_naïve locus_)
    - assumes fine level of control: seems unfeasible: _unless_ procedure itself is on a graph
      - i.e. web page connections are structured by aforementioned dominant paths through concept graph relationships and overlaid permutation graph variety
- what would a graph cut signify in this context? <sup>`TODO:clarify`</sup>
  - "low level computer vision problems (_early vision_)" ([via](https://en.wikipedia.org/wiki/Graph_cuts_in_computer_vision)) <sup>`TODO:explore`</sup>
    - see: [[Graph cut approximation]]

- - -

> If you simply do a brain dump of your process behind the project, you’ll do a pretty good job of satisfying one user story:

> Other developers who are googling around because they’re trying something similar will get a head start on solving the problems we’ve solved.

> Write what you know, right? But whoever asked you to write the post probably has other user stories in mind too.

🔰  Anna Schneider, [_The engineering blog meta-post_](https://medium.com/@aschn/the-engineering-blog-meta-post-7ffe43aa4060#.x4oxxa1ct)