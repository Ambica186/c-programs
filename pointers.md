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
##  Write the output of the following program ?
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
## Write the output of the following program ?
```c
#include <stdio.h>
void changeValue(int *ptr) {
*ptr = 30;
}
int main() {
int val = 20;
int *ptr = &val;
changeValue(ptr);
printf("%d", val);
}
```
- answer=30
## Write the output of the following program ?
```c
#include <stdio.h>
#include <stdlib.h>
int main() {
int *arr = (int *)calloc(5, sizeof(int));
for (int i = 0; i < 5; i++) {
*(arr + i) = i;
}
printf("%d", arr[3]);
free(arr);
}
```
- answwe=3
## Write the output of the following program ?
```c
#include<stdio.h>
void f(int *p, int *q)
{
p = q;
*p = 2;
}
int i = 0, j = 1;
int main()
{
f(&i, &j);
printf("%d %d", i, j);
getchar();
return 0;
}
```
- answer=0,2
## Write the output of the following program ?
```c
#include<stdio.h>
int main()
{
int a, b = 10;
a = -b--;
printf("a = %d, b = %d", a, b);
return 0;
}
```
- answer=a= -10, b=9
## Write a program to pass a 1D array to a function.
```c
#include<stdio.h>
void fun(int *arr,int size)
{
        for(int i=0;i<size;i++)
                printf("%d ",arr[i]);
}
int main()
{
        int arr[]={10,20,30,40,50};
        int size=sizeof(arr)/sizeof(arr[0]);
        fun(arr,size);
        return 0;
}
```
## Program to return more than one value from a function using call by reference
```c
#include<stdio.h>
int fun(int x,int y,int *sum,int* diff)
{
        *sum=x+10;
        *diff=y-10;
}
int main()
{
        int a,b,s,d;
        scanf("%d%d",&a,&b);
        fun(a,b,&s,&d);
        printf("%d %d",s,d);
        return 0;
}
```
## Create a function that swaps two numbers using pointers
```c
#include<stdio.h>
void fun(int *x,int *y)
{
        int temp;
        temp=*x;
        *x=*y;
        *y=temp;
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
## Implement a function that returns the length of a string using pointers
```c
#include<stdio.h>
int astrlen(char *ptr)
{
        int i=0;
        while(*ptr)
        {
                ptr++;
                i++;
        }
        return i;
}
int main()
{
        char a[10]="ambica";
        int size=astrlen(a);
        printf("%d",size);
        return 0;
}
```
## Write a program to find the maximum and minimum elements in an array using pointers
```c
#include<stdio.h>
#include<limits.h>
int main()
{
        int arr[]={8,1,4,10,12};
        int *ptr=arr;
        int min=INT_MAX;
        int max=INT_MIN;
        int n=sizeof(arr)/sizeof(arr[0]);
        for(int i=0;i<n;i++)
        {
                if(ptr[i]>max)
                {
                        max=ptr[i];
                }
                if(ptr[i]<min)
                        min=ptr[i];
        }
        printf("the maximum number=%d\n",max);
        printf("the minimum number=%d\n",min);
}
```
## Develop a function to reverse a string in place using pointers.
```c
#include<stdio.h>
#include<string.h>
void arev(char *ptr,int n)
{
        for(int i=0;i<n/2;i++)
        {
                int temp;
                temp=ptr[i];
                ptr[i]=ptr[n-1-i];
                ptr[n-1-i]=temp;
        }
}
int main()
{
        char arr[10]="linux";
        char *ptr=arr;
        int n=strlen(arr);
        arev(ptr,n);
        for(int i=0;i<n;i++)
                printf("%c",ptr[i]);
}
```
## Write a program that calculates the sum of all elements in an integer array using pointer arithmetic.
```c
#include<stdio.h>
int main()
{
        int arr[]={1,2,3,4,5};
        int *ptr=arr;
        int n=sizeof(arr)/sizeof(arr[0]);
        int sum=0;
        for(int i=0;i<n;i++)
                sum+= *(ptr+i);
        printf("%d",sum);
}
```
## Implement a function to copy one string into another using pointers, without using any standard library functions
```c
#include<stdio.h>
#include<string.h>
//char* astrcpy(char *dst , char *src)
void astrcpy(char *dst , char *src , int n)
{
 char *temp=dst;
 while((*dst=*src)!='\0')
 {
         src++;
         dst++;
 }
 for(int i=0;i<n;i++)
 {
       printf("%c",temp[i]);
       }
 //return temp;
}

int main()
{
       char arr1[10]="Linux";
       char arr2[10];
       char *ptr1=arr1;
       char *ptr2=arr2;
       int n=strlen(arr1);
       astrcpy(ptr2,ptr1,n);
       //char *ptr=astrcpy(ptr2,ptr1);
    //   for(int i=0;i<strlen(arr1);i++)
//             printf("%c ",ptr[i]);
}
```
## Write a program to compare two strings lexicographically (like the strcmp function) using pointers.
```c
#include<stdio.h>
int mystrcmp(char *ptr1, char *ptr2)
{
        while(*ptr1 && *ptr2 && (*ptr1==*ptr2))
        {
                ptr1++;
                ptr2++;
        }
        return (*ptr1-*ptr2);
}
int main()
{
        char arr1[100],arr2[100];
        printf("enter first string\n");
        scanf("%s",arr1);
        printf("enter second string \n");
        scanf("%s",arr2);
        char *ptr1=arr1,*ptr2=arr2;
        int res=mystrcmp(ptr1,ptr2);
        if(res==0)
                printf("both strings are equal");
        else if(res>0)
                printf("first string is greater than second string");
        else
                printf("second string is greater than first string");
}
```
## Develop a function to reverse an array of integers in place using pointers.
```c
#include<stdio.h>
void mystrrev(int *ptr1, int n)
{
        for(int i=0;i<n/2;i++)
        {
                int temp=ptr1[i];
                ptr1[i]=ptr1[n-1-i];
                ptr1[n-1-i]=temp;
        }
        for(int i=0;i<n;i++)
                printf("%d ",ptr1[i]);
}

int main()
{
        int arr[]={10,20,30,40,50};
        int *ptr1=arr;
        int n=sizeof(arr)/sizeof(arr[0]);
        mystrrev(ptr1,n);
}
```
## Write a program to find the largest element using Dynamic Memory Allocation.
```c
#include<stdio.h>
#include<stdlib.h>
#include<limits.h>
int main()
{
        int n;
        printf("enter number of elements");
        scanf("%d",&n);
        int *ptr;
        ptr = malloc(n*sizeof(int));
        if(ptr==NULL)
        {
        return 1;
        }
        for(int i=0;i<n;i++)
        {
           scanf("%d",&ptr[i]);
        }
        int max=INT_MIN;
        for(int i=0;i<n;i++)
        {
                if(ptr[i]>max)
                {
                        max=ptr[i];
                }
        }
        printf("the maximum number in the array = %d",max);
        free(ptr);
        ptr=NULL;
        return 0;
}
```
## Write a program in C to calculate the length of a string using a pointer
```c
#include<stdio.h>
void astrlen(char *ptr)
{
        int i=0;
        while(*ptr != '\0')
        {
                ptr++;
                i++;
        }
        printf("the length of string = %d",i);
}

int main()
{
        char str[10];
        printf("enter a string");
        scanf("%s",str);
        char *ptr=str;
        astrlen(ptr);
}
```
## Write a program to swap elements using call by reference.
```c
#include<stdio.h>
void swap(int *p,int *q)
{
        int temp=*p;
             *p=*q;
             *q=temp;

}

int main()
{
        int a,b;
        printf("enter two numbers");
        scanf("%d%d",&a,&b);
        int *p=&a;
        int *q=&b;
        swap(p,q);
        printf("%d %d",a,b);
}
```
## Write a program to find the factorial of a given number using pointers.
```c
#include<stdio.h>
int main()
{
        int n;
        int fact=1;
        scanf("%d",&n);
        int *ptr=&n;
        while(*ptr>0)
        {
                fact=fact*(*ptr);
                (*ptr)--;
        }
        printf("%d",fact);
        return 0;
}
```
## Write a program to count the number of vowels and consonants in a string using a pointer.
```c
#include<stdio.h>
#include<string.h>
int main()
{
        char a[100];
        printf("enter a string");
        gets(a);
        char *p=a;
        int n=strlen(a);
        int v_count=0,c_count=0;
        for(int i=0;i<n;i++)
        {
                if(*p=='a'||*p=='e'||*p=='i'||*p=='o'||*p=='u'||*p=='A'||*p=='E'||*p=='I'||*p=='O'||*p=='U')
                        v_count++;
                else if (*p >= 'A' && *p <= 'Z' || *p >= 'a' && *p <= 'z')
                        c_count++;
                p++;
        }
        printf("number of vowels in a string =%d\n",v_count);
        printf("number of consonants in a string = %d",c_count);
        return 0;
}
```
## Write a program to sort an array using a pointer
```c
#include<stdio.h>
int main()
{
        int arr[]={10,2,20,6,8};
        int *p=arr;
        int n=sizeof(arr)/sizeof(arr[0]);
        for(int i=0;i<n-1;i++)
        {
                for(int j=0;j<n-i-1;j++)
                {
                        int temp;
                        if(*(p+j) > *(p+j+1))
                        {
                                temp=*(p+j);
                                *(p+j)=*(p+j+1);
                                *(p+j+1)=temp;
                        }
                }

        }
        for(int i=0;i<n;i++)
                printf("%d ",*(p+i));
        return 0;
}
```
## Write a program to demonstrate how a function returns a pointer.
```c
#include<stdio.h>
int* getmax(int *x, int* y)
{
        if(*x>*y)
                return x;
        else
                return y;
}
int main()
{
        int a=10,b=20;
        int *p;
        p=getmax(&a,&b);
        printf("the greatest number=%d , it's address=%p",*p,p);
        return 0;
}
```
## Write a program to compute the sum of all elements in an array using pointers
```c
#include<stdio.h>
int main()
{
        int arr[]={10,20,30,40,50};
        int *p=arr;
        int sum=0;
        int n=sizeof(arr)/sizeof(arr[0]);
        for(int i=0;i<n;i++)
        {
                sum+=*p;
                p++;
        }
        printf("sum=%d",sum);
        return 0;
}
```
## Write a program to print the elements of an array in reverse order
```c
#include<stdio.h>
int main()
{
        int arr[]={10,20,30,40,50};
        int temp;
        int n=sizeof(arr)/sizeof(arr[0]);
        for(int i=0;i<n/2;i++)
        {
                temp=arr[i];
                arr[i]=arr[n-1-i];
                arr[n-1-i]=temp;
        }
        for(int i=0;i<n;i++)
                printf("%d ",arr[i]);
        return 0;
}
```
## Write the output of the following program ?
```c
#include<stdio.h>
int main()
{
int a = 12;
void *ptr = (int *)&a;
printf("%d", *ptr);
getchar();
return 0;
}
```
- ans:-compilation error
- Because:
-ptr is a void pointer
-A void pointer does not have a type, so it cannot be dereferenced directly
-You must typecast it back before dereferencing
-printf("%d",*(int *)ptr);---> ans:- 12
## Write the output of the following program ?
```c
int main()
{
int array[5][5];
printf("%d",( (array == *array) && (*array == array[0]) ));
return 0;
}
```
-ans:- 1
- array,*array,array[0] refers to same memory location.
## Write the output of the following program ?
```c
#include<stdio.h>
int main()
{
int x = 10;
int *y, **z;
y = &x;
z = &y;
printf("x = %d, y = %d, z = %d\n", x, *y, **z);
return 0;
}
```
-ans:-x=10,y=10,z=10
## Write the output of the following program ?
```c
#include <stdio.h>
int main()
{char a = 30;
char b = 40;
char c = 10;
char d = (a * b) / c;
printf ("%d ", d);
return 0;
}
```
-ans:- d=120
## Write the output of the following program ?
```c
#include <stdio.h>
int main()
{
int arr[] = {};
printf("%d", sizeof(arr));
return 0;
}
```
- ans:-0,(in standard c-it's an error) 
## Write the output of the following program ?
```c
#include<stdio.h>
int main()
{
int a[2][3] = {2,1,3,2,3,4};
printf("Using pointer notations:\n");
printf("%d %d %d\n", *(*(a+0)+0), *(*(a+0)+1), *(*(a+0)+2));
printf("Using mixed notations:\n");
printf("%d %d %d\n", *(a[1]+0), *(a[1]+1), *(a[1]+2));
return 0;
}
```
-ans:-
-Using pointer notations:
-2 1 3
-Using mixed notations:
-2 3 4
## Write the output of the following program ?
```c
int main() {
int a = 10, *j;
void *k;
j = k = &a;
j++;
k++;
return 0;
}
```
-ans:- no output or error , void pointer cannot be incremented because it does not have a fixed size
