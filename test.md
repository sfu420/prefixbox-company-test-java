# Prefixbox Test

## Short questions

- What is a package? How do you define a package?
```
A package is a bunch of code, it's writen by someone else and it can be imported into our projeckt. It helps sorten development time.
```
- What is a constructor? When is it executed?
```
The constructor is a part of a class, this part of code runs when we create a new instance of an object, it defines specific values for the new instance.
```
- How do you implement inheritance in Java?
```
class newChild extend Parent;
and in the constructor super() must be invoked.
```
- How do you prevent someone to inherit from a class?
```

```
- What is a final variable? Where you can assign value to final variables?
```
The value of a Final variable can't be changed. It can be assigned only at declaration.
```
- Specify the available access modifiers in Java and briefly explain them
```
public It can be reached from outside of the object.
private Only inside the object is accessible
protected Only child objects can access.
```
- Briefly explain the mechanism of exception handling
```
When the given function throws an exeption, program does not crash, instead exeption will be catched be a handler, which handles the error as we describe it in the code.
```
- What is the difference between an abstract class and an interface?
```
An interface cannot be instantiated.
```
- What is the difference between Comparator and Comparable?
- How Iterable and Iterator interface works? What methods need to exist in a
class that implements them? What is their relation to for loops?

## Programming tasks

You can write your solutions in any language, you can even write pseudo code or
using only your own words.
The point is not to make a perfectly running application, the point is the way
you think!
Don't worry if you miss a semicolon or some parantheses.
You might use the Java stream API for your solutions but none of the exercises
require them

### Palindrom

Write a function which decides whether a text is palindrom(It's the same whether
you read it forwards or backwards). E.g.: abba, rotator, stats.
You might assume that the input string is not null, the length is greater than
1 and less than one million. **Strive for the low memory complexity!**

Example:

```java
public boolean isPalindrom(String input) {
    for (i = 0, i <= (input.length % 2), i++) {
        if(!(input[i].isEqula(input[input.length-i-1]))
            return = false;
    }
    return true;
}

isPalindrom("alma"); //false
isPalindrom("görög"); //true
```

### Find The Duplicate

You have an array that contains strings. Every item in the array is
unique except one which is present in the array exactly twice.
Write a function which finds the string that is present twice in the array.
You might assume that the input array is not null, the length is greater
or equal to 2 and less than one million. **Strive for the low time complexity!**

Example:

```java
public String findTheDuplicate(String[] input) {
    for (i = 0, i < input.length-1, i++)
        for (j = i+1, j <= input.length-1, j++) {
            if(input[i].isEqual(input[]))
                return input[i];
        }
    return null;
}

String[] fruitBasket = new String[] { "apple", "banana", "coconut", "durian",
"banana", "elderberry", "fig", "grapefruit" };
findTheDuplicate(fruitBasket); //should return banana
```

### Count The Words

You have a long string that has some meaning on a real language. For example a
whole novel in a single string.
Write a function that counts the occurence of each word inside the string and
writes them to the output in the following format: `word: number of occurences`
You might assume that the input is not null and not empty. The order of the
words on the ouput does not matter.
The solution might be case insensitive, you don't have to differentiate
bwetween capital and non-capital letters.
The punctuation marks and line endings are not part of the words!

Example:

```java
public void countTheWords(String crazyLongString) {
    inputArray[] = crazyLongString.split(" ");
    HashMap<String, Number> = new HashMap<>;
    for (i = 0, i < inputArray.size, i++)
        if(HashMap has already a key with inputArray[i])
            HashMap.updateValue with (value+1) where key = inputArray[i];
        else
            HashMap.put(inputArray[i], 0);
    return HashMap.toString();
}

String boci = "Boci, boci tarka, se füle, se farka.";
countTheWords(boci);

//Output:
//boci:2
//tarka:1
//se:2
//füle:1
//farka:1
```

### What Is The Output

What is the output of the following Java application? Explain your solution!

```java
package com.mycompany.myproject;

public class Person {
    public String firstName;
    public String lastName;

    public Person(String firstName, String lastName) {
        this.firstName = firstName;
        this.lastName = lastName;
    }  

    @Override
    public String toString() {return this.firstName + " " + this.lastName;}
}

public class Main {
    public static void main(String[] args) {
        int i = 0;
        String s = "apple";
        Person p = new Person("Jonh", "Doe");

        doSomething(i, s, p);

        System.out.println(i);
        System.out.println(s);
        System.out.println(p);
    }

    public static void doSomething(int i, String s, Person p)
    {
        i = 5;
        s += "banana";
        p.lastName = "Rambo";
    }
}

Output:
5
applebanana
John Rambo

```

## SQL

- What is the PRIMARY KEY?
- What is the difference between CLUSTERED INDEX and NONCLUSTERED INDEX?
- There is a table called `Employees`. Let's assume that the columns exist
and they have the right data type.
What is going to happen if we execute the script and we destroy
the database connection during the execution? What are the possible problems
that might occure?

```sql
BEGIN TRANSACTION

UPDATE Employees
SET Salary = Salary * 1.1
WHERE
    Salary < 250000
    AND IsActiveEmployee = 1
```

## Web and HTTP

- Specify the existing HTTP request methods and describe their usage!
- What are the groups of HTTP response status codes? Write an example for each group!
