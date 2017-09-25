Sample Exam Questions
=====================

Which of the following two programs will result in an error?

Program 1:

```java
public class StaticOne {
	private int number;
	
	public static void main(String[] args) {
		this.number = 5;
	}		
}
```

Program 2:

```java
public class StaticTwo {
	private static int number;
	
	public void setNumber() {
		this.number = 1;
	}
	public static void main(String[] args) {
		(new StaticTwo()).setNumber();
	}
}
``` 
---

The following program has several problems with coding style. Identify at least five. Make sure to explain each problem you specify. You will get one point for identifying the problem and one point for your explanation, up to a maximum for 10 points for five problems.

```java
public class fraction {
	int Numerator;
	int Denominator;
	double value;
		
	fraction(int Numerator, int denom) {		
		this.Numerator = Numerator;
		this.Denominator = denom;
	}
	
	public Double GetValue() {
		value = ((double)Numerator)/Denominator;
		return value;
	}
}
```
---
What is the output of the following code fragment? This may be a trick question, so be sure to explain your answer. You may assume this code is in a valid class/method with appropriate imports, etc. In other words, compiler error because there is no main method is not the answer I am looking for.

```java
	ArrayList<String> list = new ArrayList<>();
	list.add("apple");
	list.add("zebra");
	list.add("chocolate"); 
	for(String s: list) {
		System.out.println(s);
	}
```

---
What is the output of the following code fragment? This may be a trick question, so be sure to explain your answer. You may assume this code is in a valid class/method with appropriate imports, etc. In other words, compiler error because there is no main method is not the answer I am looking for.
 
```java
	TreeMap<String, Boolean> map = new TreeMap<>();
	map.put("apple", true);
	map.put("zebra", false);
	map.put("chocolate", true);
	for(String s: map.keySet()) {
		System.out.println(map.get(s));
	}
```
---
Which of the following are *checked* exceptions?
- `FileNotFoundException`
- `ArithmeticException`
- `ArrayIndexOutOfBoundsException`
- `IOException`

---
Consider the following classes:

```java
public abstract class Beverage {

	protected int ounces;
		
	public int getSize() {
		return this.ounces;
	}
	
	public void drink() {
		System.out.println("Mmm, tasty");
	}

	public abstract String getServingGlass();
}

public class Coffee extends Beverage {
	
	protected boolean isDecaf;
	
	public Coffee(boolean isDecaf) {
		this.isDecaf = isDecaf;
	}
	
	public String getServingGlass() {
		return "Cup";
	}
	
	public boolean isDecaf() {
		return this.isDecaf;
	}	

	public void drink() {
		System.out.println("Wow, that's hot!");
	}
}
```
What is the output of the following code fragments? If the code will cause an error, explain the error.

```java
Coffee c = new Coffee(false);
System.out.println(c.getSize());

Beverage b = new Beverage();
System.out.println(b.getSize()); 

Beverage b = new Coffee(false);
System.out.println(b.isDecaf());

Beverage b = new Coffee(false);
b.drink();

Beverage b = new Coffee(false);
System.out.println(b.getServingGlass());
```
---

Which of the following are valid variable names? Select all identifiers that the compilerwill accept. Hint, the compiler does not enforce the style guidelines required for yourassignments.
- abc123- abc_123- abC123- 12ab3c- ABC_123

---
Which of the following are methods that may be called on an instance of `Scanner`.Select all that apply.
- add- next- useDelimiter- nextInt- charAt

---
What is the return type of the `equals` method of the `String` class?
- char- int- boolean- None of the above

---
Which of the following classes must be imported before they may be used in a program?Select all that apply.- java.util.ArrayList- java.lang.String- java.io.File- java.util.Scanner

---

True / False - A class must have getters and setters for all data members.
True / False - A constructor takes no parameters.True / False - All methods must have a `return` statement in the body.True / False - The `main` method in java is declared `static`. True / False - It is common practice to use all capital letters to name a constant variable.
 
 ---
 
Implement the following method `printEvensBackward`. The method takes as input an`ArrayList` of `Integer` and prints all even numbers in the list from last to first. Giventhe list [3, 5, 2, 6, 1, 6, 4] your method would print 4, 6, 6, 2. 
`public void printEvensBackward(ArrayList<Integer> numbers);`---

The following code results in a compiler error. Explain why.

```javapublic class Exam1 {	public static void main(String[] args) {		x = 10;		System.out.println("x: " + x);	}}
```