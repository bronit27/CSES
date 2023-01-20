### [Ferris Wheel](https://cses.fi/problemset/task/1090/)

```cpp
 #include<bits/stdc++.h>
using namespace std;
#define int        long long 
#define ld         long double
#define mod        1000000007
#define mod1       998244353
#define endl       "\n"
#define accelerate ios_base::sync_with_stdio(false);cin.tie(NULL);cout.tie(NULL)
#define pb         push_back
#define po         pop_back
#define bs         binary_search
#define all(x)     (x).begin(),(x).end()  
#define tc         int test;cin>>test; while(test--)
#define ra(arr,n)  vector<int> arr(n);for(int in=0;in<n;in++){cin>>arr[in];}
 
void solve()
{ 
  int n,k;
  cin>>n>>k;
  ra(arr,n);
  sort(all(arr));
  int cnt=0;
  int ans=0;
  for(int i=n-1;i>=cnt;i--)
  {
    if(arr[i]+arr[cnt]<=k)
    {
     ans++;
     cnt++;
    }else
    {
       ans++;
    }
  }cout<<ans<<endl;
}
 
signed main()
{  
     accelerate;
 
#ifndef ONLINE_JUDGE
     freopen("input.txt","r",stdin);
     freopen("output.txt","w",stdout);
#endif
     
     
     solve();
     
     return 0;
}
```
