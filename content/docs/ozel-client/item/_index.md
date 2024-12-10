---
title: Item Nasil Eklenir
bookCollapseSection: true
weight: 2
---

## Kurulum
1. IntelliJ Idea uzerinden `Paper` klasorunu acin. (Bu adimdan sonraki adimlarin hepsi intellij idea uzerinden devam edecek)
2. `PaperSpigot-Server\src\main\java\net\minecraft\server` icerisinde `ItemArmor` adindaki classa gelin.
3. `extends Item` yazan kisimdaki `Item` yazisinin ustune gelip **CTRL + SOL TIK** yapin.
4. Karsiniza cikan classi **CTRL + A** yaptiktna sonra **CTRL + C** yaparak kopyalayin.
5. `PaperSpigot-Server\src\main\java\net\minecraft\server` icerisinde `Item` adinda yeni bi class olusturun.
6. Bu class icerisinde **CTRL + A** sonra **CTRL + V** yapin.

Hangi item turu istediginize gore asagidaki yazilardan takip edin.
- [Ozelliksiz Item](./ozelliksiz): sag tik ya da sol tik yaptiginizda bir sey olmayan, armor, kilic gibi kullanilamayan temel duzeyde ozelliksiz itemler. Vanilla ornegi: deri, tavsan ayagi, kulceler...
- Baska item turleri de eklenecek


## Bilinmesi Gerekenler
Item Classindaki metodlar:
> a(item_idsi, itemin_ismi, item_obje) -> itemi tanimlar
> c(itemin_internal_ismi) -> tam islevini bilmiyorum fakat eklenmesi gerek
> **NOT**: itemin_ismi `rabbit_foot` tarzi iken itemin_internal_ismi `rabbitFoot` seklinde olmali (sart degil fakat minecraft devleri yaparken boyle yapmis)
