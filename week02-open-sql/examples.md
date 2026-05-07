\# Modern Open SQL Examples



\## Basic SELECT



```abap

SELECT matnr,

&#x20;      mtart

&#x20; FROM mara

&#x20; INTO TABLE @DATA(lt\_mara).

```



\## SELECT with WHERE



```abap

SELECT matnr,

&#x20;      ersda

&#x20; FROM mara

&#x20; WHERE mtart = 'FERT'

&#x20; INTO TABLE @DATA(lt\_materials).

```



\## INNER JOIN



```abap

SELECT mara\~matnr,

&#x20;      makt\~maktx

&#x20; FROM mara

&#x20; INNER JOIN makt

&#x20;   ON makt\~matnr = mara\~matnr

&#x20; WHERE makt\~spras = @sy-langu

&#x20; INTO TABLE @DATA(lt\_result).

```



\## Aggregate Function



```abap

SELECT werks,

&#x20;      COUNT( \* ) AS total

&#x20; FROM marc

&#x20; GROUP BY werks

&#x20; INTO TABLE @DATA(lt\_count).

```



\## CASE Expression



```abap

SELECT matnr,

&#x20;      CASE mtart

&#x20;        WHEN 'FERT' THEN 'Finished Product'

&#x20;        WHEN 'ROH'  THEN 'Raw Material'

&#x20;        ELSE 'Other'

&#x20;      END AS material\_type

&#x20; FROM mara

&#x20; INTO TABLE @DATA(lt\_material\_type).

```

