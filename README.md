## [Equal Elements](https://www.codechef.com/problems/EQUALELE)
> Submission code: [Check here](https://www.codechef.com/viewsolution/91739320)
<details><summary>Code</summary>
<p>
```C++
#include <bits/stdc++.h>
using namespace std;

void solve() {
    int n; cin>>n;
    map<int, int> occurence;
    for(int i=0; i<n; i++) {
        int num; cin>>num;
        occurence[num]++;
    }
    int maximum = INT_MIN;
    for(auto occur: occurence) {
        if(occur.second > maximum) {
            maximum= occur.second;
        }
    }
    cout<<n-maximum<<endl;
}

int main() {
	int test_case; cin>>test_case;
	while(test_case--) {
	    solve();
	}
	return 0;
}
</p>
</details>
```
###### Take Away
>```Ruby
> Let a number x occurs freq[x] times then we need N - freq[x] operations. To minimize (N - freq[x]) we have to maximize freq[x].
>```
