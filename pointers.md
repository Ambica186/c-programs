## Write a Program to print the address of variables using the address operator.
```c
#include<stdio.h>
int main()
{
        int a;
        scanf("%d",&a);
        printf("the address of a variable=%p",(void*)&a);
}
```
- (void*) → safely converts the address to a generic pointer type (void*), as required by the C standard.

## Write a program to print size of pointer variables.
```c
#include<stdio.h>
int main()
{
        int *ptr;
        float *fptr;
        char *cptr;
        short *sptr;
        printf("the size of integer pointer = %d\n",sizeof(ptr));
        printf("the size of float pointer = %d\n",sizeof(fptr));
        printf("the size of character pointer = %d\n",sizeof(cptr));
        printf("the size of short integer pointer = %d\n",sizeof(sptr));
        if(sizeof(void*)==4)
                printf("your laptop is 32-bits system so any pointer stores 4bytes");
        if(sizeof(void*)==8)
                printf("your laptop is 64-bits system so any pointer stores 8bytes");
}
```
## Write a program to print size of pointer variables and size of values Dereferenced by them.
```c
#include<stdio.h>
int main()
{
        int a=10;
        float b=12.2;
        char c='a';
        int *iptr=&a;
        int *fptr=&b;
        int *cptr=&c;
        printf("size of int pointer variable= %d\n",sizeof(iptr));
        printf("size of dereferenced variable of type int = %d\n",sizeof(a));
        printf("size of float pointer variable= %d\n",sizeof(fptr));
        printf("size of dereferenced variable of type float= %d\n",sizeof(b));
        printf("size of char pointer variable= %d\n",sizeof(cptr));
        printf("size of dereferenced variable of type char= %d\n",sizeof(c));
}
```
## Write a program to illustrate the dereferencing of pointers
```c
#include<stdio.h>
int main()
{
        int a=10;
        int *ptr;
        ptr=&a;
        printf("the value of a = %d\n",a);
        printf("the address of a = %p\n",&a);
        printf("the value stored in ptr = %p\n",ptr);
        printf("the value at ptr is(dereferenced variable)=%d\n",*ptr);
        *ptr=50;
        printf("the value at ptr is(dereferenced variable)=%d\n",*ptr);
        printf("the value stored in a =%d",a);
}
```
## C program to illustrate pointer arithmetic
```c
#include <stdio.h>

int main() {
    int arr[] = {10, 20, 30, 40};
    int *ptr = arr;                     // Pointer to first element
    int n = sizeof(arr)/sizeof(arr[0]); // Array size

    printf("Initial pointer: %p, value = %d\n", ptr, *ptr);

    // Postfix increment
    printf("\nPostfix increment (ptr++):\n");
    printf("Before increment: %p, value = %d\n", ptr, *ptr);
    printf("After increment:  %p, value = %d\n", ptr++, *ptr); // ptr moves after printing
    // Note: *ptr now points to next element

    // Prefix increment
    printf("\nPrefix increment (++ptr):\n");
    printf("Pointer after prefix increment: %p, value = %d\n", ++ptr, *ptr);

    // Postfix decrement
    printf("\nPostfix decrement (ptr--):\n");
    printf("Before decrement: %p, value = %d\n", ptr, *ptr);
    printf("After decrement:  %p, value = %d\n", ptr--, *ptr);
    // Note: *ptr now points to previous element

    // Prefix decrement
    printf("\nPrefix decrement (--ptr):\n");
    printf("Pointer after prefix decrement: %p, value = %d\n", --ptr, *ptr);

    return 0;
}
```
## Write a Program to print the value and address of elements of an array using pointers notation.
```c
#include<stdio.h>
int main()
{
        int arr[]={10,20,30,40,50};
        int *ptr=arr;
        int n=sizeof(arr)/sizeof(arr[0]);
        for(int i=0;i<n;i++)
        {
                printf("value=%d,address=%p\n",*(ptr+i),(ptr+i));
        }
        return 0;
}
/*
 * #include <stdio.h>

int main()
{
    int arr[] = {10, 20, 30, 40, 50};
    int *ptr = arr;
    int n = sizeof(arr) / sizeof(arr[0]);

    for (int i = 0; i < n; i++)
    {
        printf("value = %d, address = %p\n", *ptr, ptr);
        ptr++;  // move pointer to the next element
    }

    return 0;
}
*/
```
## Write a program to print the value of array elements using pointers and subscript notation.
```c
#include<stdio.h>
int main()
{
        int arr[]={10,20,30,40,50};
        int *ptr=arr;
        int n=sizeof(arr)/sizeof(arr[0]);
        printf("subscript notations\n");
        for(int i=0;i<n;i++)
        {
                printf("%d\n",ptr[i]);
                printf("%d\n",i[ptr]);
        }
        printf("pointers notations");
        for(int i=0;i<n;i++)
        {
                printf("%d\n",*(ptr+i));
                printf("%d\n",*(i+ptr));
        }
        return 0;
}

```
## Write a program to print the value and address of array elements by subscripting a pointer variable.
```c
#include <stdio.h>

int main()
{
    int arr[] = {10, 20, 30, 40, 50};
    int *ptr = arr;
    int n = sizeof(arr) / sizeof(arr[0]);

    printf("Value\tAddress\n");
    for (int i = 0; i < n; i++)
        printf("%d\t%p\n", ptr[i], &ptr[i]);

    return 0;
}
```
## Answer following question
```c
# include <stdio.h>
void fun(int *ptr)
{
*ptr = 30;
}
int main()
{
int y = 20;
fun(&y);
printf("%d", y);
return 0;
}
```
- answer=30
## Answer following question
```c
include <stdio.h>
void fun(int x)
{
x = 30;
}
int main()
{
int y = 20;
fun(y);
printf("%d", y);
return 0;
}
```
- ans=20
## Write a program to dereference a pointer to an array.
```c
#include<stdio.h>
int main()
{
        int arr[]={10,20,30,40,50};
        int (*ptr)[5]=&arr;
        for(int i=0;i<5;i++)
                printf("%d\n",(*ptr)[i]);
        return 0;
}
```
## Program to understand the difference between a to an integer and a pointer to an array of integers.
```c
#include<stdio.h>
int main()
{
        int a=10;
        int *ptr=&a;//pointer to an integer
        printf("the value of a = %d\n",a);
        printf("the address of a = %p\n",ptr);
        printf("the value at ptr= %d\n",*ptr);
        int arr[]={10,20,30,40,50};
        int (*ptr1)[5]=&arr;
        for(int i=0;i<5;i++)
        {
                printf("%d\n",(*ptr1)[i]);
                printf("%p\n",&(*ptr1)[i]);
        }
}
```
## program to print the values and address of elements of 2-d array.
```c
#include<stdio.h>
int main()
{
        int arr[3][3];
        for(int i=0;i<3;i++)
        {
                for(int j=0;j<3;j++)
                {
                        scanf("%d",&arr[i][j]);
                }
        }
        for(int i=0;i<3;i++)
        {
                for(int j=0;j<3;j++)
                {
                        printf("\narr[%d][%d]= %d and address= %p",i,j,arr[i][j],(void*)&arr[i][j]);
                }
                printf("\n");
        }
}
```
## Program to print elements of a 2-D array by subscripting a pointer to an array variable.
```c
#include<stdio.h>
int main()
{
        int arr[3][3];
        int (*ptr)[3]=arr;
        for(int i=0;i<3;i++)
        {
                for(int j=0;j<3;j++)
                {
                        scanf("%d",&ptr[i][j]);
                }
        }
        for(int i=0;i<3;i++)
        {
                for(int j=0;j<3;j++)
                {
                        printf(" %d ",ptr[i][j]);
                }
                printf("\n");
        }
}
```
## Program to print elements of a 3-D array using pointer notation.
```c
#include<stdio.h>
int main()
{
        int arr[2][3][3];
        int (*ptr)[3][3]=arr;
        for(int i=0;i<2;i++)
        {
                for(int j=0;j<3;j++)
                {
                        for(int k=0;k<3;k++)
                        {
                        scanf("%d",&ptr[i][j][k]);
                        }
                }
        }
        for(int i=0;i<2;i++)
        {
                for(int j=0;j<3;j++)
                {
                        for(int k=0;k<3;k++)
                        {
                                printf(" %d ",ptr[i][j][k]);
                        }
                        printf("\n");
                }

                printf("\n");
        }
}
```
## Write a simple program for call by value.
```c
#include<stdio.h>
int fun(int x, int y)
{
        x+=10;
        y+=10;
        printf("%d %d",x,y);

}


int main()
{
        int a,b;
        scanf("%d%d",&a,&b);
        fun(a,b);
        printf("\n%d %d",a,b);
        return 0;
}
```
## Write a simple program for call by reference.
```c
#include<stdio.h>
void fun(int *x, int *y)
{
        //printf("%d %d",*x,*y);
        *x+=10;
        *y+=5;
}


int main()
{
        int a,b;
        scanf("%d%d",&a,&b);
        fun(&a,&b);
        printf("%d %d",a,b);
        return 0;
}
```

  
