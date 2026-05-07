# Modern ABAP Syntax Examples

## Inline Declaration

```abap
DATA(lv_matnr) = 'MAT001'.
```

## VALUE

```abap
DATA(ls_mara) = VALUE mara(
  matnr = 'MAT001'
  mtart = 'FERT'
).
```

## COND

```abap
DATA(lv_status) =
  COND string(
    WHEN lv_qty = 0 THEN 'SEM STOCK'
    ELSE 'OK'
  ).
```

## Table Expression

```abap
DATA(ls_mara) = lt_mara[
  matnr = lv_matnr
].
```