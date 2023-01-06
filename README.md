# LeetCode

## STL

### vector
```c++
vector<int> vec(num, inital);

vec.push_back(x);
vec.pop_back();
vec2.assign(vec.begin(), vec.end());
vec.insert(vec.begin()+index, x);
vec.erase(vec.begin()+index);
vec.clear()

N1 = vec.front();
Nn = vec.back();
vec.size();
vec.empty();

sort(vec.begin(), vec.end());
sort(vec.begin(), vec.end(), greater<int>());
reverse(vec.begin(), vec.end());
vector<int>::iterator it = find(vec.begin(), vec.end(), x);
vector<int>::iterator it = adjacent_find(vec.begin(), vec.end());//查找相邻重复元素
bool binary_search(vec.begin(), vec.end(), x);
int num = count(vec.begin(), vec.end(), x);
merge(v1.begin(), v1.end(), v2.begin(), v2.end(), vtarget.begin());
replace(vec.begin(), vec.end(), x1, x2);
int total = accumulate(v.begin(), v.end(), 0);
```

### string
```c++
strint s;

s.substr(index, n);
```

### deque 双端数组，可以对头端进行插入删除操作
```c++
deque<int> vec(num, inital);

dq.push_front(x);
dq.push_back(x);
dp.pop_front();
dq.pop_back();
```

### stack
```c++
stack<int> st;

st.push(x);
st.pop();
st.top();
```

### queue
```c++
queue<int> q;

q.push(x);
q.pop();
N1 = q.front();
Nn = q.back();
```

### list
```c++
list<int> l(num, inital);

l.push_back(x);
l.push_front(x);
l.pop_back();
l.pop_front();
l.insert(l.begin()+index, x);
l.clear();
l.erase(l.begin()+index);
l.remove(x);//删除容器中所有与x值匹配的元素。

N1 = l.front();
Nn = l.back();
for(list<int>::iterator it = L1.begin(); it != L1.end(); it++)
  cout << *it;
  
l.sort();
l.reverse();

bool myCompare(int val1 , int val2)
{
    return val1 > val2;
}
l.sort(myCompare);//从大到小
```

### set
```c++
set<int> s;

s.insert(x);
s.erase(s.begin()+index);
s.erase(x);
s.clear();

for (set<int>::iterator it = s.begin(); it != s.end(); it++)
  cout << *it;

pair<string, int> p("Tom", 20);
```

### map
```c++
map<int, int> m;

m.insert(pair<int, int>(index, x));
m[index] = x; 
m.erase(s.begin()+index);
m.erase(x);
m.clear();
```
