# Ex.No:12(B)   COMPARABLE & COMPARATOR INTERFACE
## AIM :
To create and sort a list of Student objects based on the name field using a custom comparator.


## ALGORITHM :


1. **Create a `Student` class** with fields `rollno`, `name`, and `address`, and override `toString()` for display.
2. **Implement a `Comparator<Student>`** named `Sortbyname` to compare students based on their names.
3. **Take input `size`** – number of students to be added, then use a loop to create and store student objects in an `ArrayList`.
4. **Print the unsorted list** using a loop.
5. **Sort the list using `Collections.sort()`** with the `Sortbyname` comparator, then print the sorted list.

## PROGRAM:
 ```
/*
Program to implement a COMPARABLE & COMPARATOR INTERFACE using Java
Developed by: Muhammad Afshan A
RegisterNumber: 212223100035*/
```

## SOURCECODE.JAVA:
```
import java.io.*;
import java.lang.*;
import java.util.*;
class Student {
 
    int rollno;
    String name, address;
    public Student(int rollno, String name, String address)
    {
        this.rollno = rollno;
        this.name = name;
        this.address = address;
    }
    public String toString()
    {
         return this.rollno + " " + this.name + " "
            + this.address;
    }
}
class Sortbyname implements Comparator<Student> {
 
    public int compare(Student a, Student b)
    {
 
        return a.name.compareTo(b.name);
    }
}
public class Main {
    public static void main(String[] args)
    {
        ArrayList<Student> ar = new ArrayList<Student>();
        Scanner sc=new Scanner(System.in);
        int size=sc.nextInt();
        for(int i=0;i<size;i++)
        {
        ar.add(new Student(sc.nextInt(),sc.next(),sc.next()));
        }
      
        System.out.println("Unsorted");
 
        
        for (int i = 0; i < ar.size(); i++)
            System.out.println(ar.get(i));
 
         Collections.sort(ar, new Sortbyname());
 
        
        System.out.println("\nSorted by name");
 
        
        for (int i = 0; i < ar.size(); i++)
            System.out.println(ar.get(i));
 
       
    }
}

```


## OUTPUT:
![alt text](image.png)

## RESULT:
Thus the java program To create and sort a list of Student objects based on the name field using a custom comparator executed successfully.




