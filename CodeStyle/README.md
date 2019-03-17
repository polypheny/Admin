# Code Style
All Polypheny-DB projects follow an modified and extended version of the [Google Java Style Guide](https://google.github.io/styleguide/javaguide.html). The most recent Google Style Guides can be found [here](https://github.com/google/styleguide).

The IntelliJ Code Style definition can be downloaded here: 
[Polypheny-DB-Style.xml](Polypheny-DB-Style.xml)

The following sections introduce Polypheny-DB specific changes.


## Indents 
Indentations are made with **4 spaces**.


## Getter & toString()
IMPORTANT: Getter and `toString()` **must not** have any side effects.


## Vertical whitespace around
  * Methods: 2
```
lang=java
public Constructor() {
  this(0);
}


public Constructor(final int foo) {
}


private void foo() {
}


private void bar() {
}
```
  * Initializers: 2
```
lang=java
private static final int INT;


static {
  INT = 2;
}


public final String var;
```
  * Classes: 2
```
lang=java
public class Mess {


    public static class Foo {
    }


    protected class Bar {
    }


}
```


## Horizontal whitespace within
  * Array initializer braces 
```
lang=java
int[] X = new int[] { 1, 3, 5, 6, 7, 87, 1213, 2 };
```
  * Method declaration parantheses
```
lang=java
public void foo( int x, int y ) {
```
  * Method call parentheses
```
lang=java
foo( 5, i );
```
  * `if` parentheses 
``` 
lang=java
if ( 0 < x && x < 10 ) {
```
  * `for` parentheses
```
lang=java
for ( int i = 0; i < x; i++ ) {
```
  * `while` parentheses
```
lang=java
while ( x != y ) {
```
  * `switch` parentheses
```
lang=java
switch ( e.getCode() ) {
```
  * `try` parentheses
```
lang=java
try ( MyResource r1 = getResource() ) {
```
  * `catch` parentheses
```
lang=java
} catch ( MyException e ) {
```
  * `synchronized` parentheses
```
lang=java
synchronized ( this ) {
```
**Additional horizontal whitespace around**
  * The unary //**not**// operator `!` (currently not possible in IntelliJ, since IntelliJ has only the option to insert spaces around //all// unary operators)
```
lang=java
while ( ! this.isStopped ) {
```


## Documentation

### @author Tag
Do not use the JavaDoc `@author` tag or a similar tag in other language. This information can always be found accurate and up to date in the git log.

