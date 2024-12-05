# cp-snippet-cpp

Competitive programming code snippet for c++ users. Feel free to clone/fork/copy.  
Hit the star⭐️ button in case you like it.

## Getting Started

1. Install [Visual Studio Code](https://code.visualstudio.com/).

2. Go to `Settings` > `Snippets` and select `cpp.json`

3. Paste below key-value's into `cpp.json`

```json
    "Codeforces cp template": {
        "prefix": "cft",
        "body": [
            "#include <bits/stdc++.h>",
            "using namespace std;",
            "",
            "#define FAST_IO ios_base::sync_with_stdio(0), cin.tie(0);",
            "typedef long long ll;",
            "typedef pair<int,int> ii;",
            "typedef deque<int> di;",
            "typedef deque<ii> dii;",
            "typedef vector<int> vi;",
            "typedef vector<ll> vl;",
            "typedef vector<ii> vii;",
            "typedef priority_queue<int, vi, less<int>> maxHeap;",
            "typedef priority_queue<int, vi, greater<int>> minHeap;",
            "",
            "$0",
            "",
            "void solve() {",
            "    ",
            "}",
            "",
            "int main() {",
            "    FAST_IO;",
            "    int t; cin >> t;",
            "    while (t--) solve();",
            "}"
        ],
        "description": "CP template for codeforces ace."
    },
    "Modular operation utility functions": {
        "prefix": "modops",
        "body": [
            "const int MOD = 1e9 + 7;",
            "",
            "inline int _mul(int a, int b) {",
            "    ll ret = a * 1ll * b;",
            "    ret %= MOD;",
            "    return int(ret);",
            "}",
            "",
            "inline int _add(int a, int b) {",
            "    ll ret = a + b;",
            "    while (ret >= MOD) ret -= MOD;",
            "    while (ret < 0) ret += MOD;",
            "    return int(ret);",
            "}",
            "",
            "inline int _binPow(int x, int n) {",
            "    int ret = 1;",
            "    int d = x;",
            "    while (n) {",
            "        if (n & 1) {",
            "            ret = _mul(ret, d);",
            "        }",
            "        d = _mul(d, d);",
            "        n >>= 1;",
            "    }",
            "    return ret;",
            "}",
            "",
            "inline int _inv(int a) {",
            "    return _binPow(a, MOD - 2);",
            "}",
            "",
            "inline int _div(int a, int b) {",
            "    return _mul(a, _inv(b));",
            "}"
        ],
        "description": "Modular operation utility functions."
    }
```

4. Try to use snippet inside the editor, typing `cft`.

## Template Preview

### Codeforces

> prefix: "cft"

```cpp
#include <bits/stdc++.h>
using namespace std;

#define FAST_IO ios_base::sync_with_stdio(0), cin.tie(0);
typedef long long ll;
typedef pair<int,int> ii;
typedef deque<int> di;
typedef deque<ii> dii;
typedef vector<int> vi;
typedef vector<ll> vl;
typedef vector<ii> vii;
typedef priority_queue<int, vi, less<int>> maxHeap;
typedef priority_queue<int, vi, greater<int>> minHeap;

const int MOD = 1e9 + 7;

inline int _mul(int a, int b) {
    ll ret = a * 1ll * b;
    ret %= MOD;
    return int(ret);
}

inline int _add(int a, int b) {
    ll ret = a + b;
    while (ret >= MOD) ret -= MOD;
    while (ret < 0) ret += MOD;
    return int(ret);
}

inline int _binPow(int x, int n) {
    int ret = 1;
    int d = x;
    while (n) {
        if (n & 1) {
            ret = _mul(ret, d);
        }
        d = _mul(d, d);
        n >>= 1;
    }
    return ret;
}

inline int _inv(int a) {
    return _binPow(a, MOD - 2);
}

inline int _div(int a, int b) {
    return _mul(a, _inv(b));
}

void solve() {
    
}

int main() {
    FAST_IO;
    int t; cin >> t;
    while (t--) solve();
}
```