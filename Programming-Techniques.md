# Programming Techniques

## Language Features

C++ code template:

```
#include <bits/stdc++.h>

// Other libraries usually used:
// #include <iostream>
// #include <vector>
// #include <algorithm>

using namespace std;

int main(){

// solution comes here

}
```

For compilation:
```
g++ -std=c++11 -O2 -Wall test.cpp -o test
```
Where,
1. `-std=c++` refers to **C++11 standard**
2. `-O2` refers to **optimized code**
3. `-Wall` to show **warnings** about possible errors

### Input and Output

For **input**, `cin`, `scanf`, `getline`.

For **output**, `cout`, `printf`.

**Example**:

```
int a,b;
string x;

// For input
cin >> a >> b >> x;

// For output
cout << a << " " << b << " " << x << "\n";
```

**Sample input**
`10 2088 Vishwesh`

**Sample output**
`10 2088 Vishwesh`

**`cin` and `cout` are slower than `scanf` and `printf`. Add the following lines in starting of `main()` to make I/O more efficient**

```
ios::sync_with_stdio(0);
cin.tie(0);
```

**`endl` is slower than `"\n"` but causes flush operation.**

To read a whole line:

```
string s;
getline(cin, s);
```

If amount of data is unknown, use:

```
while (cin >> x){
	// process
}
```

For file I/O:

```
freopen("input.txt","r",stdin);
freopen("output.txt","w",stdout);
```

