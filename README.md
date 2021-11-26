[Звіт LAB №1!!! (1).docx](https://github.com/Gurka-202/labs/files/7606031/LAB.1.1.docx)
#include <stdio.h>
#include <stdlib.h>
#include <conio.h>
#include <math.h>
int main()
{

 unsigned int var; // 1 або 2— допустимі значення, які може приймати змінна variant
    int N, n, i;
    //int n;
    double  delta, X1, X2, Y;


    printf("Enter variant 1 or 2:");
    scanf("%u", &var);
    while(var != 1 && var != 2 )
    {
    printf("ERROR.INVALID DATA.\n");
    printf("Enter variant 1 or 2:\n");
    scanf("%u", &var);
    }

    if(var == 1)
        {
printf("\nX1: ");
scanf("%lf",&X1);
printf("\nX2: ");
scanf("%lf", &X2);
printf("\nN = ");
scanf("%lu", &N);

while(N < 0)
        {
            printf("!!!  N must be >= 0 !!!");
            scanf("%u", &N);
        }

        if(N == 0)
        {
            printf("O_o Mission complete. Have a nice day!");
            getch();
            exit(0);
        }


       printf("\n********************************************************************");
       printf("\n|   N                |             X              |           Y    |");
       printf("\n********************************************************************");
       int i=1;
       delta=(X2-X1)/(N-1);
       for(i;i<=N;i++)
       {
 Y=X1*2*X2;
printf("\n|%3.0d|%22.0f|%28.2f|\n",i, X1, Y);

if(i%1==0)
{

 printf("\nPress any key to continue...");
                         getch();
}
    X1=X1+delta;
    }
    }

    if(var == 2)
    {
  printf("\n X1: ");
                             scanf("%lf",&X1);
                              printf("\n X2: ");
                              scanf("%lf",&X2);
                               printf("\ndelta:");
                                scanf("%lf",&delta);
        int i=1;

       printf("\n********************************************************************");
       printf("\n|  N                |             X           |               F(x) |");
       printf("\n********************************************************************");
                                  while(X1<=X2)


        {
                Y=2*X2*X1;
                printf("\n|%3.0d|%22.0f|%28.0f|\n",i,X1,Y);
                if(i%1==0)
                {
                printf("\nPress any key to continue...");
                getch();
                }
                X1=X1+delta;
                i++;
                }
     }
    return 0;
            }
