// Insertion_sort
// sorting of array using insertion sort with early termination if array in between is found sorted
//---------------------------------------------------------------------------------------

#include<iostream>

using namespace std;

void sort(int arr[],int len){
	
	int i,j,temp;
	int flag=0;

	for(i = 0; i < len; i++) {
		j = i;
		while(j > 0 && arr[j]<arr[j-1]){
			temp = arr[j];
			arr[j] = arr[j-1];
			arr[j-1] = temp;
			j--;
			flag=1;
		}
		if(flag==0 && i!=len-1){
			cout<<"early termination ... ";
			break;
		}
	}
	
	cout<<"\nArray successfully sorted........";	
	cout<<"\nThe new Sorted array is :";
		for(int i=0;i<len;i++) {
		
		cout<<arr[i]<<" ";
		
	}
	
}


int main() {
	
	cout<<"Assignment 2 -> Question 2 -> INSERTION SORT\n";
	int len;
	
	cout<<"Enter the length of array:";
	cin>>len;
	
	int *arr = NULL;
	arr = new int[len];
	
	cout<<"\nEnter the Array:";
	for(int i=0;i<len;i++) {
		
		cin>>arr[i];
		
	}
	
	cout<<"\nYour Inserted array is:";
	for(int i=0;i<len;i++) {
		
		cout<<arr[i]<<" ";
		
	}
	
	cout<<"\n**** INSERTION SORT ****\n";
	sort(arr,len);

	
	return 0;
}
