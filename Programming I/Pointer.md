>[!icon]
>int\* p - Pointervariable
>int\*\* p - Pointer Pointervariable
>&p - Adresse
>\*p - Wert in einer Adresse


```cpp
#include <stdio.h>
#include <iostream>

int main() {
 int m = 7; // m speichert den Wert 7
 int* p = &m; // p speichert die Adresse von m
 int** q = &p; // q speichert die Adresse von p
 printf("m hat den Wert: %i\n", m);
 std::cout << "Der Wert von m steht an der Adresse: " << p << std::endl;
 std::cout << "p steht an der Adresse: " << &p << std::endl;
 std::cout << "m hat den Wert: " << *p << std::endl;
 std::cout << "m hat den Wert: " << **q << std::endl;
 //m = m + 1;
 *p = *p + 1;
 printf("m hat den Wert: %i\n", m);
}
```

```cpp
#include <iostream>

void foo(int *m) {
 ++*m;
 std::cout << *m << std::endl;
}
int main() {
 int a = 7;
 foo(&a);
 std::cout << a << std::endl;
}
```
