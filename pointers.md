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


