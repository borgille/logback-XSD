# logback-spring XSD

## Overview

The purpose of this project is to provide a useful XML Schema Definition file for use in logback-spring configuration files.  This project simply extends the schema from the [logback-XSD](https://github.com/borgille/logback-XSD/blob/master/README.md) project.

A simple usage example:
```
<?xml version="1.0" encoding="UTF-8"?>
<configuration
    xmlns="http://ch.qos.logback/xml/ns/logback-spring"
    xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
    xsi:schemaLocation="http://ch.qos.logback/xml/ns/logback-spring https://raw.githubusercontent.com/enricopulatzo/logback-XSD/master/src/main/xsd/logback-spring.xsd">

    <appender name="STDOUT" class="ch.qos.logback.core.ConsoleAppender">
      <encoder>
        <pattern>%d{HH:mm:ss.SSS} [%thread] %-5level %logger{36} - %msg%n</pattern>
      </encoder>
    </appender>
    <root level="WARN">
        <appender-ref ref="STDOUT" />
    </root>
</configuration>
```
