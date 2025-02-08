#include<stdio.h>
 table(int a);

int main()
{
    int x;
    printf("Enter a number greater than 1 for multiplication : ");
    scanf("%d",&x);

     table(x);
    return 0;
}

 table(int a)
{
    if( a<1)
        printf("Enter the number greater than 1 :");
    else{
        for(int i=1;i<=15;++i){
        printf("%d X %d = %d\n",i,a,a*i);

    }

}
}
