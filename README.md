# monorepo-build-sample
Sample multi-module project to test [the monorepo-build](https://github.com/anbu-xyz/monorepo-build) maven plugin. 

This project also serves as an example of how to use maven-build-cache-plugin to cache the build artifacts.

## Notes

### What goes into calculating the cache key?

In a Maven build cache, the checksum is computed based on various elements that uniquely identify the state of the 
build. The key elements involved in computing this checksum include:

1. Project POM File: The `pom.xml` file is a primary source of project configuration. Changes in dependencies,
   plugins, or other configurations in the POM will affect the checksum.
2. Source Files
3. Resources
4. Dependencies including transitive dependencies
5. Build plugins and configurations
6. Environment settings: JVM version, operating system, and environment variables.
7. Maven properties: Any properties set in the POM or through profiles or command line arguments also affect the checksum.

