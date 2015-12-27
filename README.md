#include<stdio.h>
void printarray(int,int[10][10]);
void main()
{
    int array[10][10],temp,i,j,size;
    printf("enter the size of the matrix");
    scanf("%d",&size);
    printf("\n Enter the elements");
    for(i=0;i<size;i++)
    {
          for(j=0;j<size;j++)
          {
              scanf("%d",&array[i][j]);
          }
    }
    //transpose of matrix
    for(i=0;i<size;i++)
    {
        for(j=i;j<size;j++)
        {
            temp=array[i][j];
            array[i][j]=array[j][i];
            array[j][i]=temp;
        }
    }
    printarray(size,array);
}
void printarray(int n,int transpose[10][10])
{
    int i,j;
    printf("\nTranspose Matrix");
    for(i=0;i<n;i++)
    {
        for(j=0;j<n;j++)
        {
            printf("%d\t",transpose[10][10]);
        }
        printf("\n");
    }
}
   
