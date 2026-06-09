# LTS Parent POM

Maven parent POM for UVA LTS projects. Provides a shared, consistent build foundation so individual projects don't have to repeat configuration.

## What it provides

- **Spring Boot** `3.5.14` as the upstream parent (manages dependency versions).
- **Java** `25` as the target language level.
- **[Spotless](https://github.com/diffplug/spotless)** with Google Java Format, enforced during the `compile` phase. Uses `ratchetFrom origin/main` so formatting is only checked on files changed in your branch.
- Publishing to **GitHub Packages** (`stacs/maven-repo`).

## Usage

Reference it as the parent in your project's `pom.xml`:

```xml
<parent>
    <groupId>edu.virginia.its.lts</groupId>
    <artifactId>parent-pom</artifactId>
    <version>3.5.14</version>
</parent>
```

## License

MIT
