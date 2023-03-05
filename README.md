# ForestConfigAPI
![badge](https://img.shields.io/github/v/release/ForestTechMC/ForestConfigAPI)
[![badge](https://jitpack.io/v/ForestTechMC/ForestConfigAPI.svg)](https://jitpack.io/#ForestTechMC/ForestConfigAPI)
![badge](https://img.shields.io/github/downloads/ForestTechMC/ForestConfigAPI/total)
![badge](https://img.shields.io/github/last-commit/ForestTechMC/ForestConfigAPI)
![badge](https://img.shields.io/badge/platform-spigot-lightgrey)
[![badge](https://img.shields.io/discord/896466173166747650?label=discord)](https://discord.gg/2PpdrfxhD4)
[![badge](https://img.shields.io/github/license/ForestTechMC/ForestConfigAPI)](https://github.com/ForestTechMC/ForestConfigAPI/blob/master/LICENSE.txt)

**[JavaDoc 1.0](https://foresttechmc.github.io/ForestConfigAPI/1.0/)**

Small and effective Config API for Developers! <br>
Only spigot support! <br>
([Bungee version](https://github.com/FlyUltra/TheBungeeConfig))

## Table of contents

* [Getting started](#getting-started)
* [Using the config API](#using-config-api)
* [License](#license)

## Getting started

Make sure you reloaded maven or gradle in your project.

### Add ForestConfigAPI to your project

[![badge](https://jitpack.io/v/ForestTechMC/ForestConfigAPI.svg)](https://jitpack.io/#ForestTechMC/ForestConfigAPI)

You need to add this dependency into your plugin, then look at under the dependencies example

<details>
    <summary>Maven</summary>

```xml
<repositories>
    <repository>
        <id>jitpack.io</id>
        <url>https://jitpack.io</url>
    </repository>
</repositories>

<dependencies>
    <dependency>
        <groupId>com.github.ForestTechMC</groupId>
        <artifactId>ForestConfigAPI</artifactId>
        <version>VERSION</version>
        <scope>provided</scope>
    </dependency>
</dependencies>
```
</details>

<details>
    <summary>Gradle</summary>

```gradle
allprojects {
    repositories {
        ...
        maven { url 'https://jitpack.io' }
    }
}

dependencies {
    implementation 'com.github.ForestTechMC:ForestConfigAPI:VERSION'
}
```
</details>

### Using Config API

```java
    // Main class
    private Main plugin;
    // This API
    private ConfigAPI configAPI;
    
    // Load method
    public void loadConfig() {
        // Constructor with Main class, and name
        configAPI = new ConfigAPI(plugin, "coolConfig");    
        // Create config
        configAPI.create();
        
        // getConfig() -> this return you configuration of file for using like normal config
        configAPI.getConfig().set("coolMessage", "Cool message in config!");
        // this save your edits
        configAPI.save();
    }
    
        // Here you can see, how to get string from your "coolConfig.yml" with path "coolMessage"
    public void messages() {
        configAPI.getConfig().getString("coolMessage");
    }
```

## License
ForestRedisAPI is licensed under the permissive MIT license. Please see [`LICENSE.txt`](https://github.com/ForestTechMC/ForestConfigAPI/blob/master/LICENSE.txt) for more information.