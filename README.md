# parent-pom-oss-java

The common parent POM of Suresh Jaganathan's Java libraries. This POM

* sets the current version for all standard plugins
* provides configuration for a simple release workflow
* adds plugins repeatedly used

The POM is published under the
[MIT license](http://opensource.org/licenses/MIT).

## Usage

Use this POM as parent POM of your project by adding the following
snippet to your `pom.xml`.

    <parent>
      <groupId>io.github.sureshnath</groupId>
      <artifactId>parent-pom-oss-java</artifactId>
      <version>1.0-snapshot</version>
    </parent>


## Development Guide

Check for plugin updates by running

    mvn -U versions:display-plugin-updates

Update the plugins and mention the plugin updates in the commit message.
Now release the POM.    

## Release Guide

You can release the POM to
[Maven Central](http://search.maven.org/) with a few steps.

* Set the new version in `pom.xml` and in the installation section of
  this document.
* Commit the updated `pom.xml` and `README.md`.
* Run `mvn clean deploy`
* Add a tag for the release: `git tag parent-pom-oss-java-XX`

This POM is inspired by [Stefan Birkner](https://github.com/stefanbirkner/lib-parent)