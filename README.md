#include <stdio.h>
#include <conio.h>
#include <stdlib.h>
#include <string.h>
#include <math.h>

double otd (int , double );

int main()

{

    char a[30],b[20];
    int i,j,d,p=1,q;
    double c,e,f;


    while(p<2)
{
    system("cls");
    printf("Octal to Decimal!!!\nby scompiler!\n");
    printf("\nEnter 1 for converting octal to decimal:\n");
    printf("Enter 2 for exit:\n ");
    scanf("%d",&q);

    if(q==1)
    {
        printf("Enter any octal number : ");
        scanf("%s",a);
        j=strlen(a);
        /*for (i=0;i<j;i++)
        {
            if (a[i] == '.')
                break;
            else
                b[i]=a[i];
        }*/
        c=atof(a);
        d=atoi(a);
        e=c-d;

        f=otd(d,e);
        printf("%f\n",f);
        system("pause");
    }

    else
        p=3;

}
return 0;

}

double otd (int x, double y)
{
    int i=0,j=(-1),m,g=0;
    double h,k,n ;
   while(x!=0)
    {
        g+=((x%10) * pow(8,i));
        x/=10;
        i++;
    }
  while(y!=0)
  {
    k=y*10;
    m=(int)k;
    h+=( m * pow(8,j));
    j-=1;
    y=k-m;
  }
  n=(((double)g)+h);

 return(n);
}
