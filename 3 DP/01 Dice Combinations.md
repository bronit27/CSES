### [Dice Combinations](https://cses.fi/problemset/task/1633)

```cpp
#include<bits/stdc++.h>
#include<ext/pb_ds/assoc_container.hpp>
#include<ext/pb_ds/tree_policy.hpp>
 
using namespace std;
using namespace __gnu_pbds;
 
template<class T>
using oset = tree<T, null_type, less<T>, rb_tree_tag, tree_order_statistics_node_update>;
 
#define accelerate ios_base::sync_with_stdio(false);cin.tie(NULL);cout.tie(NULL)
#define int        long long
#define ld         long double
#define mod1       998244353
#define endl       "\n"
#define ff         first
#define ss         second
#define po         pop_back
#define pb         push_back
#define ub         upper_bound
#define lb         lower_bound
#define bs         binary_search
#define all(x)     (x).begin(),(x).end()
#define ra(arr,n)  vector<int> arr(n);for(int in=0;in<n;in++){cin>>arr[in];}
#define print(arr) for(auto index:arr)cout<<index<<" ";
 
const int mod = 1e9 + 7;
const int inf = 1e18;
 
int power(int a, int b) {
    int p = 1;
    while (b > 0) { if (b & 1) p = p * a; a = a * a; b >>= 1; }
    return p;
}
 
void lessgoo()
{
    int n;
    cin >> n;
    vector<int>dp(n + 1, 0);
    dp[0] = 1;
    dp[1] = 1;
    dp[2] = 2;
    for (int i = 3; i <= n; i++)
    {
        for (int j = i - 1; j >= i - 6 && j >= 0; j--)
        {
 
            dp[i] += (dp[j]) % mod;
 
        }
    }
    cout << dp[n] % mod << endl;
 
 
}
 
 
signed main()
{
    accelerate;
 
#ifndef ONLINE_JUDGE
    freopen("input.txt", "r", stdin);
    freopen("output.txt", "w", stdout);
#endif
 
    int test = 1;
    // cin >> test;
    while (test--)
    {
        lessgoo();
 
    }
 
 
 
    return 0;
}
