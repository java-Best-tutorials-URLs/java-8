# java-8 best understanding tutorial links 
https://www.javatpoint.com/java-8-features </br>
https://beginnersbook.com/2017/10/java-8-stringjoiner/ </br>
http://www.baeldung.com/java-8-lambda-expressions-tips </br>
https://www.codementor.io/eh3rrera/using-java-8-method-reference-du10866vx </br>
http://tutorials.jenkov.com/java/lambda-expressions.html </br>
https://blog.idrsolutions.com/2015/02/java-8-method-references-explained-5-minutes/ </br>

<h2>Advantages of Lamda</h2>
https://www.nagarro.com/de/perspectives/post/26/lambda-expressions-in-java-8-why-and-how-to-use-them
1. Fewer Lines of Code </br>
2. Sequential and Parallel Execution Support by passing behavior in methods </br>
3. Higher Efficiency (Utilizing Multicore CPU’s)</br>

<h2>Functional programming <h2>


you could think about lambda expressions as a way of supporting functional programming in Java. Functional programming is a paradigm that allows programming using expressions i.e. declaring functions, passing functions as arguments and using functions as statements (rightly called expressions in Java8). If you want to learn more about why it is called Lambda expressions, you could try to understand what Lambda Calculus is.


An Overview of OOP vs. Functional Programming
For more than a decade, OOP languages featured almost every need of the programmer and would continue to do so in many years to come, no doubt. However, there are certain situations where functional programming seems to provide a better construct of the solution.

In OOP, everything is represented as an object; therefore, every solution to a problem must be defined as a scheme of classes and their properties even if we need only to implement the behaviour. This type of situation is the niche for functional programming, where we define only the behaviour through functions and not objects. This means in functional programming we directly implement a function rather than an class that contains a function. This is the basic difference between OOP and functional programming.


Method Reference :

Method reference is used to refer method of functional interface. It is compact and easy form of lambda expression. Each time when you are using lambda expression to just referring a method, you can replace your lambda expression with method reference.

<h2>Java 8 Streams</h2>
A stream represents a sequence of elements and supports different kind of operations to perform computations upon those elements.
List<String> myList =
    Arrays.asList(""a1"", ""a2"", ""b1"", ""c2"", ""c1"");

myList
    .stream()
    .filter(s -> s.startsWith(""c""))
    .map(String::toUpperCase)
    .sorted()
    .forEach(System.out::println);
Stream operations are either intermediate or terminal. Intermediate operations return a stream so we can chain multiple intermediate operations without using semicolons. 
Terminal operations are either void or return a non-stream result. In the above example filter, map and sorted are intermediate operations whereas forEach is a terminal operation. 
For a full list of all available stream operations see the Stream Javadoc. Such a chain of stream operations as seen in the example above is also known as operation pipeline.

Stream does not store elements. It simply conveys elements from a source such as a data structure, an array, or an I/O channel, through a pipeline of computational operations.
Stream is functional in nature. Operations performed on a stream does not modify it's source. For example, filtering a Stream obtained from a collection produces a new Stream without the filtered elements, rather than removing elements from the source collection.
Stream is lazy and evaluates code only when required.
The elements of a stream are only visited once during the life of a stream. Like an Iterator, a new stream must be generated to revisit the same elements of the source

<h2>Java Stream Intermediate and Terminal Operations</h2>

Java Stream API operations that returns a new Stream are called intermediate operations. Most of the times, these operations are lazy in nature, so they start producing new stream elements and send it to the next operation. Intermediate operations are never the final result producing operations. Commonly used intermediate operations are filter and map.


 
Java 8 Stream API operations that returns a result or produce a side effect. Once the terminal method is called on a stream, it consumes the stream and after that we can’t use stream. Terminal operations are eager in nature i.e they process all the elements in the stream before returning the result. Commonly used terminal methods are forEach, toArray, min, max, findFirst, anyMatch, allMatch etc. You can identify terminal methods from the return type, they will never return a Stream.</br>
https://www.journaldev.com/2774/java-8-stream </br>



