## Blackboard (architecture)

See: [Wiki](https://en.wikipedia.org/wiki/Blackboard_(design_pattern))

## Blackboard (system)

> Blackboard systems were popular before the AI Winter and, along with most symbolic AI models, fell out of fashion during that period. Along with other models it was realised that initial successes on toy problems did not scale well to real problems on the available computers of the time. __Most problems using blackboards are inherently NP-hard__, so resist tractable solution by any algorithm in the large size limit. During the same period, statistical pattern recognition became dominant, most notably via simple Hidden Markov Models outperforming symbolic approaches such as Hearsay-II in the domain of speech recognition.

> A blackboard-system application consists of three major components
  1. The software specialist modules, which are called knowledge sources (KSs). Like the human experts at a blackboard, each knowledge source provides specific expertise needed by the application.
  2. The blackboard, a shared repository of problems, partial solutions, suggestions, and contributed information. The blackboard can be thought of as a dynamic "library" of contributions to the current problem that have been recently "published" by other knowledge sources.
  3. The control shell, which controls the flow of problem-solving activity in the system. Just as the eager human specialists need a moderator to prevent them from trampling each other in a mad dash to grab the chalk, KSs need a mechanism to organize their use in the most effective and coherent fashion. In a blackboard system, this is provided by the control shell.