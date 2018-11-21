---
layout: page
title: Tutorial: test case "create hero"
permalink: /te_markdown/heroes-create-testcase/
---

- Estimated reading time: 5 minutes
- Audience: [Curious party], Noob, Somewhat experienced, Experienced, Expert

Test cases implement test specifications. They are executable and are therefore more strict on syntax than test specifications are. The vocabulary that is used within these
test cases are largely controlled by the user of the test editor, however, sane defaults are provided.

## How do I write test cases?

The software under test that is used for this example is an implementation of the heroes tutorial of the angular framework (see [here](https://angular.io/tutorial)).

![screencast: create hero](/images/tutorial/tutorial.heroes.create.app.gif "screencast: create hero"){:align="right"}

Given you have a running instance of the test-editor-web, the following steps are necessary to implement the test specification.
- navigate to (or create) the folder to hold the test case
- create a new file with the extension '.tcl' (e.g. CreateHero.tcl)
- Write the test case name into the opened editor, prefixing it with '#' (e.g. '# CreateHero')
- State that this test case implements the `CreateHero` specification ('implements CreateHero')
- Copy the specification steps of the implemented test specification (all three lines starting with '*')
- Now implement each specification step with the actual test flow intended
  - `* Given: I am on the heroes page`
```
        Component: org.testeditor.fixture.web.WebBrowser
        - Start <Firefox>
        - Browse "http://sut:4200/heroes"
```
  - `* When: I create a hero named "Sancho"`
```
        Component: org.testeditor.heroes.Heroes
        - Wait "2" seconds until <Add> is found
        - Click <Add>
        - Enter "Sancho" into <Name>
        - Wait "2" seconds until <Save> is found
        - Click <Save>
```
  - `* Then: The hero should be the last one of the list`
```
        Component: org.testeditor.heroes.Heroes
        - Wait "2" seconds // until page is fully rendered after save
        - actualName = Read <LastHero>
        - assert actualName = "21 Sancho"
```
  - and finally do some cleanup
```
        Component: org.testeditor.fixture.web.WebBrowser
        - Close browser
```

![screencase: create hero test case](/images/tutorial.heroes.create.testcase.gif "screencast: create hero test case")

That's it. Your first test in place. 

If you want to know how to execute your test, [read more](heroes-create-testcase-execution){:class="web-button-grey"}

If you want to learn more about the editor and how the tests can be written, making use of content completion etc., [read more](heroes-create-testcase-editor){:class="web-button-grey"}

## Some reflections

The test case is expected to be written by a tester before the application is in place. The function of a test case is manifold.

* It represents a concrete test execution plan that implements a test specification and can be readily understood by the domain expert who wrote the specification
* It is concrete insofar as to be executable 
* It is the concrete and detailed expection developers can realize their application for
* It functions as a bridge between actual feature implementation (developer) and feature specification (domain expert), working as an artifact for discussion between domain expert, tester and developer

It is quite common to have the test case change because of implementation issues that could not have been foreseen. Changes need to be discussed though, which again has the benefit of sharing a common understanding of the feature to be implemented between domain expert, tester and developer. 

The vocabulary used in test cases is largely defined through artifacts written in the application mapping language (AML). The tester/developer writes mappings of the test vocabulary onto the actual implementation using this AML.
For the given tutorial a minimal AML was provided (Heroes.aml), partially describing the software under test. If you want to learn more about the AML, [read more](heroes-create-aml){:class="web-button-grey"}
