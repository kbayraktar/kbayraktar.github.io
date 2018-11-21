---
layout: page
title: Write Your First Test Specification in Five Minutes
permalink: /te_markdown/heroes-create-spec/
---

- Estimated reading time: 3 minutes
- Audience: [Curious party], Noob, Somewhat experienced, Experienced, Expert

Test specifications are expectations that the software under test should satisfy.

In a **test first** environment, they are written before the actual feature is implemented.

There are only minimal rules as to how these specifications should be written. It is however good practice to follow a given-when-then pattern to group details.

Each test specification should describe a non trivial, focused domain expectation.

Each specification will eventually be implemented by a test case. A test specification is covered through non failing test cases that implement this specification.

## How do I write specifications?

The software under test is an implementation of the heroes tutorial of the angular framework (see).

[How do I get a running test-editor-instance?](local-setup)

![screencast: create hero specification](/images/tutorial/tutorial.heroes.create.spec.gif "screencast: create hero specification")

Given you have a running instance of the test-editor-web, the following (trivial) steps suffice:

- navigate to (or create) the folder to hold the specification
- create a new file with the extension '.tsl' (e.g. CreateHero.tsl)
- Write the specification name into the opened editor, prefixing it with '#' (e.g. '# CreateHero'). Currently you need to type a new line before the '#'.
- Write each aspect of the specification (specification steps):
```
        * Given: I am on the heroes page
        * When: I create a hero named "Sancho"
        * Then: The hero should be the last one of the list
```

That's it. The first specification is in place.

If you want to know how to implement and execute a test case covering this implementation, please move on (link)

If you want to know more about how specifications can and should be written, click here (link)

## Some reflections

The specification is expected to be written by a domain expert before the implementation is begun. Its function is manifold.

* It works as an intention carrying document that helps the tester and developer to understand the requirement of the requested feature.
* It provides a clear communication artifact for the domain expert, the tester and the developer that is used to clarify and adjust expectations.
* It is incomplete until implemented by test-cases that work as acceptance criteria for the feature

It is quite common to have the specification change (slightly) when actually implementing the feature. Even under change, the specification must
remain the guiding principle for the tests.

For the domain expert to write down specifications without having to think about the tooling itself, the specification is supposed to require
minimal knowledge about the test-editor-web itself and the language to be used to describe specifications.

Specifications contain specification steps. Specification steps start a line with '*'. They can be multiline and hold UTF-8 characters. Implementations of a specification must make sure to implement each specification step. 
