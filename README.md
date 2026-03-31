# 洛谷B4262答案
## 洛谷B4262题目的答案
```c++
#include <iostream>
#include <string>
using namespace std;
int main() {
    int n;
    cin >> n;
    string x,a[105] = {};
    for (int i = 0;i<n;i++) {
        cin >> x;
        for (int j = 0;j < x.size();j++) {
            if(x[j] >= 'A' && x[j] <= 'Z') x[j]+=32;
        }
        a[i] = x;
    }
    int b[105] = {};
    for (int i = 0;i<n;i++) {
        bool c = 0;
        for (int j = 0;j<i;j++) {
            if (a[i] == a[j]) {
                b[j]++;
                c = 1;
            }
        }
        if (!(c)) {
            b[i]++;
        }
    }
    int maxx = 0;
    string ans;
    for (int i = 0;i<n;i++) {
        if (b[i] > maxx) {
            maxx = b[i];
            ans = a[i];
        }
    }
    cout << ans;
    return 0;
}
```

> [!NOTE]
>
> 以上为C++代码

