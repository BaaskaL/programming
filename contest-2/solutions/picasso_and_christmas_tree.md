# Picasso and Christmas Tree
* болон - тэмдэгт ашиглан  өндөртэй дараах хэлбэрийн гацуур мод хэвлэ.

## Input
Ердөө л _**N**_ тоо.

## Output
_**N**_ мөрөөс тогтох дараах хэлбэрийн гацуур мод.

## Constraints
- **N &le; 127**

##### Sample Input 0
```
1
```
##### Sample Output 0
```
*
```

##### Sample Input 1
```
2
```
##### Sample Output 1
```
-*-
***
```

##### Sample Input 2
```
4
```
##### Sample Output 2
```
---*---
--***--
-*****-
*******
```
##### Sample Input 3
```
8
```
##### Sample Output 3
```
-------*-------
------***------
-----*****-----
----*******----
---*********---
--***********--
-*************-
***************
```

## Solution
```
#include <iostream>
using namespace std;

void print(char c, int times) {
    while (times--) {
        cout << c;
    }
}

int main() {
    int N;
    cin >> N;
    for (int i = 0; i < N; i++) {
        print('-', N - i - 1);
        print('*', 2 * i + 1);
        print('-', N - i - 1);
        cout << endl;
    }

    return 0;
}
```