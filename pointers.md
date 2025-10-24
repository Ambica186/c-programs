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


