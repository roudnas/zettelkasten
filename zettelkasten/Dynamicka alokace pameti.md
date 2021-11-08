2021-11-08 13:01

# Dynamicka alokace pameti
Funkce malloc, ktera vraci void pointer.
```ad-info
title: Alokace na heap misto stacku
```
![[dynamic_allocation.png|550]]

````ad-example
title: Dynamicka alokace int[max] 
```ad-bug
title: Spatne naalokovana pamet
~~~C
#define ARR_MAX 1000000
int *arr = (int *) malloc(ARR_MAX);
~~~
```
```ad-success
title: Spravne naalokovana pamet
~~~C
#define ARR_MAX 1000000
/* 
** Malloc vraci void pointer, potreba konverze.
** Potreba dynamicky alokovat dle typu hodnot v poli.
*/
int *arr = (int *) malloc(ARR_MAX * sizeof(*arr));
~~~
```
````

## references
[[pole]]
[[C]]
[[pointers]]
[[BI-PA1]]