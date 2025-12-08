## What keyword is used to define a structure in C?
```c
a) struct
b) union
c) typedef
d) define
```
- a)struct
## Which of the following statements is true about accessing members of a structure?
```c
a) Members are accessed using the dot (.) operator.
b) Members are accessed using the arrow (->) operator.
c) All members must have the same data type.
d) Structures cannot hold members of different data types.
```
- a) Members are accessed using the dot (.) operator.
## What is the size of a structure in memory?
```c
a) The size is always equal to the size of its largest member.
b) The size is the sum of the sizes of all its members.
c) The size depends on the compiler implementation.
d) Structures do not occupy any memory space
```
- c) The size depends on the compiler implementation.
## What is the difference between a structure and a union?
```c
a) Structures cannot hold different data types, while unions can.
b) Unions can only hold one value at a time, while structures can hold multiple values.
c) Structures are used for grouping related data, while unions are used for memory optimization.
d) All of the above.
```
- b) Unions can only hold one value at a time, while structures can hold multiple values.
## Which of the following statements is NOT valid for initializing a structure?
```c
a) Using a comma-separated list of values inside curly braces.
b) Assigning another structure variable of the same type.
c) Using individual assignment statements for each member.
d) Initializing only some members, leaving others undefined.
```
- d) Initializing only some members, leaving others undefined
## What is the purpose of the -> operator when accessing members of a structure?
```c
a) It is used to access members of a structure pointer variable.
b) It is used to modify members of a structure by reference.
c) It is an alternative way to access members of any structure.
d) It is not a valid operator for accessing structure members.
```
- a) It is used to access members of a structure pointer variable.
## How can you pass a structure by value to a function in C?
```c
a) By passing the structure name directly.
b) By passing the structure variable using the & (address-of) operator.
c) By creating a pointer to the structure and passing the pointer.
d) Structures cannot be passed by value to functions.
```
- a) By passing the structure name directly.
## What happens when you declare an array of structures?
```c
a) It creates a single structure variable that can hold multiple values.
b) It creates multiple copies of the same structure in memory.
c) It creates a contiguous block of memory to store multiple structures of the same type.
d) It creates a linked list of structures.
```
- c) It creates a contiguous block of memory to store multiple structures of the same type.
## What is padding in the context of structures?
```c
a) It is the process of adding extra bytes to the size of a structure to improve memory alignment.
b) It is a technique to optimize memory usage by storing smaller data types within larger ones. C) It is a
way to dynamically allocate memory for structures at runtime.
d) Padding is not relevant to structures in C.
```
- a) It is the process of adding extra bytes to the size of a structure to improve memory alignment.
## What is the most common use case for unions in C programming?
```c
a) To group related data of different types under a single name.
b) To store multiple values of the same type and access them interchangeably.
c) To improve code readability and maintainability.
d) To dynamically change the data type of a variable during program execution.
```
- a) To group related data of different types under a single name.
## 11. What is the difference between shallow copy and deep copy when copying structures?
```c
a) Shallow copy copies only the structure itself, while deep copy copies the members recursively.
b) Shallow copy copies the structure by value, while deep copy copies by reference.
c) Shallow copy uses the = operator, while deep copy requires a custom function.
d) There is no difference; both terms refer to the same process.
```
- a) Shallow copy copies only the structure itself, while deep copy copies the members recursively.
## 12. What is the use of self-referential structures in C?
```c
a) To represent hierarchical relationships between data, like a tree structure.
b) To create circular references that can lead to memory leaks.
c) To improve code efficiency by avoiding redundant member declarations.
d) Self-referential structures are not allowed in C.
```
- a) To represent hierarchical relationships between data, like a tree structure.
## 13. What are bit fields in C?
```c
a) A way to pack multiple small data types (like flags) into a single byte of memory.
b) A mechanism to define custom operators for user-defined data types.
c) A technique to dynamically allocate memory for structures during runtime.
d) Bit fields are not relevant to structures in C.
```
- a) A way to pack multiple small data types (like flags) into a single byte of memory.
## 14. How can you compare two structures for equality in C?
```c
a) By comparing the addresses of the structure variables.
b) By using a built-in compare function for structures.
c) By writing a custom function that compares each member individually.
d) Structures cannot be compared for equality.
```
- c) By writing a custom function that compares each member individually.
## 15. What is the potential consequence of accessing a union member that hasn’t been initialized?
```c
a) The program will crash due to undefined behavior.
b) The value accessed will be the same as the previously accessed member.
c) The value accessed will be garbage or random data.
d) There is no consequence; any member can be accessed regardless of initialization.
```
- c) The value accessed will be garbage or random data.
## 16. What is the use of anonymous structures in C?
```c
a) To declare a structure without a name, used only once within a function.
b) To define a structure template that can be used to create multiple instances with different names.
c) To create a structure that cannot be accessed directly and must be used through a pointer.
d) Anonymous structures are not supported in C.
```
- a) To declare a structure without a name, used only once within a function.
## 17. How can you define a structure within another structure in C?
```c
a) By using nested structures, where one structure is a member of another.
b) By creating a pointer to the inner structure within the outer structure.
c) By defining both structures separately and using them independently.
d) Structures cannot be members of other structures in C.
```
- a) By using nested structures, where one structure is a member of another.
## 18. Create a structure to represent a student with the following members: name (string), roll number(int), and marks (float). Write a function to display the details of a student.
```c
#include<stdio.h>
struct student
{
        char name[10];
        int rollno;
        float marks;
};
void display(struct student s1)
{
        printf("the student details are:\n");
        printf("name = %s\n",s1.name);
        printf("roll number = %d\n",s1.rollno);
        printf("marks = %f",s1.marks);
}
int main()
{
        struct student s1={"ammu",463,300.0};
        display(s1);
return 0;
}
```
## 19. Define a union to store either an integer or a floatingpoint number. Write a function to accept the type of data (integer or float) and then read the corresponding value from the user. Store the value in the union and print it.
## 33. Analyze the following code snippet and explain the potential issue:
```c
struct person {
char name[50];
int age;
};
int main() {
struct person p1;
strcpy(p1.name, "John Doe");
p1.age = 30;
printf("Name: %s, Age: %d\n", p1.name, p1.age);
return 0;
}
```
- Name: John Doe, Age: 30
## 34. Consider the following code:
```c
union data {
int i;
float f;
};
int main() {
union data value;
value.i = 10;
printf("Float value: %f\n", value.f);
return 0;
}
```
- Explain what happens when the code prints the float value. Why might this be unexpected?
- Printing value.f after assigning value.i reads the same memory as a float. Since the bits represent an integer, not a float, the output is undefined and may appear as 0.000000 or some garbage value. This is unexpected because it does not equal 10.0.

## 35. Analyze the following code snippet and explain the potential issue:
```c
struct student {
int *marks; // Pointer to an integer
int num_subjects;
};
int main() {
struct student s1;
s1.num_subjects = 5;
s1.marks = malloc(s1.num_subjects * sizeof(int)); // Allocate memory for marks
// ... (use s1.marks to store marks)
free(s1.marks); // Deallocate memory
return 0;
}
```
- Explain what happens if the code doesn't call free(s1.marks) before exiting the function.
- Answer:
- `s1` is a local variable created in the **stack frame** of `main`. Its pointer `marks` holds the base address of memory allocated on the **heap** using -`malloc`. If `free(s1.marks)` is not called:
- 1. The memory allocated on the **heap** is **not automatically deallocated**.
- 2. When `main` ends, `s1` goes out of scope and its stack memory is destroyed.
- 3. The base address of the heap memory is lost, making it **inaccessible**.
- 4. This results in a **memory leak**, as the allocated memory remains reserved but cannot be used again.
- Conclusion:
- Whenever memory is allocated dynamically using `malloc` (or similar functions), it is **mandatory to deallocate it using `free()`** to prevent memory leaks and - wastage of resources.
## 36. Analyze the following code snippet and explain the potential issue:
```c
struct data {
int i;
char str[20];
};
void print_data(struct data *d) {
printf("Integer: %d\n", d->i);
printf("String: %s\n", d->str);
}
int main() {
struct data d1;
d1.i = 10;
strcpy(d1.str, "Hello");
print_data(&d1);
return 0;
}
```
- Explain what happens if the strcpy function in print_data writes beyond the allocated memory for the str member.
- Writing beyond str in strcpy leads to buffer overflow, causing memory corruption, undefined behavior, crashes, or security vulnerabilities. Always ensure the copied string fits or use safer functions like strncpy.
## 19. Define a union to store either an integer or a floatingpoint number. Write a function to accept the type of data (integer or float) and then read the corresponding value from the user. Store the value in the union and print it.
```c
#include<stdio.h>
union Number
{
        int i;
        float f;
};
void readandprint()
{
        union Number num;
        int choice;
        printf("enter 1 for integer and enter 2 for float\n");
        scanf("%d",&choice);
        if(choice == 1)
        {
                printf("enter a integer number\n");
                scanf("%d",&num.i);
                printf("entered integer number is=%d\n",num.i);
        }
        else if(choice == 2)
        {
                printf("enter a float number\n");
                scanf("%f",&num.f);
                printf("entered integer number is=%f\n",num.f);
        }
        else
                printf("invalid input");
}
int main()
{
        readandprint();
        return 0;
}
```
## 20. Define a structure to represent a point in 2D space with x and y coordinates (both integers). Write a function to check if two points are equal (have the same x and y coordinates)
```c
#include<stdio.h>
struct Point
{
        int x,y;
};
int areequal(struct Point p1, struct Point p2)
{
        if((p1.x == p2.x) && (p1.y == p2.y))
                return 1;
        else
                return 0;
}
int main()
{
        int res;
        struct Point a;
        struct Point b;
        printf("enter x and y coordinates for point 1\n");
        scanf("%d%d",&a.x,&a.y);
        printf("enter x and y coordinates for point 2\n");
        scanf("%d%d",&b.x,&b.y);
        res=areequal(a,b);
        if(res)
                printf("both points are Equal");
        else
                printf("points are not Equal");
        return 0;
}
```
## 21. Create a structure to represent a book with the following members: title (string), author (string), ISBN (long int), and number of pages (int). Write a function to accept details of a book from the user and store them in a structure variable.
```c
#include<stdio.h>
struct Book
{
        char title[100];
        char author[100];
        long isbn;
        int nop;
};
void fun()
{
        struct Book b;
        printf("enter title of the book\n");
        fgets(b.title,50,stdin);
        printf("enter name of the author\n");
        fgets(b.author,20,stdin);
        printf("enter isbn number of the book\n");
        scanf("%ld",&b.isbn);
        printf("enter number of pages of the book\n");
        scanf("%d",&b.nop);
        printf("details of the book are\n");
        printf("Title = %s\n",b.title);
        printf("Author = %s\n",b.author);
        printf("ISBN = %ld\n",b.isbn);
        printf("Number of pages = %d",b.nop);
}
int main()
{
        fun();
        return 0;
}
```
- We can use strcspn() a string function to get clear output(without printing new lines in output)
## 22. Define a union to represent the size of a product, which can be specified in centimeters, inches, or feet. Write a function to convert the size from one unit to another (e.g., centimeters to inches).
```c
#include<stdio.h>
union Size
{
        float cm;
        float inches;
        float feet;
};
float inches_to_cm(float c)
{
        c=c*2.54;
        return c;
}
float feet_to_cm(float c)
{
        c=c*(12*2.54);
        return c;
}
float cm_to_inches(float i)
{
        i=i/2.54;
        return i;
}
float cm_to_feet(float f)
{
        f=f/(2.54*12);
        return f;
}
int main()
{
        union Size s;
        int inputunit,outputunit;
        printf("enter: \n1.centimeters\n2.inches\n3.feet\n");
        scanf("%d",&inputunit);
        if(inputunit == 1)
        {
                printf("enter a value in centimeters\n");
                scanf("%f",&s.cm);
        }
 else if(inputunit == 2)
        {
                printf("enter a value in inches\n");
                scanf("%f",&s.inches);
        }
        else if(inputunit == 3)
        {
                printf("enter a value in feet\n");
                scanf("%f",&s.feet);
        }
        else
        {
                printf("Invalid input");
                return 0;
        }
        printf("\n convert to:\n");
        printf("1.centimeters\n2.inches\n3.feet\n");
        scanf("%d",&outputunit);
        float value_in_cm,result;
        if(inputunit == 1)
                value_in_cm=s.cm;
        else if(inputunit == 2)
                value_in_cm=inches_to_cm(s.inches);
        else
                value_in_cm=feet_to_cm(s.feet);
        if(outputunit == 1)
        {
                result=value_in_cm;
                printf("Result = %.2f",result);
        }
        else if(outputunit == 2)
        {
                result=cm_to_inches(value_in_cm);
                printf("Result = %.2f",result);
        }
        else if(outputunit == 3)
        {
                result=cm_to_feet(value_in_cm);
                printf("Result = %.2f",result);
        }
        else 
        {
                printf("Invalid Output Unit");
                return 0;
        }
        return 0;
}
```
## 23. Define a structure to represent a date with day, month, and year (all integers). Write a function to check if a given year is a leap year.
```c
#include<stdio.h>
struct Date
{
        int date;
        int month;
        int year;
};
int isleap(int y)
{
        if((y%4==0 && y%100!=0)||y%400==0)
                return 1;
        else
                return 0;
}
int main()
{
        struct Date d;
        printf("enter Date: \n");
        scanf("%d",&d.date);
        printf("Enter month: \n");
        scanf("%d",&d.month);
        printf("Enter year: \n");
        scanf("%d",&d.year);
        int res=isleap(d.year);
       if(res)
               printf("year = %d is a leap year",d.year);
       else
               printf("year = %d is not a leap year",d.year);
       return 0;
}
```
## 24. Define a structure to represent a complex number with real and imaginary parts (both floats). Write a function to add two complex numbers represented by structures.
```c
#include<stdio.h>
struct Complex
{
        float real;
        float imag;
};
struct Complex add(struct Complex r1,struct Complex r2)
{
        struct Complex result;
        result.real=r1.real+r2.real;
        result.imag=r1.imag+r2.imag;
        return result;
}

int main()
{
        struct Complex c1,c2,sum;
        printf("Enter first complex number");
        scanf("%f%f",&c1.real,&c1.imag);
        printf("Enter second complex number");
        scanf("%f%f",&c2.real,&c2.imag);
        sum=add(c1,c2);
        printf("%.2f+%.2fi",sum.real,sum.imag);
        return 0;
}
```
## 28. Implement a function that takes a structure representing a date (day, month, year) and checks if the date is valid (e.g., not exceeding the number of days in a month).
```c
#include<stdio.h>
struct Date
{
        int day;
        int month;
        int year;
};
int check(struct Date d)
{
        int leap=0,days_in_mon=0;
        if((d.year%4==0 && d.year%100!=0)||d.year%400==0)
                leap=1;
        if(d.month<1||d.month>12)
        {
                printf("invalid month");
                return 0;
        }
        if(d.month==2)
        {
                days_in_mon=(leap?29:28);
        }
        else if(d.month==4 || d.month==6 || d.month==9 || d.month==11)
        {
                days_in_mon=30;
        }
        else
                days_in_mon=31;
        if(d.day<1 || d.day>days_in_mon)
        {
                printf("invalid days");
                return 0;
        }
        printf("Valid Date= %d/%d/%d",d.day,d.month,d.year);
        return 1;
}

int main()
{
        struct Date d;
        printf("Enter a date : day month year\n");
        scanf("%d",&d.day);
        scanf("%d",&d.month);
        scanf("%d",&d.year);
        check(d);
        return 0;
}
```
## 29. Define a union to represent a shape. The union can hold the dimensions of different shapes like circle (radius), rectangle (length, breadth), or triangle (base, height). Write functions to calculate the area of each shape based on the type stored in the union.
```c
#include<stdio.h>
#define PI 3.14
union Shape
{
        float radius;
        struct Rectangle
        {
                float length,breadth;
        }rect;
        struct Triangle
        {
                float base,height;
        }tri;
};
float a;
void circle_area(float r)
{
        a=PI*r*r;
        printf("The area of a Circle = %.2f",a);
}
void rectangle_area(float l, float b)
{
        a=l*b;
        printf("The area of a Rectangle = %.2f",a);
}
void triangle_area(float b, float h)
{
        a=0.5*b*h;
        printf("The area of a Triangle = %.2f",a);
}

int main()
{
        union Shape s;
        int choice;
        printf("Enter\n1:circle\n2:rectangle\n3:triangle\n");
        scanf("%d",&choice);
 if(choice == 1)
        {
                printf("Enter radius: ");
                scanf("%f",&s.radius);
                circle_area(s.radius);
        }
        else if(choice == 2)
        {
                printf("Enter length and breadth ");
                scanf("%f%f",&s.rect.length,&s.rect.breadth);
                rectangle_area(s.rect.length,s.rect.breadth);
        }
        else if(choice == 3)
        {
                printf("Enter base and height ");
                scanf("%f%f",&s.tri.base,&s.tri.height);
                triangle_area(s.tri.base,s.tri.height);
        }
        else
                printf("Invalid Choice");
        return 0;
}
```
## 31. Implement a function that takes a structure representing a time (hours, minutes, seconds) and performs basic time arithmetic (e.g., adding two time durations).
