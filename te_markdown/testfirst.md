---
layout: page
title: Test First
permalink: /te_markdown/testfirst/
---

In agile development, *domain experts* write user stories with explicit *acceptance criteria* that are used to guide *developers* during implementation, and to decide when the story is completed. To avoid delays due to misunderstandings, acceptance criteria should be rigidly defined to leave no room for ambiguities, and facilitate continuous testing from inception to completion, to drive incremental development.

**Test-Editor-Web** fosters the collaboration of domain experts, testers, and developers by providing each group with the right tool for their job:

| Domain experts use the *test specification language* (TSL) to formalize desired system behaviors, using their own, domain-specific terminology, and thus requiring no technical expertise. Test specifications function as communication basis between domain experts, testers, and developers. | Testers implement test specifications using the *test case language* (TCL), yielding test cases that are formal enough to be executed automatically, while still being expressed in non-technical language, so that domain experts can read and validate them against their specifications. | Developers use the test specification as blueprint for implementation, and rely on the test cases to continuosly validate that they are making progress towards the intended goal.|
| ![Writing a Test Specification](/images/type-create-tsl.gif "Writing a Test Specification") | ![Writing a Test Case](/images/type-create-tcl.gif "Writing a Test Case") | ![Executing a Test Case](/images/execute-create-tcl.gif "Executing a Test Case") |
{: style="table-layout: fixed; border: 0px" }

The test-first practice, enabled by Test-Editor-Web on the user acceptance level, ensures that the development process is on the right track from the very beginning. Its ability for automated test execution allows to continuously validate each increment against the specification, so that development stays on track until completion.

## Learn More

* [Test Your Domain](/te_markdown/domainexperts): Discover the power and customizability of the different languages offered by Test-Editor-Web.


## Try it for Yourself

* Write your first test specification in 5 minutes.