\# Modern ABAP Syntax Examples



\## Inline Declaration



```abap

DATA(lv\_matnr) = 'MAT001'.



DATA(ls\_mara) = VALUE mara(

&#x20; matnr = 'MAT001'

&#x20; mtart = 'FERT'

).





DATA(lv\_status) =

&#x20; COND string(

&#x20;   WHEN lv\_qty = 0 THEN 'SEM STOCK'

&#x20;   ELSE 'OK'

&#x20; ).



DATA(ls\_mara) = lt\_mara\[

&#x20; matnr = lv\_matnr

].





















