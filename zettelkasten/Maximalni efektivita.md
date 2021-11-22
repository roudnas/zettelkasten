2021-11-22 12:28

# Maximalni efektivita
```ad-note
title: K dispozici je pouze operace porovnani
```
Min slozitost porovnani pole je $$O(\log{n})$$
```ad-example
title: Binarni vyhledavani O(log n)

~~~C
int binarySearch ( int arr[], int n, int x ) {  
int lo = 0, hi = n-1, mid;  
while ( lo <= hi ) {  
mid = (lo + hi) / 2; /* toto neni 100% ok */  
if ( x < arr[mid]) hi = mid - 1;  
else if (x > arr[mid]) lo = mid + 1;  
else return 1;  
}  
return 0; /* nenalezeno */  
}
~~~

```
V pripade predchozi znalosti vstupnich dat se lze napriklad lin. interpolaci
dostat na 
$$O(\log{\log{n}})$$

## references
[[slozitost]]
[[BI-PA1]]
[[C]]
[[matematika]]