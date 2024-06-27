## Solution - [514A. Chewbaсca and Number](https://github.com/HimeshKohad/Codeforces-Solutions/blob/main/Codeforces/514A.%20Chewba%D1%81ca%20and%20Number/Problem.md)

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
    string s;
    cin >> s;

    int n = s.length();

    for(int i = 0; i < n; i++) {
        int digit = s[i] - '0';

        if(digit >= 5) {
            int inverted = 9 - digit;

            if(i == 0 && inverted == 0) {
                continue;
            }

            s[i] = inverted + '0';
        }
    }

    cout << s << endl;
}

int32_t main() {
    ios::sync_with_stdio(0);
    cin.tie(0);
    cout.tie(0);

    solve();

    return 0;
}

```
