### [Weird Algorithm](https://cses.fi/problemset/task/1068)

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
 cout<<n<<" ";
 while(n>1)
 {
   if(n%2==0)
   {
    n=n/2;
   }else
   {
    n=n*3+1;
   }cout<<n<<" ";
 } 
  cout<<endl;
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
