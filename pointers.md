## Write a Program to print the address of variables using the address operator.
```c
#include<stdio.h>
int main()
{
        int a;
        scanf("%d",&a);
        printf("the address of a variable=%p",(void*)a);
}
```
-(void*) → safely converts the address to a generic pointer type (void*), as required by the C standard.
