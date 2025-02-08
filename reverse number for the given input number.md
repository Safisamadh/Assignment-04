#include<stdio.h>
int reversed(int a);

int main()
{
    int x;
    printf("Enter your input for get reversed number : ");
    scanf("%d",&x);
    reversed(x);
    return 0;
}
int reversed(int a){
    int x=0;
    while(a != 0){
       int ld = a % 10;
        x= ld;
        printf("%d",x);
      a /= 10;
    }

    return 0;

}
