// DAA-lab
//binary search 
#include<stdio.h>
#include<time.h>
int main(){
    int i,n,e,arr[100],c=0,p;
    printf("Enter the iimit of Array : ");
    scanf("%d",&n);
    for(i=0;i<n;i++){
        printf("Element : ");
        scanf("%d",&arr[i]);
    }
    printf("\nGiven Array is : \n");
    for(i=0;i<n;i++)
    {
        printf("%d ",arr[i]);
    }
    printf("\n\nEnter the Element to search : ");
    scanf("%d",&e);
    double ts = 0.0;
    clock_t tb = clock();
    for(i=0;i<n;i++){
        if(e == arr[i]){
            c++;
            p = i;
            break;
        }
    }
    if(c == 0){
        printf("\nElement Not Found");
    }
    else{
        printf("\nElement Found at position : %d",p+1);
    }
    clock_t te = clock();
    ts  = (double)(te - tb)/CLOCKS_PER_SEC;
    printf("\n\nElapsed time = %f sec",ts);
}
