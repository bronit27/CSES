### [Removing Digits](https://cses.fi/problemset/task/1637)

```cpp
#include<bits/stdc++.h>
#include<ext/pb_ds/assoc_container.hpp>
#include<ext/pb_ds/tree_policy.hpp>
 
using namespace std;
using namespace __gnu_pbds;
 
template<class T>
using oset = tree<T, null_type, less<T>, rb_tree_tag, tree_order_statistics_node_update>;//order_of_key find_by_order
#define accelerate ios_base::sync_with_stdio(false);cin.tie(NULL);cout.tie(NULL)
#define int        long long int
#define ld         long double
#define mod1       998244353
#define endl       "\n"
#define ff         first
#define ss         second
#define all(x)     (x).begin(),(x).end()
#define ra(arr,n)  vector<int> arr(n);for(int in = 0; in < n; in++) {cin >> arr[in];}
 
const int mod = 1e9 + 7;
const int inf = 1e18;
int MOD(int x) {int a1 = (x % mod); if (a1 < 0) {a1 += mod;} return a1;}
int power( int a,  int b) {
    int p = 1; while (b > 0) { if (b & 1) p = (p * a); a = (a * a) ; b >>= 1;}
    return p;
}
int fact(int x) {
    int ans = 1;
    for (int i = 2; i <= x; i++)ans = (ans * i) % mod;
    return ans % mod;
}
 
void lessgoo()
{
    int n;
    cin >> n;
    vector<int>dp(n + 1);
    dp[0] = 0;
    for (int i = 1; i <= n; i++)
    {
        if (i <= 9)
        {
            dp[i] = 1;
        } else
        {
            int ans = INT_MAX;
            int num = i;
            while (num > 0)
            {
                int l = num % 10;
                if (l != 0) {
                    int x = i - l;
                    ans = min(ans, dp[x]);
                }
                num = num / 10;
            }
            dp[i] = ans + 1;
        }
    }
    cout << dp[n] << endl;
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
    for (int tcase = 1; tcase <= test; tcase++)
    {
        lessgoo();
 
    }
    return 0;
}
