### [Edit distance](https://cses.fi/problemset/task/1639)

```cpp
#include<bits/stdc++.h>
#include<ext/pb_ds/assoc_container.hpp>
#include<ext/pb_ds/tree_policy.hpp>
 
using namespace std;
using namespace __gnu_pbds;
 
template<class T>
using oset = tree<T, null_type, less<T>, rb_tree_tag, tree_order_statistics_node_update>;
// order_of_key(a)  -> gives index of the element(number of elements smaller than a)
// find_by_order(a) -> gives the element at index a
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
 
 
void lessgoo()
{
    string a, b;
    cin >> a >> b;
    int n = a.size();
    int m = b.size();
    n++;
    m++;
    vector<vector<int>>dp(n, vector<int>(m, 0));
    for (int i = 1; i < n; i++)dp[i][0] = i;
    for (int i = 1; i < m; i++)dp[0][i] = i;
    for (int i = 1; i < n; i++) {
        for (int j = 1; j < m; j++)
        {
            int ax = 0;
            if (a[i - 1] != b[j - 1])ax++;
            dp[i][j] = min({dp[i - 1][j - 1] + ax, dp[i - 1][j] + 1, dp[i][j - 1] + 1});
        }
    }
    cout << dp[n - 1][m - 1];
 
 
 
 
 
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
        // cout << "Case #" << tcase << ": ";
        lessgoo();
 
    }
    return 0;
}
