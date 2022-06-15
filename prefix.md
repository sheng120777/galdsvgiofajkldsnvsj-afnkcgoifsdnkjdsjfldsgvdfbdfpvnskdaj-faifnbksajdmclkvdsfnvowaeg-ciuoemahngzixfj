p1
```cpp
#include<bits/stdc++.h>
using namespace std;
#define int long long
#define endl '\n'
#define inf 2e18
#define maxn 100005
#define mod 1000000007


signed main(){

    ios::sync_with_stdio(0);
    cin.tie(0);

    int n;
    cin>>n;
    int cnt=0;
    while(n--){
        int k;
        cin>>k;
        cnt+=k;
        cout<<cnt<<" ";
    }
} 
//e339
```
p2
```cpp
#include<bits/stdc++.h>
using namespace std;
#define int long long
#define endl '\n'
#define inf 2e18
#define maxn 100005
#define mod 1000000007

signed main(){

    ios::sync_with_stdio(0);
    cin.tie(0);

    int n;
    cin>>n;
    int diff;
    cin>>diff;
    cout<<diff<<" ";
    n-=1;
    while(n--){
        int k;
        cin>>k;
        cout<<k-diff<<" ";
        diff=k;
    }
}
//e340

```
p3
```cpp
#include<bits/stdc++.h>
using namespace std;
#define int long long
#define endl '\n'
#define inf 2e18
#define maxn 200005
#define mod 1000000007

signed main(){

    ios::sync_with_stdio(0);
    cin.tie(0);

    int n;
    cin>>n;
    int arr[maxn];
    arr[0]=0;
    for(int i=1;i<=n;i++){
        cin>>arr[i];
        arr[i]+=arr[i-1];
    }
    int q;
    cin>>q;
    while(q--){
        int l,r;
        cin>>l>>r;
        cout<<arr[r]-arr[l-1]<<endl;
    }
}
//e346

```

p4
```cpp
#include<bits/stdc++.h>
using namespace std;
#define int long long
#define endl '\n'
#define inf 2e18
#define maxn 200005
#define mod 1000000007

signed main(){

    ios::sync_with_stdio(0);
    cin.tie(0);

    int n,k;
    cin>>n>>k;
    int arr[maxn];
    for(int i=0;i<n;i++){
        cin>>arr[i];
    }
    while(k--){
        int q;
        cin>>q;
        int l=0,r=n;
        while(l<r){
            int mid=(l+r)/2;
            if(arr[mid]>=q){
                r=mid;
            }
            else{
                l=mid+1;
            }
        }
        if(arr[r]==q){
            cout<<r+1<<endl;
        }
        else{
            cout<<0<<endl;
        }
    }
}
//d732
```

p5(不是很會這是抄的)
```cpp
#include<bits/stdc++.h>
using namespace std;
#define int long long
#define endl '\n'
#define inf 2e18
#define maxn 200005
#define mod 1000000007

signed main(){

    ios::sync_with_stdio(0);
    cin.tie(0);

    int n,m;
    int p[maxn];
    vector<int>pre;
    cin>>n>>m;
    for (int i=0,tot=0;i<n;i++){
        cin>>p[i];
        tot+=p[i];
        pre.push_back(tot);
    }
    int s=0;
    for (int i=0,q;i<m;i++){
        cin>>q;
        if(s!=0){
            q+=pre[s-1];
        }
        if(q>pre[n-1]){
            q-=pre[n-1];
        }
        s=(int)(lower_bound(pre.begin(),pre.end(),q)-pre.begin())+1;
        s%=n;
    }
    cout<<s;
}
```



p6
```cpp
#include<bits/stdc++.h>
using namespace std;
#define int long long
#define endl '\n'
#define inf 2e18
#define maxn 200005
#define mod 1000000007

signed main(){

    ios::sync_with_stdio(0);
    cin.tie(0);

    int n,m;
    cin>>n>>m;
    int a[maxn];
    int b[maxn];
    memset(a,0,sizeof(a));
    while(m--){
        int x,y,w;
        cin>>x>>y>>w;
        a[x]+=w;
        a[y+1]-=w;
    }
    for(int i=1;i<=n;i++){
        cin>>b[i];
    }
    for(int i=1;i<=n;i++){
        a[i]=a[i]+a[i-1];
    }
    sort(a+1,a+n+1);
    sort(b+1,b+n+1);
    int ans=0;
    for(int i=1;i<=n;i++){
        ans+=a[i]*b[n-i+1];
    }
    cout<<ans;
}
//g597
```


p7(我不會這是抄的)
```cpp
#include<bits/stdc++.h>
using namespace std;
#define int long long
#define endl '\n'
#define inf 2e18
#define maxn 400005
#define mod 1000000007

signed main(){

    ios::sync_with_stdio(0);
    cin.tie(0);

    int n;
    pair<int,int>p[maxn];
    priority_queue<int,vector<int>,greater<int>>pq;

	cin>>n;
	for(int i=0;i<n;i++)
		cin>>p[i].first>>p[i].second;
	int sum=0;
    int decrease=0;
	for(int i=0;i<n;i++) {
		decrease+=p[i].second;
		int temp=0;
		int sz=pq.size();
		while(!pq.empty() and pq.top()<decrease) {
			temp+=decrease-pq.top();
			pq.pop();
		}
		sum-=(p[i].second*sz)-temp-p[i].first;
		cout<<sum<<endl;
		pq.push(decrease+p[i].first);
	}
}
```
