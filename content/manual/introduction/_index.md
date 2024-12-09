---

title: "Introduction"
weight: 10
layout: "single"

menu:
  main:
    identifier: "user-guide-introduction"

---


Welcome to the Operaton Manual! Operaton is a Java-based framework supporting BPMN for workflow and process automation, CMMN for Case Management and DMN for Business Decision Management. Also see: [Implemented Standards]({{< ref "/manual/introduction/implemented-standards.md" >}}).

This document contains information about the features provided by Operaton.

To give you an overview of Operaton, the following illustration shows the most important components along with some typical user roles.

{{< img src="img/architecture-overview.png" title="Operaton Components and Roles" >}}


# Process Engine & Infrastructure

* [Process Engine]({{< ref "/manual/user-guide/process-engine/_index.md" >}}) The process engine is a Java library responsible for executing BPMN 2.0 processes, CMMN 1.1 cases and DMN 1.3 decisions. It has a lightweight POJO core and uses a relational database for persistence. ORM mapping is provided by the MyBatis mapping framework.
* [Spring Framework Integration]({{< ref "/manual/user-guide/spring-framework-integration/_index.md" >}})
* [CDI/Java EE Integration]({{< ref "/manual/user-guide/cdi-java-ee-integration/_index.md" >}})
* [Runtime Container Integration]({{< ref "/manual/user-guide/runtime-container-integration/_index.md" >}}) (Integration with application server infrastructure.)

# Modeler

* [Operaton Modeler]({{< ref "/manual/modeler/_index.md" >}}): Modeling tool for BPMN 2.0 and CMMN 1.1 diagrams as well as DMN 1.3 decision tables.
* [bpmn.io](http://bpmn.io/): Open-source project for the modeling framework and toolkits.

# Web Applications

* [REST API]({{< ref "/manual/reference/rest/_index.md" >}}) The REST API allows you to use the process engine from a remote application or a JavaScript application. (Note: The documentation of the REST API is factored out into own documents.)
* [Operaton Tasklist]({{< ref "/manual/webapps/tasklist/_index.md" >}}) A web application for human workflow management and user tasks that allows process participants to inspect their workflow tasks and navigate to task forms in order to work on the tasks and provide data input.
* [Operaton Cockpit]({{< ref "/manual/webapps/cockpit/_index.md" >}}) A web application for process monitoring and operations that allows you to search for process instances, inspect their state and repair broken instances.
* [Operaton Admin]({{< ref "/manual/webapps/admin/_index.md" >}}) A web application that allows you to manage users, groups and authorizations.
