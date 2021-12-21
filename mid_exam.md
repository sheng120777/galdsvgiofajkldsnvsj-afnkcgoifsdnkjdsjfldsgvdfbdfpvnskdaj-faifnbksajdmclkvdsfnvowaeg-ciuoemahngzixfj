```cpp
#pragma GCC optimize("Ofast")
#pragma GCC target("sse,sse2,sse3,ssse3,sse4,popcnt,abm,mmx,avx,avx2,fma")
#pragma GCC optimize("unroll-loops")
#include<bits/stdc++.h>
using namespace std;
#define int long long
#define endl '\n'
#define inf 2e18
#define maxn 10000005
#define mod 1000000007

signed main(){

    ios::sync_with_stdio(0);
    cin.tie(0);

    string s;
    getline(cin,s);
    cout<<s<<" "<<s;
}
```

```cpp
#pragma GCC optimize("Ofast")
#pragma GCC target("sse,sse2,sse3,ssse3,sse4,popcnt,abm,mmx,avx,avx2,fma")
#pragma GCC optimize("unroll-loops")
#include<bits/stdc++.h>
using namespace std;
#define int long long
#define endl '\n'
#define inf 2e18
#define maxn 10000005
#define mod 1000000007

signed main(){

    ios::sync_with_stdio(0);
    cin.tie(0);

    int n;
    while(cin>>n){
        if(n>=1){
            cout<<1911+n<<endl;
        }
        else{
            cout<<1912+n<<endl;
        }
    }
}
```

```cpp
#pragma GCC optimize("Ofast")
#pragma GCC target("sse,sse2,sse3,ssse3,sse4,popcnt,abm,mmx,avx,avx2,fma")
#pragma GCC optimize("unroll-loops")
#include<bits/stdc++.h>
using namespace std;
#define int long long
#define endl '\n'
#define inf 2e18
#define maxn 10000005
#define mod 1000000007

signed main(){

    ios::sync_with_stdio(0);
    cin.tie(0);

    int a,b,c;
    cin>>a>>b>>c;
    cout<<a+b+c;
}
```

```cpp
#pragma GCC optimize("Ofast")
#pragma GCC target("sse,sse2,sse3,ssse3,sse4,popcnt,abm,mmx,avx,avx2,fma")
#pragma GCC optimize("unroll-loops")
#include<bits/stdc++.h>
using namespace std;
#define int long long
#define endl '\n'
#define inf 2e18
#define maxn 10000005
#define mod 1000000007

signed main(){

    ios::sync_with_stdio(0);
    cin.tie(0);

    int n;
    cin>>n;
    if(n<=6){
        cout<<1;
    }
    else{
        n-=6;
        cout<<1+(n-1)/8+1;
    }
}   
```

```cpp
#pragma GCC optimize("Ofast")
#pragma GCC target("sse,sse2,sse3,ssse3,sse4,popcnt,abm,mmx,avx,avx2,fma")
#pragma GCC optimize("unroll-loops")
#include<bits/stdc++.h>
using namespace std;
#define int long long
#define endl '\n'
#define inf 2e18
#define maxn 10000005
#define mod 1000000007

signed main(){

    ios::sync_with_stdio(0);
    cin.tie(0);

    int n;
    cin>>n;
    while(n--){
        int a,b,c,d;
        cin>>a>>b>>c>>d;
        bool flag=false;
        if(c<=a and a<=d){
            flag=true;
        }
        if(c<=b and b<=d){
            flag=true;
        }
        if(a<=c and b>=c){
            flag=true;
        }
        if(a<=d and b>=d){
            flag=true;
        }
        if(flag){
            cout<<"Yes"<<endl;
        }
        else{
            cout<<"No"<<endl;
        }
    }
}
```


```cpp
#pragma GCC optimize("Ofast")
#pragma GCC target("sse,sse2,sse3,ssse3,sse4,popcnt,abm,mmx,avx,avx2,fma")
#pragma GCC optimize("unroll-loops")
#include<bits/stdc++.h>
using namespace std;
#define int long long
#define endl '\n'
#define inf 2e18
#define maxn 10000005
#define mod 1000000007

signed main(){

    ios::sync_with_stdio(0);
    cin.tie(0);

    string s;
    getline(cin,s);
    for(int i=0;i<s.length();i++){
        if(isalpha(s[i])){
            cout<<s[i];
        }
    }
}
```


```cpp
#pragma GCC optimize("Ofast")
#pragma GCC target("sse,sse2,sse3,ssse3,sse4,popcnt,abm,mmx,avx,avx2,fma")
#pragma GCC optimize("unroll-loops")
#include<bits/stdc++.h>
using namespace std;
#define int long long
#define endl '\n'
#define inf 2e18
#define maxn 10000005
#define mod 1000000007

signed main(){

    ios::sync_with_stdio(0);
    cin.tie(0);

    int n;
    cin>>n;
    while(n--){
        int arr[50];
        for(int i=0;i<50;i++){
            arr[i]=true;
        }
        int a,b,c;
        cin>>a>>b>>c;
        vector<int>vec;
        for(int i=a;i<=b;i++){
            if((i+7)%c==0){
                arr[i]=false;
            }
        }
        for(int i=1;i<=43;i++){
            if(arr[i]==true){
                vec.push_back(i);
            }
        }
        if(vec.size()==0){
            cout<<0;
        }
        else{
            for(int i=0;i<vec.size();i++){
                cout<<vec[i]<<" ";
            }
        }
        cout<<endl;
    }
}
```
