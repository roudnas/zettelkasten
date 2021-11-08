2021-11-08 11:59

# Eratosthenovo sito
Efektivneji nalezame prvocisla vyskrtavanim nasobku prvocisel z ciselne rady.
```ad-info
title: Graficka reprezentace
![[eratosthen-sieve.png|50vw]]
```
```ad-example
title: Implementace
~~~C
void sieve(char set[], int max) {
	int p = 2, pmax = (int) sqrt(max);
	for ( int i = 0; i < max; i ++)
		set[i] = 1;
	set[0] = set[1] = 0; //0 a 1 nejsou prvocisla
	do { 
		for (int i = p*p; i < max; i+=p)
			set[i] = 0; //skrtani nasobku
	} while (p <= pmax);
}
~~~
```
## references
[[pole]]
[[prvocisla]]
[[C]]
[[BI-PA1]]