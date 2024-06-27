## Solution - [282A. Bit++](https://github.com/HimeshKohad/Codeforces-Solutions/blob/main/Codeforces/282A.%20Bit%2B%2B/Problem.md)

```cpp

#include <iostream>
#include <vector>
#include <string>
#include <algorithm>
#include <cmath>
#include <limits>
#include <set>
#include <map>
#include <queue>
#include <stack>
#include <bitset>
#include <numeric>
#include <fstream>
#include <iomanip>
#include <sstream>
#include <functional>
using namespace std;

#define int long long
#define MOD 1000000007
#define INF LLONG_MAX
#define PI 3.14159265358979323846

#define pb push_back
#define pop pop_back
#define mp make_pair
#define ff first
#define ss second
#define all(x) (x).begin(), (x).end()
#define sz(x) ((int)(x).size())
#define FOR(i, a, b) for (int i = (a); i < (b); ++i)
#define FORR(i, a, b) for (int i = (a); i > (b); --i)

typedef vector<int> vi;
typedef vector<vi> vvi;
typedef pair<int, int> pii;

void solve() {
    int n;
    cin >> n;

    int sum = 0;

    while(n--) {
        string s;
        cin >> s;

        for(int i = 0; i < s.length(); i++) {
            if(s[i] == '+' && s[i + 1] == '+') {
                sum++;
            }

            if(s[i] == '-' && s[i + 1] == '-') {
                sum--;
            }
        }
    }

    cout << sum << endl;
    
}

int32_t main() {
    ios::sync_with_stdio(0);
    cin.tie(0);
    cout.tie(0);

    solve();

    return 0;
}

```
