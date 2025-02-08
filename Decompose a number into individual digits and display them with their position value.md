#include<stdio.h>
int find(int x);
int main(){

int input;
printf("Enter a number within 0 and 99999 : ");
scanf("%d",&input);
if(input>=0 && input <=99999){
  printf("|>......\n");
  find(input);
}
  else {
    printf("input was incorect\n Enter a number within 0 and 99999 : ");
    return 0;
  }
}
int find(int x){
  char *potition[]={"1's","10's","100's","1000's","10000's"} ;
   //potition = 0;
  for(int i=0;i<5;++i){
    int a = x %10;
    printf("No of %s = %d\n",potition[i],a);
    x /=10;
  }

}
