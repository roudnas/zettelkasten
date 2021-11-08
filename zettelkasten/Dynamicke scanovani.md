2021-11-08 13:36

# Dynamicke scanovani
```ad-danger 
title:Dynamicky naalokovana data je potreba radne uvolnovat.
```
```ad-example
title: Avg.c
Vypocet prumeru a standardni odchylky n cisel.
~~~C
int *data = NULL;
int dataNr = 0;
int dataMax = 0;
int x;
while ( scanf("%d", &x) == 1 ) {
	if ( dataNr == dataMax ) {
		/* Paket dat nastavujeme na n
		** Iterujeme pres paket.
		*/
		dataMax += dataMax / 2 + 20;
		//Alokace pro nove cislo
		data = (int*) realloc( sizeof(*data) * (dataMax) );
		/*
		int *tmp = (int*) malloc( sizeof(*tmp) * (dataNr + 1) );
		for ( int i = 0; i < dataNr; i++) 
			tmp[i] = data[i]
		// naalokovana stara data je potreba uvolnit
		free(data);
		data = tmp;
		*/
	}
	data[dataNr++] = x;
}
if ( !feof(stdin) ) {
	free(data);
	return EXIT_FAILURE;
}
double avg = 0;
for ( int i = 0; i < dataNr; i++)
	avg += data[i];
avg /= dataNr;

double stdDev = 0;
for (int i = 0; i < dataNr; i++)
	stdDev += (data[i] - avg) * (data[i] - avg);
stdDev = sqrt(stdDev/dataNr);

~~~

```
## references
[[Dynamicka alokace pameti]]
[[C]]
[[pole]]
[[slozitost]]
[[BI-PA1]]