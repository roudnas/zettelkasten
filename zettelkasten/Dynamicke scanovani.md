2021-11-08 13:36

# Dynamicke scanovani
```ad-example
title: Avg.c
~~~C
int *data = NULL;
int dataNr = 0;
int x;
while ( scanf("%d", &x) == 1 ) {
	//Alokace pro nove cislo
	int *tmp = (int*) malloc( sizeof(*tmp) * (dataNr + 1) );
	for ( int i = 0; i < dataNr; i++) 
		tmp[i] = data[i]
	tmp[dataNr++] = x;
	data = tmp;
}

if ( !feof(stdin) ) {
	return EXIT_FAILURE;
}

double avg = 0;
for ( int i = 0; i < dataNr; i++)
	avg += data[i];

double stdDev = 0;
for (int i = 0; i < dataNr; i++)
	

~~~

```
## references
[[Dynamicka alokace pameti]]
[[C]]
[[pole]]