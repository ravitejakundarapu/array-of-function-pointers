# array-of-function-pointers
Simple calculator with array of function pointers... 
#include<stdio.h>
int add(int n1,int n2);
int subtract(int n1,int n2);
int multiply(int n1,int n2);
int divide(int n1,int n2);
int main(){
    int x,y,choice,result;
    int(*op[4])(int,int);
    op[0]=add;
    op[1]=subtract;
    op[2]=multiply;
    op[3]=divide;
    printf("enter two integers:");
    scanf("%d %d",&x,&y);
    printf("enter \n 0 to add\n 1 to subtract \n 2 to multiply \n 3 to divide\n");
    printf("your choice:");
    scanf("%d",&choice);
    result=op[choice](x,y);
    printf("%d",result);
    return 0;
}
int add(int x,int y){
    return(x+y);
}
int subtract(int x,int y){
    return(x-y);
   
}
int multiply(int x,int y){
    return(x*y);
}
int divide(int x,int y){
    if(y!=0)
    return(x/y);
    else
    return 0;
}
