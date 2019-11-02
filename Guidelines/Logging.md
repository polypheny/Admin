# Logging

This file describes how to handle logging in Polypheny-DB.

## Logger Annotation

We use Project Lombok for creating the logger field. It is therefore only required to add the `@Slf4j` Annotation to the class.

```java
@Slf4j
public class LogExample {
  
    public void foo() {
        log.error("A sophisticated log message");
    }
  
}
```


## Guards

Use appropriate logging levels and make sure that there are "guards" in front of the lower levels. Use something like:

```java
if ( LOGGER.isTrace() ) {

    LOGGER.trace( "..." + foo + "..." + getSomething() + "..." );

}
```

This is especially important if additional method calls are required in order to prepare the log message. Furthermore, a guard avoids unnecessary concatenations and expression evaluations.

