### [Sum of Two Values](https://cses.fi/problemset/task/1640/)

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
  int arr[n],sr[n];
  for(int i=0;i<n;i++)
  {
     cin>>arr[i];
     sr[i]=arr[i];
  }
  int s=0;
  int e=n-1;
  bool ans=false;
  sort(arr,arr+n);
  while(s<e)
  {
     if(arr[s]+arr[e]==k)
     {
          ans=true;
          // cout<<s+1<<" "<<e+1<<endl;
          break;
     }else if(arr[s]+arr[e]<k)
     {
          s++;
     }else
     {
          e--;
     }
  }if(!ans){
     cout<<"IMPOSSIBLE"<<endl;
  }else
  {   
     // cout<<arr[s]<<arr[s]<<endl;
     // int a=-1,b=-1;
     for(int i=0;i<n;i++)
     {
          if(sr[i]==arr[s])
          {
               
               cout<<i+1<<" ";
               sr[i]=-1;
               break;
               
          }
          
     }for(int i=0;i<n;i++)
     {
          if(sr[i]==arr[e])
          {
           cout<<i+1<<endl;
           break;
          }
     }
  }
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
