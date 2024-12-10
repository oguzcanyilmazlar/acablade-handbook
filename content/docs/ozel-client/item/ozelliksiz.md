---
title: Ozelliksiz Item
weight: 2
---
Ornek olarak kendi clientimda olan 853 id'li `hammer` esyasini ekleyecegim ben
1. `\net\minecraft\server\Item` classinda **CTRL + F** yapip `rabbit_foot` aratin
2. Bu gordugunuz satirdaki metodun aciklamasi [Item](../#bilinmesi-gerekenler) sayfasinda var
3. Bu satiri kopyaladiktan(secim yapmadan **CTRL + C** yaparsaniz tum satiri kopyalar) sonra bu metodun sonuna yapistirin(`record_wait` itemi eklendikten sonra benim icin)
4. Kopyaladiktan sonra [Item](../#bilinmesi-gerekenler) sayfasinda anlattigim gibi duzenledigimde
    ```java
    ...
    a(2267, (String)"record_wait", (new ItemRecord("wait")).c("record"));
    a(853, "hammer", (new Item()).c("hammer"));
    ...
    ```
    seklinde gozukuyor.
5. [Materyal ekleyin](../materyal)
