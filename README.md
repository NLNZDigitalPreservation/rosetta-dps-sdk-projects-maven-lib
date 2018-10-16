# Rosetta DPS SDK Projects Maven Lib (rosetta-dps-sdk-projects-maven)

## Synoposis

Provide a maven-friendly binary redistribution of the Rosetta
DPS SDK jar (`dps-sdk-<version>.jar`) and pom.xml and with the
Rosetta DPS SDK jar for upload to a nexus-style or maven local
repository.

## Motivation

The Rosetta DPS SDK, found at [github ExLibrisGroup/Rosetta.dps-sdk-projects](https://github.com/ExLibrisGroup/Rosetta.dps-sdk-projects)
distributes a fat JAR, `dps-sdk-<version>.jar`, which contains many of the
dependencies necessary to use the Rosetta SDK. This jar is suitable for use in
ant build scripts, but for maven it would be helpful if the jar could be
uploaded into a Nexus-style repository or local maven repository with a
pom with its group and artifact id, its version and its dependencies.

This project does that very thing.

## Versioning

Versions are by filename. For example, the 5.5.0 version is in the dps-sdk-5.5.0.jar
file and the pom file is dps-sdk-5.5.0-pom.xml.

## Usage

### Uploading to Nexus repository

### Uploading to Maven local (.m2) repository

```
mvn install:install-file -Dfile=<path-to-dps-sdk-jar-file> -DpomFile=<path-to-pomfile-coversioned-with-dps-sdk-jar-file>
```

## Including in projects

### For maven projects
```
<dependency>
    <groupId>com.exlibris.dps</groupId>
    <artifactId>dps-sdk-fat-all</artifactId>
    <version><the-version-number></version>
</dependency>

```

### For gradle projects
```
compile 'com.exlibris.dps:dps-sdk-fat-all:<the-version-number>'
```

## Contributors

See git commits to see who contributors are. Issues are tracked through the github issue tracker.

## License

`dps-sdk-<version>.jar`: See LICENSE-Rosetta.dps-sdk-projects.txt

All other files: &copy; 2018 National Library of New Zealand. All rights reserved. MIT license.
