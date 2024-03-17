# 10-data-
10萬筆data(插入排序)
#include<stdio.h>
#include<stdlib.h>
#include<time.h>
#define number 100000

//sorting  algorithm(insertion  sort)


void insertionsort(int data[],int len){//insertion sort  algorithm
	
	int i;
	int j;
	int key;
	
	for(i=0;i<len;i++){
		
		j=i;
		key=data[i];
		
		
		while(j>0 && data[j-1]>key){
			
			data[j]=data[j-1];
			j--;
			
		}	
		data[j]=key;	
	}		
		
}		
		


int main(void ) {
	
	  
    double start,end;
    
    
    
    start = clock();  
      
  
	int len = sizeof(data) / sizeof(data[0]);
    
    insertionsort(data,len); 
    
    for(int i = 0; i < len; ++i) {
     
	 	
     printf("%d\n",data[i] )	;
    	
	}
	
   
  
    
     
    end = clock();  
  

    double diff = end - start; // ms 
    printf(" %f  ms" , diff);
    printf(" %f  sec", diff / CLOCKS_PER_SEC );
  



    
	
    return 0; 
    
}    
    
    
    
   
     
    
	
	
	
