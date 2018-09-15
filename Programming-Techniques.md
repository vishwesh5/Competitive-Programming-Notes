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

### Working with Numbers

**Integers**

1. `int`: 32-bit, **Range: -2^31 to 2^31 - 1, or -2 * 10^9 to 2 * 10^9)**.
2. `long long`: 64-bit, **Range: -2^63 to 2^63 - 1, or -9 * 10^18 to 9 * 10^18)**. Example: `long long x = 123456789123456789LL;`

**Common mistake**
```
int a = 123456789;
long long b = a*a;
cout << b << "\n";
```
`a*a` will still return an `int` creating **overflow**.

**Solution**: use `long long a` instead of `int a`.

**Modular arithmetic**

1. `(a+b) mod m = (a mod m + b mod m) mod m`
2. `(a-b) mod m = (a mod m - b mod m) mod m`
3. `(a*b) mod m = (a mod m * b mod m) mod m`

**For negative numbers**

```
x = x%m;
if (x < 0) x+= m;
```

**Floating point numbers**

