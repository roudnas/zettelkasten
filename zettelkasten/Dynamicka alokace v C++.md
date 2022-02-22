2022-02-22 11:10

# Dynamicka alokace v C++
Klicove slova `new` a `delete`
```C++
// Dynamicky alokovan int
int *x = new int();
// Inicializace na 10
int *xIsTen = new int(10);

int *arr = new int[1000];

delete x;
delete xIsTen;
delete []arr;
```
## references
[[BI-PA2]]
[[C++]]
[[Dynamicka alokace pameti]]