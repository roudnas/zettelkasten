2021-11-08 13:01

# Dynamicka alokace pameti
Funkce malloc: void pointer.
```ad-info
title: Alokace na heap misto stacku
```

```ad-example
Dynamicka alokace int[max]
```ad-bug
~~~C
#define ARR_MAX 1000000
int *arr = (int *) malloc(ARR_MAX);
~~~
```
```C
#define ARR_MAX 1000000
/* 
** Malloc vraci void pointer, potreba konverze.
** Potreba dynamicky alokovat dle typu hodnot v poli.
*/
int *arr = (int *) malloc(ARR_MAX * sizeof(*arr));
```
## references
[[pole]]
[[C]]
[[pointers]]