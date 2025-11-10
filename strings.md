## Write a program in C to input a string and print it.
```c
#include<stdio.h>
#include<string.h>
int main()
{
        char arr[10];
        //strcpy(arr,"ambica");
        gets(arr);
        printf("%s",arr);
         return 0;
}
```
## Write a program in C to find the length of a string without using library functions
```c
#include<stdio.h>
#include<string.h>
void astrlen(char *ptr)
{      short i=0;
        short count=0;
        while(*(ptr+i)!='\0')
        {
                count++;
                i++;
        }
        printf("length of string = %hd\n",count);
}
int main()
{
        char arr[100];
        strcpy(arr,"ambica ammu");
        //gets(arr);
        astrlen(arr);
        printf("%s",arr);
}
```
## Write a program in C to separate individual characters from a string.
```c
#include<stdio.h>
#include<string.h>
int main()
{
        char arr[20];
        strcpy(arr,"ambica");
        char *p=arr;
        int n=strlen(arr);
        for(int i=0;i<n;i++)
        {
                printf("%c\n",*(p+i));
        }
        return 0;
}
```
## Write a program in C to print individual characters of a string in reverse order.
```c
#include<stdio.h>
#include<string.h>
int main()
{
        char arr[20];
        strcpy(arr,"ambica");
        char *p=arr;
        int n=strlen(arr);
        /*for(int i=n-1;i>0;i--)
        {
                printf("%c\n",*(p+i));
        }*/
        for(int i=0;i<n/2;i++)
        {
                char temp;
                temp=*(p+i);
                *(p+i)=*(p+(n-1-i));
                *(p+(n-1-i))=temp;
        }
       for(int i=0;i<n;i++)
               printf("%c\n",*(p+i));

        return 0;
}
```
## Write a program in C to count the total number of words in a string
```c
#include<stdio.h>
#include<string.h>
int main()
{
        char arr[100];
        strcpy(arr,"empowering students to skillfully navigate the complexities of society");
        char *p=arr;
        int n=strlen(arr);
        int count=0;
        for(int i=0;*(p+i)!='\0';i++)
        {
                if(*(p+i)!=' ' && (i==0 || *(p+i-1)==' '))
                        count++;
        }
        printf("the number of words in the string are:%d",count);
        return 0;
}
```

