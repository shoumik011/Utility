# Java Utility Class

This project contains a utility class `Utility<T>` that provides various utility methods for working with lists of generic type `T`. It also includes several auxiliary classes such as `Point`, `MyInteger`, `NaturalNumber`, `OddNumber`, and `EvenNumber` to demonstrate the usage of the utility class with different data types.

## Utility Class

The `Utility<T>` class provides the following methods:

- `linearSearch(T element)`: Performs linear search to find the index of the specified element in the list.
- `mergeList(List<? super T> inputList)`: Merges the contents of the input list into the current list.
- `containList(List<? extends T> inputList)`: Checks if the current list contains all elements of the input list.
- `removeMultipleOf10(List<? extends MyInteger> myList)`: Removes elements from the list that are multiples of 10.

## Auxiliary Classes

The auxiliary classes demonstrate how to use the `Utility<T>` class with different data types:

- `Point`: Represents a two-dimensional point with custom comparison logic.
- `MyInteger`: Represents an integer number with custom comparison logic.
- `NaturalNumber`: Represents a subset of integer numbers known as natural numbers, extending `MyInteger`.
- `OddNumber`: Represents a subset of natural numbers known as odd numbers, extending `NaturalNumber`.
- `EvenNumber`: Represents a subset of natural numbers known as even numbers, extending `NaturalNumber`.

## Usage

To use the utility class and auxiliary classes:

1. Include the `Utility.java` file in your Java project.
2. Create instances of the `Utility<T>` class with appropriate type parameters.
3. Call the utility methods as needed to perform operations on lists of different data types.

## Example

```java
// Create a Utility instance for Integer
Utility<Integer> utility = new Utility<>();
List<Integer> integerList = Arrays.asList(1, 2, 3, 4, 5);
utility.setList(integerList);

// Perform linear search
int index = utility.linearSearch(3);
System.out.println("Index of element 3: " + index);

// Merge lists
List<Integer> mergeList = new ArrayList<>();
mergeList.add(6);
mergeList.add(7);
utility.mergeList(mergeList);
System.out.println("Merged list: " + utility.getList());

// Check containment
List<Integer> checkList = Arrays.asList(2, 4);
boolean contains = utility.containList(checkList);
System.out.println("Contains list [2, 4]: " + contains);

// Remove multiples of 10
List<MyInteger> myIntegerList = Arrays.asList(new MyInteger(10), new MyInteger(15), new MyInteger(20));
utility.removeMultipleOf10(myIntegerList);
System.out.println("List after removing multiples of 10: " + myIntegerList);
