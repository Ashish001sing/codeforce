# codeforce
codeforce problem 800 rating 
      problem linl "https://codeforces.com/contest/2019/problem/A" type in browser and get q.
      # code  
      # include <iostream>
#include <cmath>
using namespace std;
int fun(int arr[], int n) {
   int sum=arr[0];
   int cure=arr[1];
   int val=1;
   int cal=1;
   for (int i=3;i<n;i+=2){
      if (arr[(i)%n]>=cure){
    cure=arr[i];
    cal++;
  }
  cure =cal+cure;
   }
   
   for (int i=2;i<n;i+=2){
  if (arr[(i)%n]>=sum){
    sum=arr[i];
    val++;
  }
  
   }
sum =val+sum;

sum=max(sum,cure);
return sum;
}
int main()
{
    int t;
    cin>>t;
    while (t>0){
        int n;
        cin>>n;
        int arr[n];
        for (int i=0;i<n;i++){
            cin>>arr[i];
        }
       int rer = fun(arr,n);
       cout <<rer<<endl;
      t--;
    }
    return 0;

}
