---
title: Paper Source Alma
weight: 1
---

# Paper Source Almak

## Indirilmesi Gerekenler
1. [Java 8](https://www.azul.com/downloads/?version=java-8-lts&package=jdk#zulu)
2. ~~[Git Bash](https://git-scm.com/downloads)~~
    <sub>(hatali oldugunu bildirdigi ve fixlememde yardimci oldugu icin @lavelty'ye tesekkur ederim)</sub>
3. [WSL](https://ubuntu.com/desktop/wsl)

## Kurulum

[Kurulum Videosu](https://www.youtube.com/watch?v=7fMxUuZzbRQ)

1. Istediginiz yere bir klasor acin.
2. O klasorun icerisinde WSL acin.
3. Acilan terminale sirasiyla
    ```bash
    sudo apt update
    sudo apt install openjdk-8-jdk
    sudo apt install maven
    sudo apt install dos2unix
    ```
    komutlarini girin
3. terminale `git clone https://www.github.com/papermc/paper-archive --branch ver/1.8.8` komutunu girerek paper reposunu klonlayin
4. Bu girdigimiz komut yuzunden `Paper` isimli bi klasor olusacaktir. `cd Paper` komutu ile o klasorun icerisine girin
5. `sudo dos2unix build.sh` <sub>(@p.leasan.t dosya formatlarindan kaynakli hatayi gosterdigi icin tesekkur ederim)</sub>
6. `sudo build.sh` komutunu calistirin
7. Bu komut size `The MD5 checksum of the downloaded server jar does not match the BuildData hash.` hatasi atacaktir.
8. `Paper` klasorunun icerisinde olan `work` klasorune girin, bu klasorun icinde olan `1.8.8` klasorunun icerisindeki `1.8.8.jar` dosyasini silin.
9. `1.8.8` klasorunun icerisine [indirdiginiz](https://getbukkit.org/get/5fafba3f58c40dc51b5c3ca72a98f62dfdae1db7) jari atip ismini `1.8.8.jar` olarak degistirin.
10. `Paper` klasorunun icerisinde `sudo build.sh` komutunu calistirin.
11. IntelliJ Idea ile `Paper` klasorunu acin

> **NOT**: Paperclip hatasi almaniz normal, goz ardi edebilirsiniz.

> **NOT**:
> ```
> Applying member mappings...
> Exception in thread "main" java.util.zip.ZipException: error in opening zip file
>	 at java.util.zip.ZipFile.open(Native Method)
>	 at java.util.zip.ZipFile.<init>(ZipFile.java:236)
>	 at java.util.zip.ZipFile.<init>(ZipFile.java:162)
>	 at java.util.jar.JarFile.<init>(JarFile.java:171)
>	 at java.util.jar.JarFile.<init>(JarFile.java:135)
>	 at net.md_5.ss.SpecialSource.map(SpecialSource.java:69)
>	 at net.md_5.ss.SpecialSource.main(SpecialSource.java:44)
>Failed to apply member mappings.
> ```
> hatasini alirsaniz [SpecialSource-2](https://hub.spigotmc.org/stash/projects/SPIGOT/repos/builddata/browse/bin/SpecialSource-2.jar?at=master) adli dosyayi indirip `BuildData\bin\` klasorunun icerisine atin ve `work\1.8.8\1.8.8-cl.jar` dosyasini silin

## Build
1. IntelliJ Idea uzerinde sagdaki `M` yazan logoya tiklayin.
2. Acilan menuden `PaperSpigot-Parent` yazisinin arkasindaki `>` yazisina tiklayin
3. Acilan menuden `Lifecycles` yazisinin arkasindaki `>` yazisina tiklayin
4. Menu
    ```
    ∨ PaperSpigot-Parent
      ∨ Lifecycle
        clean
        validate
        compile
        test
        package
        verify
        install
        site
        deploy
    ```
    seklinde gozukmeli
5. `package` secenegine cift tiklayin
6. islem bittikten sonra `PaperSpigot-Server\target` klasoru icerisindeki `paperspigot-1.8.8-R0.1-SNAPSHOT.jar` dosyasini kullanabilirsiniz.
