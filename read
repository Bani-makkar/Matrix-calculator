Matrix 1 = arr[][] , Matrix 2 = brr[][]  and Result Matric =crr[][]:
Row = r,  Columns = c, 

#include<stdio.h>
void getmatrix(int r, int c, int arr[r][c], char name)
{
    printf("enter the name of matrix %c :\n", name);
    for(int i=0; i<r; i++)
    {
        for(int j=0; j<c; j++)
        {
            printf("enter the elements of the matrix [%d][%d] :", i+1, j+1);
            scanf("%d" ,&arr[i][j]);
        }
    }
}
void printmatrix(int r, int c, int crr[r][c])
{
    printf("Resultant matrix(crr):\n");
    for(int i=0; i<r; i++)
    {
        for(int j=0; j<c; j++)
        {
            printf("%d\t" ,crr[i][j]);
        }
        printf("\n");
    }
}
void addmatrices(int r, int c, int arr[r][c], int brr[r][c], int crr[r][c])
{
    for(int i=0; i<r; i++)
    {
        for(int j=0; j<c; j++)
        {
            crr[i][j] = arr[i][j] + brr[i][j];
        }
    }
}
void submatrices(int r, int c, int arr[r][c], int brr[r][c], int crr[r][c])
{
    for(int i=0; i<r; i++)
    {
        for(int j=0; j<c; j++)
        {
            crr[i][j] = arr[i][j] - brr[i][j];
        }
    }
}
void multiplymatrices(int r1, int c1, int arr[r1][c1], int r2, int c2, int brr[r2][c2], int crr[r1][c2])
{
    for(int i=0; i<r1; i++)
    {
        for(int j=0; j<c1; j++)
        {
            crr[i][j] = 0;
            for(int k=0; k<c1; k++)
            {
                crr[i][j] = crr[i][j] + (arr[i][k] * brr[k][j]);
            }
        }
    }
}
void transpose(int r, int c, int arr[r][c], int brr[c][r])
{
    for(int i=0; i<r; i++)
    {
        for(int j=0; j<c; j++)
        {
            brr[j][i] = arr[i][j];
        }
    }
}

int main()  {
    int choice, r, c;
    printf("matrix calculator\n");
    printf("choose an operation:\n1. Addition\n2. Subtraction\n3. multiplication\n4. transpose\n");
    printf("enter your choice : ");
    scanf("%d" ,&choice);
    if(choice == 1 || choice == 2)
    {
        printf("enter the value of r:");
        scanf("%d" ,&r);
        printf("enter the value of c:");
        scanf("%d" ,&c);
        int arr[r][c], brr[r][c], crr[r][c];
        getmatrix(r, c, arr, 'A');
        getmatrix(r, c, brr, 'B');
        if(choice == 1) 
        {
            addmatrices(r, c, arr, brr, crr);
        }
        else {
            submatrices(r, c, arr, brr, crr);
        }
        printmatrix(r, c, crr);
    }
    else if(choice == 3)  {
        int r1, c1, r2, c2;
        printf("enter the value of r1 for arr:");
        scanf("%d" ,&r1);
        printf("enter the value of c1 for arr:");
        scanf("%d" ,&c1);
        printf("enter the value of r2 for brr;");
        scanf("%d" ,&r2);
        printf("enter the value of c2 for brr:");
        scanf("%d" ,&c2);
        if(c1 != r2) 
        {
            printf("matrices cannot be multiplied. Colums of first matrix(arr), must equal rows of second matrix(brr)\n");
            return 1;
        }
        int arr[r1][c1], brr[r2][c2], crr[r1][c2];
        getmatrix(r1, c1, arr, 'A');
        getmatrix(r2, c2, brr, 'B');
        multiplymatrices(r1, c1, arr, r2, c2, brr, crr);
        printmatrix(r1, c2, crr);
        }
        else if ( choice == 4) 
        {
            printf("enter the value of r:");
            scanf("%d" ,&r);
            printf("enter the value of c:");
            scanf("%d" ,&c);
            int arr[r][c], brr[r][c];
            getmatrix(r, c, arr, 'A');
            transpose(r, c, arr, brr);
            printmatrix(c, r, brr);
        }
        else {
            printf("Invaild choice\n");
        }
    
    return 0;
}
