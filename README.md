#杨辉三角
#include <stdio.h>
#include <stdlib.h>

int nn(int n)
{
    int i,x=1;
    for(i=1;i<=n;i++)
        x=x*i;
        return x;

};

void K(int m,int n)
{
    int i;
    for(i=0;i<(n-m);i++)
        printf(" ");
}

void YH1()
{
    int n=1;
    printf("请输入杨辉三角阶数：");
    scanf("%d",&n);
    int m,i;
    printf("=================\n");
    for(i=0;i<n;i++)
    {
        for (m=0;m<=i;m++)
        printf("%d ",nn(i)/nn(i-m)/nn(m));
        printf("\n");
    }
    printf("=================\n");
}
void YH2()
{

    int n=1;
    printf("请输入杨辉三角阶数：");
    scanf("%d",&n);
    int m,i;
    printf("=================\n");
    for(i=0;i<n;i++)
    {
        K(i+1,n);
        for (m=0;m<=i;m++)
            printf("%d ",nn(i)/nn(i-m)/nn(m));
        K(i+1,n);
        printf("\n");
    }
    printf("=================\n");
}
