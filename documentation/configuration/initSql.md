---
layout: documentation
pill: initSql
subtitle: flyway.initSql
---

# Init SQL

## Description
The SQL statements to run to initialize a new database connection immediately after opening it.

This is mainly used for setting some state on the connection that needs to be shared across all scripts, or should not be included into any one script.

## Usage

### Commandline
```
./flyway -initSql="ALTER SESSION SET NLS_LANGUAGE='ENGLISH';" info
```

### Configuration File
```
flyway.initSql=ALTER SESSION SET NLS_LANGUAGE='ENGLISH';
```

### Environment Variable
```
FLYWAY_INIT_SQL=ALTER SESSION SET NLS_LANGUAGE='ENGLISH';
```

### API
```
flyway.configure()
    .initSql("ALTER SESSION SET NLS_LANGUAGE='ENGLISH';")
    .load()
```

### Gradle
```
flyway {
    initSql = "ALTER SESSION SET NLS_LANGUAGE='ENGLISH';"
}
```

### Maven
```
<configuration>
    <initSql>ALTER SESSION SET NLS_LANGUAGE='ENGLISH';</initSql>
</configuration>
```