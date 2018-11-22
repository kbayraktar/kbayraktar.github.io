---
layout: page
title: Test Your Application
permalink: /te_markdown/testdrivers/
---

Estimated reading time: 3 minutes

User acceptance tests should focus on the needs and expected behaviors of the software under test from a user-centric perspective, expressed in technology-agnostic terms of the application domain. However, to automate these tests, the particular technology stack of the software under test have to be taken into account. Effective user acceptance test tools have to cater to both requirements, while also being generic enough to be applicable to the testing of different applications build on diverse platforms and technologies.

**Test-Editor-Web** decouples test specification and test case descriptions from concrete, executable tests that can be run against a given software under test. From test cases expressed with the test case language (TCL), the actual test code is generated on demand, relying on different *test fixtures* that encapsulate the mapping of generic test steps to concrete actions appropriate for a particular technology. Out of the box, the following fixtures are available:

 * Web Fixture: Allows to test contemporary *web applications* (HTML5 in general, with particular support for *Angular* applications) with Firefox or Chrome.
 * REST Fixture: Allows to test *REST services* using JSON data to drive them.
 * Swing Fixture: Allows to test *Java Swing* applications.
 * Host Fixture: Allows to test mainframe programs through *3270 terminal emulation*.

Test-Editor-Web is extensible in this respect, and additional test fixtures can be implemented and added to address target platforms that are not yet covered.

## Learn More

* [Test Containerized](/te_markdown/testexec): Find out about the ability and benefits of executing tests in dedicated Docker containers.


## Try it for Yourself

* Do you want to write your first test specification in 5 minutes? [read more](/te_markdown/heroes-create-spec){:class="web-button-grey reduced-padding"}
* Do you want to Write your first test case in 8 minutes? [read more](/te_markdown/heroes-create-testcase){:class="web-button-grey reduced-padding"}
