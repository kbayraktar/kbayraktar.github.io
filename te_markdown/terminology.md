---
layout: page
title: Overview and Terminology
permalink: /te_markdown/terminology/
---

Test-Editor-Web is a lightweight application for specifying, implementing, and executing user acceptance tests, that lives in your browser. This page provides a high-level [overview](#overview) of its user interface and its central components. If you would rather like to jump right in and try out Test-Editor-Web for yourself, have a look at one of the [quickstart tutorials](/te_markdown/tutorials). If any questions should arise, you may want to come back here to get your bearings by looking at the overview, or look up individual terms in the [glossary](#glossary) further down.

## Overview

![Overview](/images/te.overview.svg?sanitize=true){:class="img-responsive"}

### The different areas of the Test-Editor-Web
In the screenshot above you can see the different areas of the Test-Editor-Web which are divided
through the different yellow areas. The description of the specific area can be found under the number of this area underneath.   

#### 1. The Test-Navigator area
In this area the user can specify the structure of the different test artifacts.
He can create, delete, rename, cut, copy and paste test artifacts and refresh the workspace.
The user can filter the different test-artifacts, so that just the specific test-artifact is visible which was selected.

#### 2. The Editor area
This area is the place to write different test artifacts. The editor supports the user with a content completion of the different possibilities during typing and saving your test case e.g. through the shortcut ```STRG + S``` . 

#### 3. The Test-Step-Selector area
The user can find the different testdriver test steps as an overview in the Test-Step-Selektor area, to define test cases.

#### 4. The Test-Execution-Navigator area
Here you can excute the chosen testcase through clicking the start button on top left corner of this area. After test execution the results of the separate test case steps are shown in this area.
* Green icons representing a successful test run. 
* Red icons representing an abortion of the test run. The possible reason of the failure situation will be recorded briefly. The details cause of failure will be presented in the Test-Execution-Details area. 


#### 5. The Test-Execution-Details area
In this area, details cause of failure and accordingly details of test case steps are presented.

----

## Glossary

* Domain Expert
* Developer
* Test Case Language (TCL)
* Test-Editor-Web
* Test Specification Language (TSL)
* Tester

<!--- TODO: write user-friendly definitions, layout the glossary as definition list with anchors for cross-referencing. The following is an example of how that might look:
<a name="domain-expert"></a>Domain expert
: A stakeholder and probably a user of the system under test, who has a deep understanding of the problem domain. Domain experts specify what they expect the system to do and how it should behave, using the [test specification language (TSL)](#test-specification-language).

<a name="developer"></a>Developer
: TBW

<a name="tester"></a>Tester
: TBW

<a name="test-specification-language"></a>Test Specification Language (TSL)
: TBW
-->