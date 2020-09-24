---
layout: documentation
pill: driver
subtitle: flyway.driver
---

# Driver

## Description
The fully qualified classname of the jdbc driver to use to connect to the database.

This must match the driver for the database type in the [url](/documentation/configuration/url) you are using.

## Default
Auto-detected based on the url

## Usage

### Commandline
```
./flyway -driver=com.microsoft.sqlserver.jdbc.SQLServerDriver info
```

### Configuration File
```
flyway.driver=com.microsoft.sqlserver.jdbc.SQLServerDriver
```

### Environment Variable
```
FLYWAY_DRIVER=com.microsoft.sqlserver.jdbc.SQLServerDriver
```

### API
```
flyway.configure()
    .driver("com.microsoft.sqlserver.jdbc.SQLServerDriver")
    .load()
```

### Gradle
```
flyway {
    driver = 'com.microsoft.sqlserver.jdbc.SQLServerDriver'
}
```

### Maven
```
<configuration>
    <driver>com.microsoft.sqlserver.jdbc.SQLServerDriver</driver>
</configuration>
```