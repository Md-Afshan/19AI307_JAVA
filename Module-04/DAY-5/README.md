# Ex.No:4(E)  PARAMETERIZED CONSTRUCTOR

## AIM:

To write a parameterized constructor in the Employee class that initializes name and designation, and then call getter methods in the main() method of another class (Sample) to display the values.

## ALGORITHM :

1. Start the program.
2. Define a class `Employee`:
   - a. Declare two private string variables: `name` and `designation`.
3. Create a parameterized constructor in `Employee`:
   - a. Accept two parameters: `name` and `designation`.
   - b. Assign the parameters to the class fields.
4. Define two getter methods in the `Employee` class:
   - a. `getName()` – returns the value of `name`.
   - b. `getDesg()` – returns the value of `designation`.
5. Create another class `Sample` with the `main` method.
6. Inside the `main` method:
   - a. Create an object of `Employee` using the constructor and pass `"John"` and `"Asst.Manager"` as arguments.
   - b. Call `getName()` and store the result in a variable `empName`.
   - c. Call `getDesg()` and store the result in a variable `empDesg`.
7. Print the values of `empName` and `empDesg`.
8. End the program.

## PROGRAM:

```
/*
Program to implement a Parameterized Constructor Using Java
Developed by: Muhammad Afshan A
RegisterNumber: 212223100035
*/
```

## PROGRAM QUESTION AND SAMPLE INPUT:
![alt text](image.png)

## SOURCECODE.JAVA:

```
class Employee {
    String name;
    String desg;

    Employee(String name, String desg) {
        this.name = name;
        this.desg = desg;
    }

    public String getName() {
        return name;
    }

    public String getDesg() {
        return desg;
    }
}

public class Sample {
    public static void main(String[] args) {
        Employee emp = new Employee("John", "Asst.Manager");
        String Ename = emp.getName();
        String Edesg = emp.getDesg();
        System.out.print(Ename + "\n" + Edesg);
    }
}
```

## OUTPUT:
![alt text](image-1.png)

## RESULT:

Thus, the Java program was successfully demonstrates the use of a parameterized constructor to initialize class fields.
