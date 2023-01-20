###[Distict Numbers](https://cses.fi/problemset/task/1621)

```cpp
#include<bits/stdc++.h>
using namespace std;
#define endl "\n"
#define int long long int
#define fastio() ios_base::sync_with_stdio(false);cin.tie(NULL);cout.tie(NULL)
#define tc int t;cin>>t;while(t--)
 
 
void solve()
{ 
 int n;
 cin>>n;
 int arr[n];
 int a=0;
 for(int i=0;i<n;i++)
 {
  cin>>arr[i];
 }sort(arr,arr+n);
 for(int i=0;i<n-1;i++)
 {
  if(arr[i]!=arr[i+1])
  {
    a++;
  }
 }cout<<a+1<<endl;
}
signed main()
  {  
     fastio();
#ifndef ONLINE_JUDGE
    freopen("input.txt","r",stdin);
    freopen("output.txt","w",stdout);
    freopen("Error.txt","w",stderr);
#endif
      solve();
      
#ifndef ONLINE_JUDGE
     cerr << "Time : " << (float)clock() / CLOCKS_PER_SEC << " Secs" << endl;
#endif
 
 
return 0;
}
```
