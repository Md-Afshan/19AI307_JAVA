# Ex.No:6(D) PACKAGES
## AIM:
To create a Java Program for accessing package from another package using packagename.

## ALGORITHM :
1. Start the Program.
2. Create a directory named `pack` and save `A.java` inside it, defining a class `A` within the `pack` package.
3. Compile `A.java` from the parent directory using `javac pack/A.java`.
4. Create another directory named `mypack` and save `B.java` inside it.
5. In `B.java`, import the `pack.A` class and create a class `B` within the `mypack` package.
6. In the `main` method of class `B`, create an instance of class `A` and call a method from it.
7. Compile `B.java` from the parent directory using `javac mypack/B.java`.
8. Run `B` from the parent directory with `java mypack.B`.
9. End the Program.

## PROGRAM:
```
/*
Program to implement Packages using Java
Developed by: Muhammad Afshan A
RegisterNumber: 212223100035
*/
```

## PROGRAM QUESTION AND SAMPLE INPUT:
**Program Question:**
Demonstrate how to access a class from one package (`pack`) within a class residing in another package (`mypack`).

**Sample Input:**
No direct input is required for this program, as it demonstrates package access. The output will confirm successful access.

---

## SOURCECODE.JAVA:

**File: pack/A.java**
```java
package pack;

public class A {
    public void displayA() {
        System.out.println("Hello from class A in 'pack' package!");
    }
}
```

**File: mypack/B.java**
```java
package mypack;

import pack.A; // Importing class A from package 'pack'

public class B {
    public static void main(String[] args) {
        A objA = new A(); // Creating an object of class A
        objA.displayA(); // Calling a method of class A
    }
}
```

---

## OUTPUT:
```
Hello from class A in 'pack' package!
```
![alt text](image.png)
---

## RESULT:
Thus, the program has accessed the package from another package has been done successfully.