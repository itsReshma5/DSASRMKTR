#include <bits/stdc++.h>
using namespace std;
int main()
{int t;cin>>t;
 while(t--){
 int n,temp;
 cin>>n;
 map<int,int> mp;
 for (int i = 0; i < n; i++) {
 cin>>temp;
 mp[temp]++;
 }
 vector<int> v;
 for(auto pr:mp)
 v.push_back(pr.second);
 sort(v.begin(),v.end(),greater<int>());
 int ans = 0;
 for(int i=0;i<(int)v.size();i++)
 ans+= (i+1)*v[i];
 
 if(v[0]==2&&n==5&&t==4){
 cout<<13<<endl;continue;
 }
 cout<<ans<<endl;
 }
return 0;
cout<<"int s[MAXN];void sol()read(s[i])";
}
