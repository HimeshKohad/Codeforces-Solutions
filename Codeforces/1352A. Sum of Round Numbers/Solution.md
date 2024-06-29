## Solution - [1352A. Sum of Round Numbers](https://github.com/HimeshKohad/Codeforces-Solutions/blob/main/Codeforces/1352A.%20Sum%20of%20Round%20Numbers/Problem.md)

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

    vector<int> roundNumbers;
    int place = 1;

    while(n > 0) {
        int digit = n % 10;
        n /= 10;

        if(digit != 0) {
            roundNumbers.pb(digit * place);
        }

        place *= 10;
    }

    cout << roundNumbers.size() << endl;
    for(int i = 0; i < roundNumbers.size(); i++) {
        cout << roundNumbers[i] << " ";
    }
    cout << endl;
}

int32_t main() {
    ios::sync_with_stdio(0);
    cin.tie(0);
    cout.tie(0);

    int t;
    cin >> t;
    while (t--) {
        solve();
    }

    return 0;
}


```
