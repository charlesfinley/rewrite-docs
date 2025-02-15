# Migrate Spring Boot properties to 2.7

** org.openrewrite.java.spring.boot2.SpringBootProperties\_2\_7**
_Migrate properties found in `application.properties` and `application.yml`._

## Source

[Github](https://github.com/openrewrite/rewrite-spring), [Issue Tracker](https://github.com/openrewrite/rewrite-spring/issues), [Maven Central](https://search.maven.org/artifact/org.openrewrite.recipe/rewrite-spring/4.27.0/jar)

* groupId: org.openrewrite.recipe
* artifactId: rewrite-spring
* version: 4.27.0


## Usage

This recipe has no required configuration options and can be activated directly after taking a dependency on org.openrewrite.recipe:rewrite-spring:4.27.0 in your build file:

{% tabs %}
{% tab title="Gradle" %}
{% code title="build.gradle" %}
```groovy
plugins {
    id("org.openrewrite.rewrite") version("5.29.2")
}

rewrite {
    activeRecipe("org.openrewrite.java.spring.boot2.SpringBootProperties_2_7")
}

repositories {
    mavenCentral()
}

dependencies {
    rewrite("org.openrewrite.recipe:rewrite-spring:4.27.0")
}
```
{% endcode %}
{% endtab %}

{% tab title="Maven POM" %}
{% code title="pom.xml" %}
```markup
<project>
  <build>
    <plugins>
      <plugin>
        <groupId>org.openrewrite.maven</groupId>
        <artifactId>rewrite-maven-plugin</artifactId>
        <version>4.34.2</version>
        <configuration>
          <activeRecipes>
            <recipe>org.openrewrite.java.spring.boot2.SpringBootProperties_2_7</recipe>
          </activeRecipes>
        </configuration>
        <dependencies>
          <dependency>
            <groupId>org.openrewrite.recipe</groupId>
            <artifactId>rewrite-spring</artifactId>
            <version>4.34.2</version>
          </dependency>
        </dependencies>
      </plugin>
    </plugins>
  </build>
</project>
```
{% endcode %}
{% endtab %}

{% tab title="Maven Command Line" %}
{% code title="shell" %}
```shell
mvn org.openrewrite.maven:rewrite-maven-plugin:4.34.0:run \
  -Drewrite.recipeArtifactCoordinates=org.openrewrite.recipe:rewrite-spring:4.27.0 \
  -DactiveRecipes=org.openrewrite.java.spring.boot2.SpringBootProperties_2_7
```
{% endcode %}
{% endtab %}
{% endtabs %}

Recipes can also be activated directly from the command line by adding the argument `-Drewrite.activeRecipes=org.openrewrite.java.spring.boot2.SpringBootProperties_2_7`

## Definition

{% tabs %}
{% tab title="Recipe List" %}
* [Move SAML relying party identity provider property to asserting party](../../../java/spring/boot2/samlrelyingpartypropertyapplicationpropertiesmove.md)
* [Change key](../../../yaml/changekey.md)
  * oldKeyPath: `$.spring.security.saml2.relyingparty.registration.*[?(@.identityprovider)]`
  * newKey: `assertingparty`
* [Change property key](../../../properties/changepropertykey.md)
  * oldPropertyKey: `spring.artemis.host`
  * newPropertyKey: `spring.artemis.broker-url`
* [Change property key](../../../yaml/changepropertykey.md)
  * oldPropertyKey: `spring.artemis.host`
  * newPropertyKey: `spring.artemis.broker-url`
* [Change property key](../../../properties/changepropertykey.md)
  * oldPropertyKey: `spring.artemis.port`
  * newPropertyKey: `spring.artemis.broker-url`
* [Change property key](../../../yaml/changepropertykey.md)
  * oldPropertyKey: `spring.artemis.port`
  * newPropertyKey: `spring.artemis.broker-url`
* [Change property key](../../../properties/changepropertykey.md)
  * oldPropertyKey: `spring.batch.initialize-schema`
  * newPropertyKey: `spring.batch.jdbc.initialize-schema`
* [Change property key](../../../yaml/changepropertykey.md)
  * oldPropertyKey: `spring.batch.initialize-schema`
  * newPropertyKey: `spring.batch.jdbc.initialize-schema`
* [Change property key](../../../properties/changepropertykey.md)
  * oldPropertyKey: `spring.batch.schema`
  * newPropertyKey: `spring.batch.jdbc.schema`
* [Change property key](../../../yaml/changepropertykey.md)
  * oldPropertyKey: `spring.batch.schema`
  * newPropertyKey: `spring.batch.jdbc.schema`
* [Change property key](../../../properties/changepropertykey.md)
  * oldPropertyKey: `spring.batch.table-prefix`
  * newPropertyKey: `spring.batch.jdbc.table-prefix`
* [Change property key](../../../yaml/changepropertykey.md)
  * oldPropertyKey: `spring.batch.table-prefix`
  * newPropertyKey: `spring.batch.jdbc.table-prefix`
* [Change property key](../../../properties/changepropertykey.md)
  * oldPropertyKey: `spring.datasource.continue-on-error`
  * newPropertyKey: `spring.sql.init.continue-on-error`
* [Change property key](../../../yaml/changepropertykey.md)
  * oldPropertyKey: `spring.datasource.continue-on-error`
  * newPropertyKey: `spring.sql.init.continue-on-error`
* [Change property key](../../../properties/changepropertykey.md)
  * oldPropertyKey: `spring.datasource.data`
  * newPropertyKey: `spring.sql.init.data-locations`
* [Change property key](../../../yaml/changepropertykey.md)
  * oldPropertyKey: `spring.datasource.data`
  * newPropertyKey: `spring.sql.init.data-locations`
* [Change property key](../../../properties/changepropertykey.md)
  * oldPropertyKey: `spring.datasource.data-password`
  * newPropertyKey: `spring.sql.init.password`
* [Change property key](../../../yaml/changepropertykey.md)
  * oldPropertyKey: `spring.datasource.data-password`
  * newPropertyKey: `spring.sql.init.password`
* [Change property key](../../../properties/changepropertykey.md)
  * oldPropertyKey: `spring.datasource.data-username`
  * newPropertyKey: `spring.sql.init.username`
* [Change property key](../../../yaml/changepropertykey.md)
  * oldPropertyKey: `spring.datasource.data-username`
  * newPropertyKey: `spring.sql.init.username`
* [Change property key](../../../properties/changepropertykey.md)
  * oldPropertyKey: `spring.datasource.initialization-mode`
  * newPropertyKey: `spring.sql.init.mode`
* [Change property key](../../../yaml/changepropertykey.md)
  * oldPropertyKey: `spring.datasource.initialization-mode`
  * newPropertyKey: `spring.sql.init.mode`
* [Change property key](../../../properties/changepropertykey.md)
  * oldPropertyKey: `spring.datasource.platform`
  * newPropertyKey: `spring.sql.init.platform`
* [Change property key](../../../yaml/changepropertykey.md)
  * oldPropertyKey: `spring.datasource.platform`
  * newPropertyKey: `spring.sql.init.platform`
* [Change property key](../../../properties/changepropertykey.md)
  * oldPropertyKey: `spring.datasource.schema`
  * newPropertyKey: `spring.sql.init.schema-locations`
* [Change property key](../../../yaml/changepropertykey.md)
  * oldPropertyKey: `spring.datasource.schema`
  * newPropertyKey: `spring.sql.init.schema-locations`
* [Change property key](../../../properties/changepropertykey.md)
  * oldPropertyKey: `spring.datasource.schema-password`
  * newPropertyKey: `spring.sql.init.password`
* [Change property key](../../../yaml/changepropertykey.md)
  * oldPropertyKey: `spring.datasource.schema-password`
  * newPropertyKey: `spring.sql.init.password`
* [Change property key](../../../properties/changepropertykey.md)
  * oldPropertyKey: `spring.datasource.schema-username`
  * newPropertyKey: `spring.sql.init.username`
* [Change property key](../../../yaml/changepropertykey.md)
  * oldPropertyKey: `spring.datasource.schema-username`
  * newPropertyKey: `spring.sql.init.username`
* [Change property key](../../../properties/changepropertykey.md)
  * oldPropertyKey: `spring.datasource.separator`
  * newPropertyKey: `spring.sql.init.separator`
* [Change property key](../../../yaml/changepropertykey.md)
  * oldPropertyKey: `spring.datasource.separator`
  * newPropertyKey: `spring.sql.init.separator`
* [Change property key](../../../properties/changepropertykey.md)
  * oldPropertyKey: `spring.datasource.sql-script-encoding`
  * newPropertyKey: `spring.sql.init.encoding`
* [Change property key](../../../yaml/changepropertykey.md)
  * oldPropertyKey: `spring.datasource.sql-script-encoding`
  * newPropertyKey: `spring.sql.init.encoding`
* [Change property key](../../../properties/changepropertykey.md)
  * oldPropertyKey: `spring.flyway.check-location`
  * newPropertyKey: `spring.flyway.fail-on-missing-locations`
* [Change property key](../../../yaml/changepropertykey.md)
  * oldPropertyKey: `spring.flyway.check-location`
  * newPropertyKey: `spring.flyway.fail-on-missing-locations`

{% endtab %}

{% tab title="Yaml Recipe List" %}
```yaml
---
type: specs.openrewrite.org/v1beta/recipe
name: org.openrewrite.java.spring.boot2.SpringBootProperties_2_7
displayName: Migrate Spring Boot properties to 2.7
description: Migrate properties found in `application.properties` and `application.yml`.
recipeList:
  - org.openrewrite.java.spring.boot2.SamlRelyingPartyPropertyApplicationPropertiesMove
  - org.openrewrite.yaml.ChangeKey:
      oldKeyPath: $.spring.security.saml2.relyingparty.registration.*[?(@.identityprovider)]
      newKey: assertingparty
  - org.openrewrite.properties.ChangePropertyKey:
      oldPropertyKey: spring.artemis.host
      newPropertyKey: spring.artemis.broker-url
  - org.openrewrite.yaml.ChangePropertyKey:
      oldPropertyKey: spring.artemis.host
      newPropertyKey: spring.artemis.broker-url
  - org.openrewrite.properties.ChangePropertyKey:
      oldPropertyKey: spring.artemis.port
      newPropertyKey: spring.artemis.broker-url
  - org.openrewrite.yaml.ChangePropertyKey:
      oldPropertyKey: spring.artemis.port
      newPropertyKey: spring.artemis.broker-url
  - org.openrewrite.properties.ChangePropertyKey:
      oldPropertyKey: spring.batch.initialize-schema
      newPropertyKey: spring.batch.jdbc.initialize-schema
  - org.openrewrite.yaml.ChangePropertyKey:
      oldPropertyKey: spring.batch.initialize-schema
      newPropertyKey: spring.batch.jdbc.initialize-schema
  - org.openrewrite.properties.ChangePropertyKey:
      oldPropertyKey: spring.batch.schema
      newPropertyKey: spring.batch.jdbc.schema
  - org.openrewrite.yaml.ChangePropertyKey:
      oldPropertyKey: spring.batch.schema
      newPropertyKey: spring.batch.jdbc.schema
  - org.openrewrite.properties.ChangePropertyKey:
      oldPropertyKey: spring.batch.table-prefix
      newPropertyKey: spring.batch.jdbc.table-prefix
  - org.openrewrite.yaml.ChangePropertyKey:
      oldPropertyKey: spring.batch.table-prefix
      newPropertyKey: spring.batch.jdbc.table-prefix
  - org.openrewrite.properties.ChangePropertyKey:
      oldPropertyKey: spring.datasource.continue-on-error
      newPropertyKey: spring.sql.init.continue-on-error
  - org.openrewrite.yaml.ChangePropertyKey:
      oldPropertyKey: spring.datasource.continue-on-error
      newPropertyKey: spring.sql.init.continue-on-error
  - org.openrewrite.properties.ChangePropertyKey:
      oldPropertyKey: spring.datasource.data
      newPropertyKey: spring.sql.init.data-locations
  - org.openrewrite.yaml.ChangePropertyKey:
      oldPropertyKey: spring.datasource.data
      newPropertyKey: spring.sql.init.data-locations
  - org.openrewrite.properties.ChangePropertyKey:
      oldPropertyKey: spring.datasource.data-password
      newPropertyKey: spring.sql.init.password
  - org.openrewrite.yaml.ChangePropertyKey:
      oldPropertyKey: spring.datasource.data-password
      newPropertyKey: spring.sql.init.password
  - org.openrewrite.properties.ChangePropertyKey:
      oldPropertyKey: spring.datasource.data-username
      newPropertyKey: spring.sql.init.username
  - org.openrewrite.yaml.ChangePropertyKey:
      oldPropertyKey: spring.datasource.data-username
      newPropertyKey: spring.sql.init.username
  - org.openrewrite.properties.ChangePropertyKey:
      oldPropertyKey: spring.datasource.initialization-mode
      newPropertyKey: spring.sql.init.mode
  - org.openrewrite.yaml.ChangePropertyKey:
      oldPropertyKey: spring.datasource.initialization-mode
      newPropertyKey: spring.sql.init.mode
  - org.openrewrite.properties.ChangePropertyKey:
      oldPropertyKey: spring.datasource.platform
      newPropertyKey: spring.sql.init.platform
  - org.openrewrite.yaml.ChangePropertyKey:
      oldPropertyKey: spring.datasource.platform
      newPropertyKey: spring.sql.init.platform
  - org.openrewrite.properties.ChangePropertyKey:
      oldPropertyKey: spring.datasource.schema
      newPropertyKey: spring.sql.init.schema-locations
  - org.openrewrite.yaml.ChangePropertyKey:
      oldPropertyKey: spring.datasource.schema
      newPropertyKey: spring.sql.init.schema-locations
  - org.openrewrite.properties.ChangePropertyKey:
      oldPropertyKey: spring.datasource.schema-password
      newPropertyKey: spring.sql.init.password
  - org.openrewrite.yaml.ChangePropertyKey:
      oldPropertyKey: spring.datasource.schema-password
      newPropertyKey: spring.sql.init.password
  - org.openrewrite.properties.ChangePropertyKey:
      oldPropertyKey: spring.datasource.schema-username
      newPropertyKey: spring.sql.init.username
  - org.openrewrite.yaml.ChangePropertyKey:
      oldPropertyKey: spring.datasource.schema-username
      newPropertyKey: spring.sql.init.username
  - org.openrewrite.properties.ChangePropertyKey:
      oldPropertyKey: spring.datasource.separator
      newPropertyKey: spring.sql.init.separator
  - org.openrewrite.yaml.ChangePropertyKey:
      oldPropertyKey: spring.datasource.separator
      newPropertyKey: spring.sql.init.separator
  - org.openrewrite.properties.ChangePropertyKey:
      oldPropertyKey: spring.datasource.sql-script-encoding
      newPropertyKey: spring.sql.init.encoding
  - org.openrewrite.yaml.ChangePropertyKey:
      oldPropertyKey: spring.datasource.sql-script-encoding
      newPropertyKey: spring.sql.init.encoding
  - org.openrewrite.properties.ChangePropertyKey:
      oldPropertyKey: spring.flyway.check-location
      newPropertyKey: spring.flyway.fail-on-missing-locations
  - org.openrewrite.yaml.ChangePropertyKey:
      oldPropertyKey: spring.flyway.check-location
      newPropertyKey: spring.flyway.fail-on-missing-locations

```
{% endtab %}
{% endtabs %}
