1-py
```py
def main():
  data=input().split()
  for i in range(3):
    data[i]=int(data[i])
    data[i]=bool(data[i])
  flag=False
  if (data[0] and data[1])==data[2]:
    print('AND')
    flag=True  
  if (data[0] or data[1])==data[2]:
    print('OR')
    flag=True  
  if (data[0]^data[1])==data[2]:
    print('XOR')
    flag=True
  if not flag:
    print('IMPOSSIBLE')  
main()
```

2-py
```py
lst=[]
a=[]
b=[]
data=str(input())
for i in data:
    lst.append(i)
if len(lst)%2==1:
    for j in range(1,len(lst)-1,2):
        a.append(int(lst[j-1]))
        b.append(int(lst[j]))
    a.append(int(lst[(len(lst))-1]))
    A=sum(a)
    B=sum(b)
    ans=abs(A-B)
else:
    for j in range(1,len(lst),2):
        a.append(int(lst[j-1]))
        b.append(int(lst[j]))
    A=sum(a)
    B=sum(b)
    ans=abs(A-B)
print(ans)
```


3-py
```py
data=input().split()

def select (data):
  for i in range(2):
    for j in range(i+1,3):
      if int(data[i])>int(data[j]):
        data[i],data[j]=data[j],data[i]

select(data)
for i in range(3):
  print(data[i],end=" ")


if int(data[0])+int(data[1])<int(data[2]):
  print("\nNo")
elif int(data[0])*int(data[0])+int(data[1])*int(data[1])<int(data[2])*int(data[2]): 
  print("\nObtuse")
elif int(data[0])*int(data[0])+int(data[1])*int(data[1])>int(data[2])*int(data[2]):
  print("\nAcute")
else:
  print("\nRight")
```

4-py
```py
def main():
  n=int(input())
  new=input().split()
  for i in range(n-1,-1,-1):
    for j in range(i):
      if int(new[j])>int(new[j+1]):
        new[j],new[j+1]=new[j+1],new[j]
  for i in range(n):
    print('%d' %(int(new[i])),end=' ')

  newdata=list(map(int,new))

  target=0

  if min(newdata)>60:
    print('\nbest case')
  else:
    for i in range(n):
      if (abs(60-newdata[i]))<(abs(60-target)) and newdata[i]<60:
        target=newdata[i]
    print('\n''%d'%(target))

  
 
  max=0
  for i in newdata:
    if (abs(max is None or i>max)):
      max=i

  target=min(newdata)
  if max<60:
    print('worst case')
  else:
    for i in range(n):
      if abs((60-newdata[i]))<(60-target) and newdata[i]>60:
        target=newdata[i]
      if newdata[i]==60:
        target=60
    print('%d'%(target))
      
main()
```


5-cpp
```cpp
#include<bits/stdc++.h>
using namespace std;
#define int long long
#define endl '\n'

signed main(){

    ios::sync_with_stdio(0);
    cin.tie(0);

    int a,b,c;
    cin>>a>>b>>c;
    int d,e,f;
    cin>>d>>e>>f;
    int n;
    cin>>n;
    int ans=-10000000;
    for(int i=0;i<=n;i++){
        int tmp=(a*i*i + b*i + c)+(d*(n-i)*(n-i) + e*(n-i) +f);
        ans=max(ans,tmp);
    }
    cout<<ans;
}
```

6-cpp
```cpp
#include<bits/stdc++.h>
using namespace std;
#define int long long
#define endl '\n'

signed main(){

    ios::sync_with_stdio(0);
    cin.tie(0);

    int a,b;
    cin>>a>>b;
    int n;
    cin>>n;
    int ans=0;
    for(int i=0;i<n;i++){
        int tag;
        int num_a=0;
        int num_b=0;  //initialize
        while(cin>>tag and tag!=0){
            if(tag==a){
                num_a++;
            }
            if(tag==-a){
                num_a--;
            }
            if(tag==b){
                num_b++;
            }
            if(tag==-b){
                num_b--;
            }
        }
        if(num_a>=1 and num_b>=1){
            ans++;
        }
    }
    cout<<ans;
}
```

7-cpp
```cpp
#include<bits/stdc++.h>
using namespace std;
#define int long long
#define endl '\n'

signed main(){

    ios::sync_with_stdio(0);
    cin.tie(0);

    int n,d;
    cin>>n>>d;
    int num=0;//買的數量
    int total=0;//花的總價
    for(int i=1;i<=n;i++){
        int price[3];
        cin>>price[0]>>price[1]>>price[2];
        sort(price,price+3);
        int gap=price[2]-price[0];// high-low
        if(gap>=d){
            int average=(price[0]+price[1]+price[2])/3;
            num++;  //num=num+1  or  num+=1
            total+=average;
        }
    }
    cout<<num<<" "<<total;
}
```

8-cpp
```cpp
#include<bits/stdc++.h>
using namespace std;
#define int long long
#define endl '\n'

signed main(){

    ios::sync_with_stdio(0);
    cin.tie(0);

    int n;
    cin>>n;
    for(int i=1;i<=n;i++){
        int up[50];
        int down[50];
        vector<string>rule;  //vector<資料型態>名稱;
        for(int i=1;i<=7;i++){
            cin>>up[i];
        }
        for(int i=1;i<=7;i++){
            cin>>down[i];
        }
        if(up[2]==up[4] or up[2]!=up[6] or down[2]==down[4] or down[2]!=down[6]){
            rule.push_back("A");
        }
        if(up[7]==0 or down[7]==1){
            rule.push_back("B");
        }
        if(up[2]==down[2] or up[4]==down[4] or up[6]==down[6]){
            rule.push_back("C");
        }

        if(rule.size()>0){
            for(int i=0;i<rule.size();i++){
                cout<<rule[i];  
            }
        }
        else{
            cout<<"None";
        }
        cout<<endl;
    }
}
```

9-cpp
```cpp
#include<bits/stdc++.h>
using namespace std;
#define int long long
#define endl '\n'

signed main(){

    ios::sync_with_stdio(0);
    cin.tie(0);

    int arr[100005];
    int n;
    cin>>n;
    for(int i=1;i<=n;i++){
        cin>>arr[i];
    }
    int ans=0;
    for(int i=1;i<=n;i++){
        if(arr[i]==0){
            if(i==1){
                ans=ans+arr[2];
            }
            else if(i==n){
                ans=ans+arr[n-1];  //n的前一隻就是第n-1隻
            }
            else{
                ans=ans+min(arr[i-1],arr[i+1]);
            }
        }
    }
    cout<<ans;
}
``` 

10-cpp
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


    int f;
    int n;
    cin>>f;
    cin>>n;
    
    int arr[1005];
    for(int i=0;i<n;i++){
        cin>>arr[i];
    }
    int i;
    for(i=0;i<n;i++){
        if(i>0){
            if(i>=2 and (arr[i-1]==arr[i-2])){
                if(arr[i-1]==0){
                    f=5;
                }
                else if(arr[i-1]==2){
                    f=0;
                }
                else if(arr[i-1]==5){
                    f=2;
                }
            }
            else{
                f=arr[i-1];
            }
        }
        
        cout<<f<<" ";
        if(f==arr[i]){
            continue;
        }
        else{
            if(f==0){
                if(arr[i]==2){
                    cout<<": Won at round ";
                }
                if(arr[i]==5){
                    cout<<": Lost at round ";
                }
            }
            if(f==2){
                if(arr[i]==5){
                    cout<<": Won at round ";
                }
                if(arr[i]==0){
                    cout<<": Lost at round ";
                }
            }
            if(f==5){
                if(arr[i]==0){
                    cout<<": Won at round ";
                }
                if(arr[i]==2){
                    cout<<": Lost at round ";
                }
            }
            
            cout<<i+1;
            break;
        } 
    }
    if(i==n){
        cout<<": Drew at round "<<n;
    }
    
    return 0; 
}
```

11-cpp
```cpp
#include<bits/stdc++.h>
using namespace std;
#define int long long
#define endl '\n'

signed main(){

    ios::sync_with_stdio(0);
    cin.tie(0);

    int n,d;
    cin>>n>>d;
    int stock[100005];   //第i天的股價
    for(int i=1;i<=n;i++){
        cin>>stock[i];
    }
    bool position=true;  //持倉狀況
    int entry=stock[1];    //第一天的股價
    int exit=0;
    int profit=0;
    for(int i=2;i<=n;i++){
        if(stock[i]-entry>=d and position==true){
            exit=stock[i];
            profit=profit+(exit-entry);
            position=false;
        }
        if(position==false and exit-stock[i]>=d){
            entry=stock[i];
            position=true;
        }
    }
    cout<<profit<<endl;
}
```
