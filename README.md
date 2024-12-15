MoonMC
===========

The most optimized, high-performance Paper fork that aims to fix gameplay and mechanics inconsistencies.

How To (Server Admins)
------
MoonMC is a jar file that you can download and run just like a normal jar file.

Download MoonMC from our [releases page](https://github.com/JTDMedia/MoonMC/releases).

Run the MoonMC jar directly from your server. Just like old times

* Documentation on using MoonMC (same as papermc): [docs.papermc.io](https://docs.papermc.io)
  
How To (Plugin Developers)
------
* See our API patches [here](patches/api)
* Paper API javadocs here: [papermc.io/javadocs](https://papermc.io/javadocs/)
#### Repository (for paper-api)
##### Maven

```xml
<repository>
    <id>papermc</id>
    <url>https://repo.papermc.io/repository/maven-public/</url>
</repository>
```

```xml
<dependency>
    <groupId>io.papermc.paper</groupId>
    <artifactId>paper-api</artifactId>
    <version>1.21.4-R0.1-SNAPSHOT</version>
    <scope>provided</scope>
</dependency>
```
##### Gradle
```kotlin
repositories {
    maven {
        url = uri("https://repo.papermc.io/repository/maven-public/")
    }
}

dependencies {
    compileOnly("io.papermc.paper:paper-api:1.21.4-R0.1-SNAPSHOT")
}

java {
    toolchain.languageVersion.set(JavaLanguageVersion.of(21))
}
```

How To (Compiling Jar From Source)
------
To compile MoonMC, you need JDK 21 and an internet connection.

Clone this repo, run `./gradlew applyPatches`, then `./gradlew createMojmapBundlerJar` from your terminal. You can find the compiled jar in the project root's `build/libs` directory.

To get a full list of tasks, run `./gradlew tasks`.

How To Contribute
------
See [Contributing](CONTRIBUTING.md)
