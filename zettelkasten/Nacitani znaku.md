2021-11-08 11:18

# Nacitani znaku
```ad-info
title: Nebezpecne nacitani retezce

```ad-bug
~~~C
scanf("%s");
~~~
```


Je temer vzdy prilis nebezpecne nacitani retezce.
Hrozi buffer overflow
```ad-success
title:Spravne nacitani retezce
~~~C
//max_size = 99
scanf("%99s");
~~~

```

## references
[[retezce]]
[[pole]]
[[C]]
[[BI-PA1]]