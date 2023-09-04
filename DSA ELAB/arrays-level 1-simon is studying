#include<bits/stdc++.h>
using namespace std;
int MaxOcurrence(int arr[],int n){
    sort(arr,arr+n);
    int max_count=1,crnt_count=1,res,i;
    for(i=1;i<n;i++){
        if(arr[i]==arr[i-1])
            crnt_count++;
        else{
            if(crnt_count > max_count){
                max_count = crnt_count;
                res = arr[i-1];
            }
            crnt_count = 1;
        }
    }
    if(crnt_count > max_count){
        max_count = crnt_count;
        res = arr[n-1];
    }
    return res;
}
int main(){
    int n,i;
    cin >> n;
    int arr[n];
    for(i= 0;i< n;i++)
        cin >> arr[i];
    cout << MaxOcurrence(arr,n);
    return 0;
}
