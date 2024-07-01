## Solution - [510A. Fox And Snake](https://github.com/HimeshKohad/Codeforces-Solutions/blob/main/Codeforces/510A.%20Fox%20And%20Snake/Problem.md)

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
    int n, m;
    cin >> n >> m;

    // predefining matrix with all '.'
    vvc mat(n, vc(m, '.'));
    

    for (int i = 0; i < n; ++i) {
        if (i % 2 == 0) {
            // Fill the entire row with '#'
            for (int j = 0; j < m; ++j) {
                mat[i][j] = '#';
            }
        } 
        
        else {
            if ((i / 2) % 2 == 0) {
                // Place '#' at the end for rows where (i / 2) is even
                mat[i][m - 1] = '#';
            } 
            
            else {
                // Place '#' at the beginning for rows where (i / 2) is odd
                mat[i][0] = '#';
            }
        }
    }

    // Print the matrix
    for(int i = 0; i < n; i++) {
        for(int j = 0; j < m; j++) {
            cout << mat[i][j];
        }
        cout << endl;
    }
    
}

int32_t main() {
    ios::sync_with_stdio(0);
    cin.tie(0);
    cout.tie(0);

    solve();

    return 0;
}

```
