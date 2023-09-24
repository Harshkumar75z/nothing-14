// Q1: Write a program to store 10 at every index of a 2D matrix with 5 rows and 5 columns.
#include<iostream>
using namespace std;
int main(){
    int arr[5][5];
    for(int i=0;i<5;i++){
        for(int j=0;j<5;j++){
            arr[i][j]=10;
        }
    }
    for(int i=0;i<5;i++){
        for(int j=0;j<5;j++){
            cout<<arr[i][j]<<" ";
        }cout<<endl;
    }
}

// Q2: Write a program to add two matrices and save the result in one of the given matrices.
#include<iostream>
using namespace std;
int main(){
    int arr[3][3]={1,2,3,4,5,6,7,8,9};
    int brr[3][3]={4,5,8,0,0,8,1,2,0};  
    for(int i=0;i<3;i++){
        for(int j=0;j<3;j++){
            brr[i][j] += arr[i][j];
            cout<<brr[i][j]<<" ";
        }cout<<endl;
    }
    
}


// Q3: Given a matrix ‘A’ of dimension n x m and 2 coordinates (l1, r1) and (l2, r2). Return the sum of the
// rectangle from (l1,r1) to (l2, r2).
#include<iostream>
using namespace std;
int main(){
    int m;
    cout<<"Enter Number of Rows : ";
    cin>>m;
    int n;
    cout<<"Enter Number of Columns : ";
    cin>>n;
    int arr[m][n];
        // Taking Input
    for(int i=0;i<m;i++){
        for(int j=0;j<n;j++){
            cin>>arr[i][j];
        }
    }
    // Taking Dimnesions
    int x1,x2,y1,y2;
    cout<<"Enter 1st Dimension : ";
    cin>>x1>>y1;
    cout<<"Enter 2nd Dimension : ";
    cin>>x2>>y2;
    // Output
    int sum=0;
    for(int i=x1;i<=x2;i++){
        for(int j=y1;j<=y2;j++){
            sum=sum+arr[i][j];
        }
    }cout<<sum;
}


// Q4: Write a C++ program to find the largest element of a given 2D array of integers.
#include<iostream>
#include<climits>
using namespace std;
int main(){
    int m;
    cout<<"Enter Number of Rows : ";
    cin>>m;
    int n;
    cout<<"Enter Number of Columns : ";
    cin>>n;
    int arr[m][n];
    // Taking Input
    for(int i=0;i<m;i++){
        for(int j=0;j<n;j++){
            cin>>arr[i][j];
        }
    }
        // Find Largest 
    int max=INT_MIN;
    for(int i=0;i<m;i++){
        for(int j=0;j<n;j++){
                if(max<arr[i][j]){
                    max = arr[i][j];
            }
        }
    }cout<<max<<" ";
}


// Q5: Write a program to print the row number having the maximum sum in a given matrix.
#include<iostream>
#include<climits>
using namespace std;
int main(){
    int m;
    cout<<"Enter the Value of Rows : ";
    cin>>m;
    int n;
    cout<<"Enter the Value of Columns : ";
    cin>>n;
    int arr[m][n];
    // Input
    for(int i=0;i<m;i++){
        for(int j=0;j<n;j++){
            cout<<"Enter Elements : ";
           cin>>arr[i][j]; 
        }
    }
    // Sum of Rows
    int MaxSum=INT_MIN;
    int MaxRow=-1;
    int sum=0;
    for(int i=0;i<m;i++){
        int sum=0;
        for(int j=0;j<n;j++){
            sum=sum+arr[i][j];           
            if(sum>MaxSum){
                MaxSum = sum;
                MaxRow = i;
            }
        }
    }cout<<"Maximum Sum is "<<MaxSum<<endl;
    cout<<"Row Number : "<<MaxRow;
}


// Q6: Write a function which accepts a 2D array of integers and its size as arguments and displays the
// elements of middle row and the elements of middle column.
#include<iostream>
using namespace std;
int main(){
    int m;
    cout<<"Enter the Value of Rows : ";
    cin>>m;
    int arr[m][m];
    // Input
    for(int i=0;i<m;i++){
        for(int j=0;j<m;j++){
            cout<<"Enter Elements : ";
           cin>>arr[i][j]; 
        }
    }
    for(int i=0;i<m;i++){
        for(int j=0;j<m;j++){
            if(i==m/2 || j==m/2){
                cout<<arr[i][j]<<" ";
            }
            else
            cout<<" "<<" ";
        }cout<<endl;
    }
}
