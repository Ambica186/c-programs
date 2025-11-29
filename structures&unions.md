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
