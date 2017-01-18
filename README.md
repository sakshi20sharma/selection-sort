# selection-sort
/*Selection sort is a sorting technique in which the first element is considered as the ṁinimum element(which may be or may not be) and the element is compared to the resst if the array. If a smaller element is found, it is swapped with the first element. Then we move on to the second element, do the comparison and the process continues until whole array is sorted.*/


#include<stdio.h>

int main()
{
    int n, i, min, j;
    printf("enter no. of elements \n");
    scanf("%d", &n);
    int a[n];
    for( i = 0; i < n; i++ )        //not taking user input
    {
        a[i] = n-i; 
    }
    for( i = 0; i < n; i++ )
    {
        min = i;
        for( j = i+1; j < n; j++ )
        {
            if( a[min] > a[j] )
                min = j;    
        }
        int temp = a[i];
        a[i] = a[min];
        a[min] = temp;
    }
    printf("Sorted array:\n");
    for( i = 0; i < n; i++ )
    {
        printf(" \t a[i] " );
    }
    return 0; 
} 
