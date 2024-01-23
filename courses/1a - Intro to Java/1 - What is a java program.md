# What is a java program?
As discussed in [Programming Languages](../0%20-%20Intro%20to%20computing/1%20-%20Programming%20Languages.md), Java is a compiled language that requires a runtime. How exactly does this work?

## Program entrypoint
Despite the fact that computers seems to do many things at once, they can only operate on code sequentially. Therefore, every program needs an entrypoint (a place to start). The general consensus for compiled languages is that this entrypoint should be a function called main. Looking at the code that REPL.it automatically created for you, you see a function like this:
```java
public static void main(String[] args)
```

This is the main function and where this program will always start. Now what do all those parts means?

The first part `public` allows this functions to be called by other programs not inside our program. We will cover this more later when discussing a concept called Encapsulation.

The second part `static` means that this function is pure and exists all on its own. It doesn't require an instance of the class to exist to be called. More on this during classes sections.

The third part `void` is the return type of the function. `void` means nothing will be returned. We will discuss this more in the functions and types sections of this module.

The fourth part `main` is the name of the function and by convention calling this main will let the computer know this is the entrypoint.

The final part `(String[] args)` are the parameters we can include in our function. We will talk more about parameters in the functions section, but the parameters for main are always this. By convention, computes will always allow you to pass into a program a list of arguments to change it's behavior.

## What about the rest of this stuff?
Java is an object oriented programming language. More on this later, but that means EVERYTHING is a thing known as a class. Therefore, even our entrypoint needs to exist inside a class. Again, by convention we have to put our entrypoint function `main` inside a class called `main`.

```java
class Main {
  public static void main(String[] args) {
    ...
  }
}
```

## Printing to the screen
Java has a built-in class called `System` which allows you to interact with the computer's operating system directly. This class has a static parameter which can be used directly called `out`. This has a set of functions that let's us interact with a default part of computers called `stdout`. Anytime a program writes to `stdout` it will appear on the screen. So the next part prints `Hello World!` to `stdout` so that it will appear on the screen. The `ln` part of `println` means to print it as a line which basically just means to include a newline at the end.

```java
System.out.println("Hello world!");
```

## All the green stuff
This are just comments. REPL.it includes some comments on how to include their testing framework which we will get into in the next section. In Java, any code beginning with `//` is just for reference and will not be executed or compiled.

## All done. Let's run it
Click `Run` at the top of the page and you will see `Hello World!` appear on the right hand side.

Under the hood, what is happening is REPL.it is building the Java code and then running it using the runtime and forwarding the underlying `stdout` to your browser.

# Additional Resources
https://www.w3schools.com/java/java_intro.asp
https://www.w3schools.com/java/java_getstarted.asp
https://www.w3schools.com/java/java_syntax.asp
https://www.w3schools.com/java/java_output.asp
https://www.w3schools.com/java/java_comments.asp
