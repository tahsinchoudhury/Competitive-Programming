#include<bits/stdc++.h>
using namespace std;

#define endl '\n'
#define pb push_back
#define ll long long
#define all(v) v.begin(), v.end()
#define pii pair<int, int>

#ifdef LOCAL
#define dbg(x) cerr << #x << " is " << x << endl
#else
#define dbg(x)
#endif

const int N = 1e6 + 5;

int main()
{
	ios_base::sync_with_stdio(false);
	cin.tie(NULL);

	int n;
	cin >> n;
	vector <ll> v(n + 1, 0);
	for(int i = 1; i <= n; i++) cin >> v[i];

	vector <ll> prefix_sum(n + 1, 0), m(n + 1, 0);
	for(int i = 1; i <= n; i++) 
		prefix_sum[i] = prefix_sum[i - 1] + v[i],
		m[i] = v[i] * prefix_sum[i];
	for(int i = 1; i <= n; i++) m[i] += m[i - 1];

	int q;
	cin >> q;

	while(q--){
		int u, v;
		cin >> u >> v;
		u++, v++;

		cout << m[v] - m[u - 1] - prefix_sum[u - 1] * (prefix_sum[v] - prefix_sum[u - 1]) << "\n";
	}

	return 0;
} 
