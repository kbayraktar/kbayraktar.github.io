---
layout: page
title: Test Continuously
permalink: /te_markdown/ci/
---

Estimated reading time: 2 minutes

 ![Test continuously](/images/04-en_cut.png "Test continuously"){: style="    display: block; margin-left: auto; margin-right: auto; width: 100%;" }

Modern, agile development practices encompass continuous integration, delivery, and deployment. User acceptance testing should be a part of these processes, to monitor progress while developing with each increment and complement existing quality assurance measures. Therefore, the tests have to be integrable into the corresponding build pipelines.

**Test-Editor-Web** allows to both start test runs directly from within the web-based user interface, but also to execute them completely independent. Tests can therefore be easily made part of automated build processes to be run either locally or within the context of a CI-server. Technically, this option is provided through the [Gradle](https://gradle.org/) build automation system.

## Try it for Yourself

* Do you want to write your first test specification in 5 minutes? [read more](/te_markdown/heroes-create-spec){:class="web-button-grey reduced-padding"}
* Do you want to Write your first test case in 8 minutes? [read more](/te_markdown/heroes-create-testcase){:class="web-button-grey reduced-padding"}
