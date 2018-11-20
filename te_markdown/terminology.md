---
layout: page
title: Overview and Terminology
permalink: /te_markdown/terminology/
---

Test-Editor-Web is a lightweight application for specifying, implementing, and executing user acceptance tests, that lives in your browser. This page provides a high-level [overview](#overview) of its user interface and its central components. If you would rather like to jump right in and try out Test-Editor-Web for yourself, have a look at one of the [quickstart tutorials](/te_markdown/tutorials). If any questions should arise, you may want to come back here to get your bearings by looking at the overview, or look up individual terms in the [glossary](#glossary) further down.

## Overview

<!--- TODO: insert (annotated?) overview image and briefly describe the main areas of the user interface -->
![Overview](/images/te.overview.png){:class="img-responsive"}

### The different areas of the Test-Editor-Web
In the screenshot above you can see the different areas of the Test-Editor-Web which are divided
under different colors. The description of the specific area can be found under the number of this area.   

#### 1. The Test-Navigator area
In this area the user can specify the structure of the different test artifacts.
He can create, delete, rename, copy and paste test artifacts.
In this example we have the path structure of a test specification named 'Create.tsl'
```
org -> testeditor -> heroes -> solution -> Create.tsl
``` 
![Test-Navigator](/images/te.navigator.png){:class="img-responsive"}

**Test-Navigator functionality**

In the yellow marked area , the user can create, delete, rename, copy and paste test artifacts.

![Navigator-Tools](/images/te.navigator_tools.svg?sanitize=true)

**Test-Navigator Filter**

In the yellow marked area, the user can filter the different test-artifacts, so that just the specific test-artifact is visible which was selected.

![Navigator-Filter](/images/te.navigator_filter.svg?sanitize=true)


#### 2. The Editor area


#### 3. The Test-Step-Selector area


#### 4. The Test-Execution-Navigator area


#### 5. The Test-Execution-Details area


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