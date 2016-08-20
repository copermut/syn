---
layout: post
---
- [x] [How does Keras compare to other Deep Learning frameworks like Tensor Flow, Theano, or Torch?](https://www.quora.com/How-does-Keras-compare-to-other-Deep-Learning-frameworks-like-Tensor-Flow-Theano-or-Torch)
  - Theano and TensorFlow are very similar as Tensorflow reuses many key ideas laid out in Theano. Both are languages for defining abstract general purpose comp graphs 
      - Not quite ‘DL frameworks’ and can be used for more than DL! 

  - Keras is an actual DL framework: well-designed API that allows you to build DL models by joining high-level building blocks 
      - Runs on top of TensorFlow/Theano, so no performance cost to using Keras cf. “lower level” frameworks 
  - Keras = better UX

- - -

- [x] [Why should I care about Keras if I am already using Tensor Flow?](https://www.quora.com/Why-should-I-care-about-Keras-if-I-am-already-using-Tensor-Flow)

      - Simpler, quicker building/training models in TF, no performance cost ∵ models still run by same engine  
      
> Last week I came across [these two scripts that implement XOR in Keras and TF](https://gist.github.com/cburgdorf/e2fb46e5ad61ed7b9a29029c5cc30134), put together as a “Hello World” by someone trying to learn about neural networks. It sums it all: the Keras version is much easier to read, understand, and write. There is less code overhead and cognitive overhead to working with Keras.  

  - Though: more complicated models, “starker productivity benefits” of Keras  

  - Shines for models heavily weight sharing, for composites of multiple models, multi-task models etc.   

    - E.g. [this reimplementation of the paper "Deep compositional captioning" [1] in ~30 lines of Keras](https://gist.github.com/fchollet/0ecc151189b997fd4400bc2fecf2489f) (written in 15 mins)   

      - [1] [Describing Novel Object Categories without Paired Training Data](https://arxiv.org/abs/1511.05284)  

- A pure TF implementation would spread over multiple files, 100s of lines of codes, and “quite a challenge” to do at all   

- - -

- [ ] [What are some important engineering and design decisions you made in creating Keras?](https://www.quora.com/What-are-some-important-engineering-and-design-decisions-you-made-in-creating-Keras)
- [x] [What is your favorite machine learning algorithm?](https://www.quora.com/What-is-your-favorite-machine-learning-algorithm-2)

  - Matrix factorisation: simple, beautiful, dim. Reduction, “and dimensionality reduction is the essence of cognition” 
    - However, fundamentally shallow, deep NNs will outperform if any kind of supervision labels are available

- - -

- [ ] [Why has Keras been so successful lately at Kaggle competitions?](https://www.quora.com/Why-has-Keras-been-so-successful-lately-at-Kaggle-competitions)
- [ ] [What is the best way to get started with Deep Learning using Keras?](https://www.quora.com/What-is-the-best-way-to-get-started-with-Deep-Learning-using-Keras)
- [ ] [Do you recommend using Theano or Tensor Flow as Keras' backend?](https://www.quora.com/Do-you-recommend-using-Theano-or-Tensor-Flow-as-Keras-backend)

- - -

- [x] [What is the state of distributed learning (multi-GPU and across multiple hosts) in Keras and what are the future plans?](https://www.quora.com/What-is-the-state-of-distributed-learning-multi-GPU-and-across-multiple-hosts-in-Keras-and-what-are-the-future-plans)

  - It’s currently possible to do both model-level parallelism (sending diffferent ops in a single net to different devices) and data level parallelism (replicating one model onto different devices processing different batches in parallel, then mergin results) 
    - Only with the TF backend 

  - In future: unified, user-friendly API to handle both forms of parallelism in Theano/TF with a single codebase…  
    - For time being, with TF backend, model parallelism is ~ trivial, data paralellism fairly easy 
    - Must know how to do it in TF (not easy...) 

>  [Here's a blueprint of how to do it](https://gist.github.com/fchollet/2c9b029f505d94e6b8cd7f8a5e244a4e), to be used in conjunction with [this tutorial](https://www.tensorflow.org/versions/r0.10/how_tos/distributed/index.html).

- - -
- [ ] [Why did you decide to implement Keras?](https://www.quora.com/Why-did-you-decide-to-implement-Keras)

- - -

- [x] [Deep Learning is mostly implemented on big data. What are your thoughts on using it on data with limited samples but high dimensions like fMRI?](https://www.quora.com/Deep-Learning-is-mostly-implemented-on-big-data-What-are-your-thoughts-on-using-it-on-data-with-limited-samples-but-high-dimensions-like-fMRI)

  - DL is fundamentally about automatic learning features from raw data, in a setup where __the raw data is assumed noisy and highly unstructured__.
  - Shallow ML was "like feeding impure gold nuggets into a machine and getting pure gold out" but DL is more like feeding raw dirt... you need a lot more dirt"
    - the higher the intrinsic dimensionality of your data, the more examples needed to densely sample its manifold

  - some cases where it's possile to learn from "a few" samples but highly dependent on nature of problem and definition of "few"

    - e.g. can train classsifier on 100s or 1000s of samples, best wchieved by fine tuning a net that was previouslt trained n a large dataset of similar images
      - see: [Building powerful image classification models using very little data](https://blog.keras.io/building-powerful-image-classification-models-using-very-little-data.html)

  - could work on fMRI, but better ask an expert on it.

- - -

- [ ] [Why is it important to democratize machine learning?](https://www.quora.com/Why-is-it-important-to-democratize-machine-learning)
- [ ] [Do you ever hire undergraduate interns? Is so what academic background do you like them to have?](https://www.quora.com/Do-you-ever-hire-undergraduate-interns-Is-so-what-academic-background-do-you-like-them-to-have)
- [ ] [What are your long-term career goals?](https://www.quora.com/What-are-your-long-term-career-goals)
- [ ] [What are your goals in the long term?](https://www.quora.com/What-are-your-goals-in-the-long-term?no_redirect=1)
- [ ] [Would an AI that creates algorithms and writes software to solve complex problems be an efficient replacement for programmers?](https://www.quora.com/Would-an-AI-that-creates-algorithms-and-writes-software-to-solve-complex-problems-be-an-efficient-replacement-for-programmers)
- [ ] [Can Keras be used for shallow/standard machine learning?](https://www.quora.com/Can-Keras-be-used-for-shallow-standard-machine-learning)

- - -

- [x] [What advice would you give to people studying ML/DL from MOOCs (Udacity, Coursera, edx, MIT Opencourseware) or from books in their own time?](https://www.quora.com/What-advice-would-you-give-to-people-studying-ML-DL-from-MOOCs-Udacity-Coursera-edx-MIT-Opencourseware-or-from-books-in-their-own-time)

  - The best way to study ML is along the lines of: 
    - Get a precise understanding of key lgos, try reimplementing ourself in Numpy (convnet, MLP, LSTM, … ) 
      - Get familiar with practical applications, look at examples on Keras, modifying them, adapting to new data 
      - Get a feel for research and real-world with Kaggle competitions 
      - “At last, you can start reading theoretical books and research apers to develop a more abstract and mathematical understanding of the processes you have been practicing” 

  - “Overall much easier to grok the theoretical side of ML when already familiar with its practice cf. other way around. A sound understandng comes from confrontation with real-world problems, not confrontation with MOOCs and books.”

- - -

- [x] [What advice would you give to someone starting a PhD in machine learning on how to achieve strong results?](https://www.quora.com/What-advice-would-you-give-to-someone-starting-a-PhD-in-machine-learning-on-how-to-achieve-strong-results)

  - “Identify an important, under-appreciated problem with high potential impact 
  - Ensure problem an be broken up into smaller intermediate steps that are valuable in themselves, so you can have useful results to show even if you fail to solve the large problem at hand, i.e. make sure ou have a fallback plan. 
  - The easiest way to achieve “a large impact” is to author the first couple papers in a new subfield of deep learning that is just about to take off. [GANs](https://www.quora.com/What-are-Generative-Adversarial-Networks) are a good example of this happening in recent memory.

- - -

- [ ] [How can the open source community help with developing Keras more?](https://www.quora.com/How-can-the-open-source-community-help-with-developing-Keras-more)
- [ ] [What's more realistic in the future: a really good understanding how to systematically design neural networks or NNs that build themselves?](https://www.quora.com/Whats-more-realistic-in-the-future-a-really-good-understanding-how-to-systematically-design-neural-networks-or-NNs-that-build-themselves)
- [ ] [What is Wysp?](https://www.quora.com/What-is-Wysp)
- [ ] [Is Neon support planned in Keras?](https://www.quora.com/Is-Neon-support-planned-in-Keras)
- [ ] [Have you ever considered building Deep Learning models in Haskell?](https://www.quora.com/Have-you-ever-considered-building-Deep-Learning-models-in-Haskell)
- [ ] [Starting from scratch, and knowing python and a little numpy, how long does it take for someone to get comfortable with Keras and Theano?](https://www.quora.com/Starting-from-scratch-and-knowing-python-and-a-little-numpy-how-long-does-it-take-for-someone-to-get-comfortable-with-Keras-and-Theano)
- [ ] [Is the work on DeepMath continuing at Google?](https://www.quora.com/Is-the-work-on-DeepMath-continuing-at-Google)
 
- - -

- [ ] [When do you expect to finish your book?](https://www.quora.com/When-do-you-expect-to-finish-your-book)

  - Q1 2017, in stores end of 2017

- - -

- [ ] [Does using Batch Normalization reduce the capacity of a deep neural network?](https://www.quora.com/Does-using-Batch-Normalization-reduce-the-capacity-of-a-deep-neural-network)
- [ ] [Is the integration of pre-trained model an important direction forward for Keras/Democratizing AI?](https://www.quora.com/Is-the-integration-of-pre-trained-model-an-important-direction-forward-for-Keras-Democratizing-AI)