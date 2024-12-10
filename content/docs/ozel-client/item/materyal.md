---
title: Materyal Ekleme
weight: 1
---

## Ilk Kurulum
1. `PaperSpigot-API\src\main\java\org\bukkit\Material` classina gelin, **CTRL + F**  yapin ve `Material[] byId` diye aratin
2. buldugunuz satirdaki `383` yerine `Material.values().length` yazin.
3. satirin son hali
    ```java
    private static Material[] byId = new Material[Material.values().length];
    ```
    seklinde olmali

## Yeni Materyal Ekleme
1. `PaperSpigot-API\src\main\java\org\bukkit\Material` classinda `RECORD_12(` diye aratin.
2. Buldugunuz satirin altina yeni satir acin (`;` olan satirin ustu)
3. `MATERYAL_ADI(item_id),` seklinde yazin.
4. [Ozelliksiz Item](../ozelliksiz.md) orneginde ekledigim hammer itemi icin son sekli asagidaki gibi oluyor:
    ```java enum
    ...
    RECORD_12(2267),
    HAMMER(853),
    ;
    ...
    ```
5. Bundan sonra eklediginiz materyalleri bu eklediginiz materyalin altina ekleyin.
