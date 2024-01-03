# Introduction to Generics

### What are generics?
<p>Generics in Java allows you to create classes, interfaces and methodes that operates on data types without specifying the actual type until the code is used.</p>
<br>
<p>This enchances type safety and resuability by enabling the creation of generic classes and methods that woe with a variety of data types</p>

### Why Generic?
<p><b> Type safety: </b> Generic provides compile time type checking, reducing the risk of runtime errors. This ensures that the correct types are used enchancing the reliability of code</p>

<p><b> Code Reusability: </b> With generics you can create classes and methods that operates on different types. This promotes code resuse since the same logic is applied to various data typeswithout duplicating code :)</p>

<p><b> Type casting elimination: </b>Generics eliminate the need for explicit type casting, making the code cleaner and more readable. This also helps in avoiding potent ClassCastExeception at runtime</p>

<p><b> API Design: </b>Generics enchance API design by allowing developers to create flexible and generic interfaces and classes. This enable the development for more versatile and adaptable libraries.</p>

<p><b> Collections Framework: </b>The Java Collection Framework(JCF) extensively use generics. This results in more type-safety and efficient collections, allowing developers to work with collections of any type in standarised and type safe manner</p>

### Types of Generic in Java:

<p>There are two types of Generics in Java 1st is <b>Generic Methods</b> and 2nd is <b>Generic Classes</b></p>


### Generic Methods:
<p>i) In java Generic Method take some parameter and returns some value after completing of a task, In short generic methods in Java allows you to write an methods that can be operated on different types without specifying the type casting</p>
<p>ii) The compilers take care of the type of safety which enables programmers to code easily and since they do not have to perform long, individual type castings</p>
<br>

<p>The above code snippet:</p>

```java
// Generic method to find the maximum of two elements
public class GenericExample {
    public static <T extends Comparable<T>> T findMax(T a, T b) {
        return a.compareTo(b) > 0 ? a : b;
    }

    public static void main(String[] args) {
        System.out.println(findMax(5, 8));       // Output is 8
        System.out.println(findMax("abc", "xyz")); // Output is xyz
    }
}
```

### Generic Classes:
<p>i) A generic class is implmented exactly like non-generic class. The only difference is that it contains a type parameter section.</p>

<p>ii) There can be more than one parameter separated by comma(,)</p>

<p>iii) The classes that accepts more than one parameter are called as <b>parameterized class</b> or <b>parameterized types.</b></p>

<p>iv) Users of the generic class can use it without casting, improving code readability and reducing the risk of runtime errors.</p>

<p>v) Users of the generic class can use it without casting, improving code readability and reducing the risk of runtime errors.</p>

<b>Syntaxt for creating a Generic Class:</b>

```java
BaseType <Type> obj = new BaseType <Type>()
```
<p> Code snippet for finding the maximum number in a generic class</p>

```java

public class Box<T Comparable<T>> {
    private T content;
    //constructor
    public Box(T content) {
        this.content = content;
    }
    //Getter and setter
    public T getContent() {
        return content;
    }
    public void setcontent(T content) {
        this.content = content;
    }
    //Generic method to find maximum of two elements
    public static <T extends Comparable<T>> T findMax(T a, T b) {
        return a.compareTo(b)>0 ? a:b;
    }

    public T findMaxInBox(Box<T> anotherBox) {
        return findMax(this.getContent(),anotherBox.getContent());
    }
}

```