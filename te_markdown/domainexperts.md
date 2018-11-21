---
layout: page
title: Test Your Domain
permalink: /te_markdown/domainexperts/
---

User acceptance testing is a collaborative activity involving domain experts, testers, and developers. Therefore, effective and efficient tools have to address the different needs of each of these roles. In particular, they must not expose technical aspects that would shut out less tech-savvy users that nevertheless need to participate in the process. 
For example, tools embedded into heavy-weight integrated development environments expose far too many unneeded features and capabilities that distract from the task at hand, and unnecessarily steepen the learning curve. The same is true for using existing general-purpose programming languages to express test specifications and test cases, that were not build with these use cases in mind.

**Test-Editor-Web** is designed specifically so that domain experts are empowered to write testable specifications, without requiring deep technical knowledge.

To this end, the languages used to express test specifications and test cases are tailored specifically towards their respective use cases. They have been purpose-built from scratch, as opposed to extending an existing programming language, so that no unneeded and potentially confusing concepts are exposed, allowing to express test specification and test cases in a clear and concise manner. 

At the same time, the languages are *customizable*, so that concepts from the application domain and the software under test can be defined and given semantics to be used directly in tests, making them natural to read and understand for domain experts.

~~~
* Create a hero named "Sancho"
Component: MyHeroes
- Enter "Sancho" into <Name>
- Press <Add>
~~~

Furthermore, the user interface has been kept clear and reduced to the essential features that help users with their tasks. Domain experts, testers, and developers can use filters to further focus their view with respect to their respective tasks and expertise.

## Learn More

* [Test Your Application](/te_markdown/testdrivers): Read about Test-Editor-Web's capabilities to target different application technologies.


## Try it for Yourself

* Write your first test specification in 5 minutes.
* Write your first test case in 5 minutes.
