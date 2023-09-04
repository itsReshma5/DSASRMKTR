#include <bits/stdc++.h>
using namespace std;
int main()
{
 int r,c;
 cin>>r>>c;
 int arr[r][c];
 int arrTemp[r][c];
 for (int i = 0; i < r; i++) {
 for (int j = 0; j < c; j++) {
 cin>>arr[i][j];
 arrTemp[i][j] = 0;
 }
 }
 
 for (int i = 0; i < r; i++) {
 for (int j = 0; j < c; j++) {
 if(arr[i][j]==1){
 for(int i1 = 0;i1<r;i1++){
 arrTemp[i1][j] =1;
 }
 for(int i1 = 0;i1<c;i1++){
 arrTemp[i][i1] =1;
 }
 }
 }
 }
 for (int i = 0; i < r; i++) {
 for (int j = 0; j < c; j++) {
 cout<<arrTemp[i][j];
 if(j!=c-1)cout<<' '; 
 }
 cout<<endl;
 }
 
return 0;
printf("for(m=0;m<r;m++)");
}
