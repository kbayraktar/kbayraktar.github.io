---
layout: page
title: Application Mapping Language
permalink: /te_markdown/heroes-create-aml/
---

Estimated reading time: 8 minutes

The [Application Mapping Language](/te_markdown/terminology#application-mapping-language) (AML) is used to define interactions with the application, which are then referenced by test steps within a test case (see [TCL](/te_markdown/terminology#test-case-language)). It decouples the concrete [fixtures](/te_markdown/terminology#test-fixture) on the application mapping to be tested from the test implementation. This separation enables a tester role which concentrates on test implementation agnostic to technology.

## Prerequisites

The software under test that is used for this example is an implementation of the heroes tutorial of the angular framework (see [here](https://angular.io/tutorial)).

You want to know more about the software that is tested here? [read more](/te_markdown/sut-heroes){:class="web-button-grey reduced-padding"}

The test specification that is implemented in this example is described in detail in this [tutorial TSL](/te_markdown/heroes-create-spec).

The test case we want to use for our AML in this example is described in detail in this [tutorial TCL](/te_markdown/heroes-create-testcase) 

## How do I write an AML ?

First we create an AML file through clicking on the 'create new' button on the left corner of the [Test Navigator](/te_markdown/terminology#test-navigator) 
- create a new file with the extension '.aml' (e.g. [Heroes.aml](https://github.com/test-editor/language-examples/blob/tutorial/hero-create-testcase/src/test/java/org/testeditor/heroes/Heroes.aml)) and type ```CTRL + S``` to save the file.

![screencase: create aml file](/images/tutorial/tutorial_create_aml_file.gif "screencast: create aml file")

Every AML file need some preconfiguration, like which [fixture](/te_markdown/terminology#test-fixture) or which [locator strategy](/te_markdown/terminology#locator-strategy) to use. Please copy following lines into the new created AML file and save the file with the keyboard shortcut ```CTRL + S```.

```
package org.testeditor.heroes

import org.testeditor.fixture.web.*

import static org.testeditor.fixture.web.LocatorStrategy.XPATH

```
![screencase: add configuration](/images/tutorial/tutorial_create_aml_file_copy_configuration.gif "screencast: add configuration")

For GUI Automation the first thing to do is, to identify the GUI-Elements on the [Software Under Test](/te_markdown/terminology#software-under-test) sites. Meanwhile the most popular browser provider support developer tools to recognize web elements. In our example we use the 'Web Developer Tool' for Firefox. To activate the developer tool in an opened Firefox browser, just click the function key `F12` on your keyboard.    

The following steps are necessary to identify all Gui-Elements for every single test step.
- navigate to your Software Under Test with your preferred browser (in our example we use Firefox)
- open the 'Developer Tools' with the keyboard  shortcut `F12`.
- activate the inspection tool on the left upper corner of the Developer Tools' 
- click on the add button to show more attributes about this web element in the marked section of the 'Developer Tools' on the right. 

![screencase: recognize add button](/images/tutorial/tutorial_identify_add_button.gif "screencast: recognize add button")

The path for the add button which is shown in the screencast is:

`home > body > my-root > my-heroes > button`

To get a better overview of all web-elements on one page you can summarize them in a [component](/te_markdown/terminology#component). In our example we name our page 'Heroes'   

```
package org.testeditor.heroes

import org.testeditor.fixture.web.*

import static org.testeditor.fixture.web.LocatorStrategy.XPATH

component Heroes is Page {
}
```

![screencase: add component heroes](/images/tutorial/tutorial_create_aml_file_component_heroes.gif "screencast: add component heroes")

- Add the button element with the above found path as XPATH locator into the component 'Heroes'.

```
package org.testeditor.heroes

import org.testeditor.fixture.web.*

import static org.testeditor.fixture.web.LocatorStrategy.XPATH

component Heroes is Page {
  element Add is button locate by XPATH "/html/body/my-root/my-heroes/button"
}
```

![screencase: add element add button](/images/tutorial/tutorial_create_aml_file_element_ADD.gif "screencast: add element add button")

- Do the same procedure for the Save Button with the XPATH : `/html/body/my-root/my-heroes/div[1]/my-hero-detail/div/button[2]`.  

```
package org.testeditor.heroes

import org.testeditor.fixture.web.*

import static org.testeditor.fixture.web.LocatorStrategy.XPATH

component Heroes is Page {
  element Add is button locate by XPATH "/html/body/my-root/my-heroes/button"
  element Save is button locate by XPATH "/html/body/my-root/my-heroes/div[1]/my-hero-detail/div/button[2]"
}
```

![screencase: add element save button](/images/tutorial/tutorial_create_aml_file_element_SAVE.gif "screencast: add element save button")

- For input web elements you have to use a field as a component element type instead of a button.

```
package org.testeditor.heroes

import org.testeditor.fixture.web.*

import static org.testeditor.fixture.web.LocatorStrategy.XPATH

component Heroes is Page {
  element Add is button locate by XPATH "/html/body/my-root/my-heroes/button"
  element Save is button locate by XPATH "/html/body/my-root/my-heroes/div[1]/my-hero-detail/div/button[2]"
  element Name is field locate by XPATH "/html/body/my-root/my-heroes/div[1]/my-hero-detail/div/div[2]/input"
}
```

![screencase: add element name field](/images/tutorial/tutorial_create_aml_file_element_NAME.gif "screencast: add element name field")

- Do the same procedure for the last item field with the XPATH : `"/html/body/my-root/my-heroes/ul/li[last()]/span"`

```
package org.testeditor.heroes

import org.testeditor.fixture.web.*

import static org.testeditor.fixture.web.LocatorStrategy.XPATH

component Heroes is Page {
  element Add is button locate by XPATH "/html/body/my-root/my-heroes/button"
  element Save is button locate by XPATH "/html/body/my-root/my-heroes/div[1]/my-hero-detail/div/button[2]"
  element Name is field locate by XPATH "/html/body/my-root/my-heroes/div[1]/my-hero-detail/div/div[2]/input"
  element LastListItem is field locate by XPATH "/html/body/my-root/my-heroes/ul/li[last()]/span"
}
```

![screencase: add element last field](/images/tutorial/tutorial_create_aml_file_element_FIELD.gif "screencast: add element last field")


That's it. Your first AML is in place. 

Do you want to know how to execute your test? 
[read more](/te_markdown/heroes-create-testcase-execution){:class="web-button-grey reduced-padding"}

Do you want to learn more about the editor and how the tests can be written, saved or making use of content completion etc.?
[read more](/te_markdown/heroes-create-testcase-editor){:class="web-button-grey reduced-padding"}

## Some reflections

The AML is expected to be written by a developer when the application is in place. 

The vocabulary used in test cases is largely defined through artifacts written in the application mapping language (AML). The tester/developer writes mappings of the test vocabulary onto the actual implementation using this AML.
For the given tutorial a minimal AML was provided (Heroes.aml), partially describing the software under test.


Do you want to learn more about how to write a test specification?
[read more](/te_markdown/heroes-create-spec){:class="web-button-grey reduced-padding"}
