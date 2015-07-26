andreptb-component-parent [![Maven Central](https://maven-badges.herokuapp.com/maven-central/com.github.andreptb/andreptb-component-parent/badge.svg)](https://maven-badges.herokuapp.com/maven-central/com.github.andreptb/andreptb-component-parent/)
==============

[Maven Parent POM](https://maven.apache.org/guides/introduction/introduction-to-the-pom.html) designed to provide common tasks for projects available on [Maven Central](http://search.maven.org/). These tasks are implemented by various plugins registered and configured on this parent POM, as detailed below:

| Plugin | [Phase](https://maven.apache.org/ref/3.3.3/maven-core/lifecycles.html) | Description |  
| -------| ---------------------------------------------------------------------- | ---- | ----------- |
| [maven-scm-plugin](http://maven.apache.org/scm/maven-scm-plugin) | initialize | Checkout configuration files such as source code formatters, static analysis rules and CI related files) |
| [maven-formatter-plugin](https://github.com/velo/maven-formatter-plugin) | process-sources | Formats the source code considering  eclipse [configuration files](src/config/eclipse) retrieved from [maven-scm-plugin](http://maven.apache.org/scm/maven-scm-plugin). |
| [jacoco-maven-plugin](http://www.eclemma.org/jacoco/trunk/doc/maven.html) | process-test-sources | Adds coverage configuration  with Jacoco. |
| [maven-source-plugin](https://maven.apache.org/plugins/maven-source-plugin) | package | Generates project's source code artifact. |
| [maven-javadoc-plugin](https://maven.apache.org/plugins/maven-javadoc-plugin) | package | Generates project's javadoc artifact. |
| [maven-gpg-plugin](https://maven.apache.org/plugins/maven-gpg-plugin) | package | Generates project's gpg artifacts. |
| [nexus-staging-maven-plugin](https://github.com/sonatype/nexus-maven-plugins/tree/master/staging/maven-plugin) | deploy | Deploys generated artifacts to maven central. |
