In my view, DivideAndRule is a method which can make a very big problem divide into pieces of small and same questions.
Always, these small questions have the same mode, if you understand what this mode actually is, then, the solution of this problem is easy to get.
For example, here is a classic problem about Divide and Rule --- Hanoi Tower.

```
#include <iostream>
#include <cstdio>
#include <algorithm>
#include <cmath>
using namespace std;
void Hanoi(int n, char first, char second, char third);
int main(void) {
   int n;

   cin >> n;

   cout << pow(2, n) - 1 << "\n";

   Hanoi(n, 'A', 'C', 'B');

    return 0;
}

void Hanoi(int n, char first, char second, char third) {
    if(n == 0) {
        return;
    }
    else {
        Hanoi(n - 1, first, third, second);
        cout << first << "->" << second << "\n";
        Hanoi(n - 1, third, second, first);
    }
}
```
Trough this example, you can clearly understand how the Divide and Rule run.
The Recursion use this method usually, and recusion is also used on Graph and Tree.
Though this part seems easy to understand, it always hard to edit the Recursive boundary and Recurive condition. Those are most improtant in Recusion.
