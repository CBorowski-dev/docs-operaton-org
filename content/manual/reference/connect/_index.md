---

title: 'Operaton Connector Reference'
weight: 70
layout: "single"

menu:
  main:
    name: "Connectors"
    identifier: "connect-ref"
    parent: "references"

---

Operaton Connect provides a simple API for connecting HTTP services and other
things. It aims at two usage scenarios: usage in a generic system such as the
Operatonprocess engine and standalone usage via API.

# Connectors

Operaton Connect provides a HTTP and a SOAP HTTP connector. If you want to
add an own connector to Connect please have a look at the [extending Connect]({{< ref "/manual/reference/connect/extending-connect.md" >}})
section. This section also describes the usage of a `ConnectorConfigurator` to
configure the connector instances.

During the request invocation of a connector an interceptor chain is passed.
The user can add own interceptors to this chain. The interceptor is called for
every request of this connector.

```java
connector.addRequestInterceptor(interceptor).createRequest();
```

# Maven Coordinates

Connect can be used in any Java-based application by adding the following maven
dependency to your `pom.xml` file:

{{< note title="Operaton BOM" class="info" >}}
If you use other Operatonprojects please import the
[Operaton BOM](/get-started/apache-maven/)
to ensure correct versions for every Operaton project.
{{< /note >}}

```xml
<dependencyManagement>
  <dependencies>
    <dependency>
      <groupId>org.camunda.connect</groupId>
      <artifactId>camunda-connect-bom</artifactId>
      <scope>import</scope>
      <type>pom</type>
      <version>${version.camunda}</version>
    </dependency>
  </dependencies>
</dependencyManagement>
```

```xml
<dependencies>
  <dependency>
    <groupId>org.camunda.connect</groupId>
    <artifactId>camunda-connect-core</artifactId>
  </dependency>

  <dependency>
    <groupId>org.camunda.connect</groupId>
    <artifactId>camunda-connect-connectors-all</artifactId>
  </dependency>
</dependencies>
```

Operaton Connect is published to [maven central](http://search.maven.org/#search%7Cga%7C1%7Ccamunda-connect).

{{< note title="Process engine plugin" class="info" >}}
If you are using Connect in the Operatonprocess engine, you also need the `camunda-engine-plugin-connect` dependency. For more information, refer to the [Connectors guide]({{< ref "/manual/user-guide/process-engine/connectors.md" >}}).
{{< /note >}}

# Logging

Operaton Connect uses [camunda-commons-logging](https://github.com/camunda/camunda-bpm-platform/tree/master/commons/logging) which itself uses [SLF4J](http://slf4j.org) as
a logging backend. To enable logging a SLF4J implementation has to be part of
your classpath. For example `slf4j-simple`, `log4j12` or `logback-classic`.

To also enable logging for the Apache HTTP client you can use a [SLF4J
bridge](http://www.slf4j.org/legacy.html) like `jcl-over-slf4j` as the Apache HTTP Client doesn't support
SLF4J.
