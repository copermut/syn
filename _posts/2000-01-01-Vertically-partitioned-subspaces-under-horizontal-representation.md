---
layout: post
---
![](https://raw.githubusercontent.com/lmmx/shots/master/2016/Aug/pure-twitter-gold.png)

- Chance find: while looking for [entity-attribute-value model](https://en.wikipedia.org/wiki/Entity%E2%80%93attribute%E2%80%93value_model) databases (also known as _vertical databases_) (which I'm familiar with through R ['wide and long'](http://seananderson.ca/2013/10/19/reshape.html) data frames)

- Paper: Cui _et al._ (2010) [Exploring Correlated Subspaces for Efficient Query Processing in Sparse Databases](https://www.computer.org/csdl/trans/tk/2010/02/ttk2010020219-abs.html), author-hosted [PDF](http://net.pku.edu.cn/~cuibin/Papers/2010tkde.pdf)

  - discusses high-dimensionality sparse data sets
  - [with references to ecommerce removed]:

    > As we introduced previously, the pure horizontal or
vertical representation may yield unsatisfactory performance
in sparse databases. Therefore, we propose a new
representation called _HoVer_, which can effectively exploit
the characteristics of sparse data sets, such as __sparsity
and dimension correlation__. We aim at achieving good
space and time performance for storing and querying
high-dimensional sparse data sets.
    >
    > Although the dimensionality of sparse data sets could be
very high, up to thousands, __a single data object typically has
only a few active dimensions, and similar objects have a
better chance to share similar active dimensions. A closer
inspection of many [...] sparse data sets shows
that typical [...] data sets have a wide variety of
items which can be organized into categories and the
categories themselves are hierarchically grouped__; items that
belong to a common category are likely to have common
attributes, while those within the same subcategory are
likely to have more common attributes. The RDF data (Wilkinson _et al._ 2003)
also shows that the attributes of similar subjects tend to be
defined together. This motivates us to find certain subspaces
which are shared by similar data groups, and to split
the full space into some lower-dimensional subspaces.

      - Ref: K. Wilkinson, C. Sayers, H.A. Kuno, and D. Reynolds, “Efficient
RDF Storage and Retrieval in Jena2,” Proc. Int’l Workshop Semantic
Web and Databases (SWDB), pp. 131-150, 2003. ([pdf](http://www.hpl.hp.com/techreports/2003/HPL-2003-266.pdf))