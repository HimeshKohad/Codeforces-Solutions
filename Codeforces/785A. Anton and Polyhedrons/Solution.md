## Solution - [785A. Anton and Polyhedrons](https://github.com/HimeshKohad/Codeforces-Solutions/blob/main/Codeforces/785A.%20Anton%20and%20Polyhedrons/Problem.md)

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
typedef vector<char> vc;
typedef vector<vc> vvc;
typedef pair<int, int> pii;

void solve() {
    int n;
    cin >> n;
    
    int sides = 0;

    FOR(i, 0, n) {
        string s;
        cin >> s;

        if(s == "Tetrahedron") sides += 4;
        else if(s == "Cube") sides += 6;
        else if(s == "Octahedron") sides += 8;
        else if(s == "Dodecahedron") sides += 12;
        else sides += 20;
    }

    cout << sides << endl;
}

int32_t main() {
    ios::sync_with_stdio(0);
    cin.tie(0);
    cout.tie(0);

    solve();

    return 0;
}

```
