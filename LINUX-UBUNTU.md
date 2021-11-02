﻿﻿# **LINUX NEDİR**
Linux bilinenin aksine bir işletim sistemi değil, **işletim sistemi çekirdeğidir.** 

**Linux dağıtımları** ise Linux çekirdeğinin üzerine eklenen yazılım ve araçlara denir. Yani Linux dağıtımları Linux çekirdeğini işletim sistemi haline getirir.

Bir Linux dağıtımının içerisinde

- Linux çekirdeği
- GNU yazılımları
- Paket Yöneticisi

bulunmaktadır. 

Debian, Manjaro, Ubuntu, Manjaro gibi dağıtımlar Linux çekirdeği ve gerekli yazılımlar ile birleşip işletim sistemi haline gelmiştir.

Linux çekirdeği(Kernel) işletim sisteminin kalbidir. Sebebi ise **donanım ile yazılımı** birbirine bağlamaktadır. Yani bu durumda Linux çekirdeği donanımı sarmalamaktadır.

Bizim bilgisayarla iletişim kurabilmemiz ve emir verebilmemiz için çekirdeğe(kernel) ihtiyacımız vardır ancak bunu direkt olarak yapamayız. Komutlarımızı kernele ileterek işlemler yapmamızı sağlayan komut satırına ise **kabuk(shell)** denir.

Kısaca kabuk(shell) donanım ve çekirdeği(kernel) sarmalamaktadır.

![](img/Aspose.Words.b6e0df8a-337a-49f3-bb0c-f932a633c435.001.png)





Shell,  çekirdek ile kullanıcı arasında ki iletişimi sağlar. Böylece emirleri yerine getirebilir.

Linux’un kullandığı Shell aracı programı  Bourne Again Shell ifadesinin kısaltması olan **BASH**’dir. 
# **LINUX DİZİN HİYERARŞİSİ HAKKINDA BİLİNMESİ GEREKENLER**
Öncelikle Linux C: D: vb. sürücüleri bulundurmaz. **Tekil Hiyerarşik Dizin** Yapısını kullanır. 

Tekil hiyerarşik dizin yapısında tüm dosya, dizin, disk, işlemler vb. **eğik çizgi(/)** ile belirtilen, **kök dizin** veya ağaç yapısı olarak adlandırılan yapıda tutulur.

**Kök dizin(/)** adından da anlaşılacağı üzeri en başta ki dizindir ve altında herhangi bir dizin yoktur. Yani son ulaşabileceğimiz dizindir.

Tüm dizinlerin adının sonunda (/) simgesi bulunur ve bunun dizin olduğu anlamına gelir.

**Peki kök dizin içerisinde hangi dizinler bulunur.**
### **/bin**
İşletim sistemine ait komutların bulunduğu dizindir.

Linux dağıtımlarında sıklıkla kullanılan **ls, ping, mkdir vb. komutlar** bu dizin içerisinde yer alır.
### **/boot**
İşletim sistemini başlatılması için kullanılan Linux çekirdek dosyaları bu dizinde bulunur. Örneğin grub, lilo vb.
### **/etc**
**Linux işletim sisteminde ki en önemli dizindir.** Bu dizin içerisinde işletim sistemi ve uygulamaların ayarları bulunmaktadır.
### **/home**
Kullanıcılara ait dosyaların bulunduğu dizindir.

Yeni bir kullanıcı oluşturulduğunda /home dizini altında kullanıcı adına sahip bir dizin oluşturulur ve kullanıcı verilerini bu dizine yükler.

### **/lib ve /lib64**
Sistemdeki uygulamaların çalışabilmesi için gerekli olan kütüphane dosyaları bu dizinlerde yer alır. Linux türevi işletim sistemlerinde kütüphane dosyaları **.so** uzantılıdır.
### **/media**
Sistem üzerindeki CD-Rom, USB bellek vb. çıkarılabilir aygıtlara bu dizin üzerinde erişilir. Aygıtlara erişebilmek için bağlama (**mount**) işleminin yapılması gerekir.
### **/mnt**
Sistem üzerindeki çeşitli birimleri **geçici** olarak bağlama (**mount**) işleminin yapıldığı dizindir. Bu dizin **/media** diziniyle aynı işleve sahiptir. Çoğunlukla sistem yöneticileri tarafından yedekleme, onarım vb. işlemler içi kullanılır.
### **/opt**
Yüklenecek çeşitli uygulamaların bulunduğu dizindir. Uygulamalar farklı dizinlere de kurulabilir ancak bu dizin genel kabul görmüştür.
### **/proc**
![](img/Aspose.Words.b6e0df8a-337a-49f3-bb0c-f932a633c435.002.png)
Çalışan aygıt ve işlemlerle ilgili bilgilerin olduğu dizindir. Örneğin; Sistemdeki işlemciyle ilgili bilgi almak için **/proc/cpuinfo** yolu kullanılır.





### **/root**
Linux tabanlı sistemlerde en yetkili kullanıcı olan **root** kullanıcısına ait verilerin saklanabileceği dizindir.
### **/run**
Çalışan dosyalarla ilgili bilgilerin bulunduğu dizindir. Dizin önceki Linux sürümlerinde /var/run içerisinde yer alan dosyaları tutar.
### **/sbin**
Sistem yönetimi için kullanılan ve sadece yetkili kullanıcıların kullanabileceği komutların yer aldığı dizindir.
### **/srv**
Sistem içinde bulunan servislerle ilgili dosyaların yer aldığı dizindir.

Bunlar sadece bazılarıdır.

Tam liste olarak verilirse eğer;

**/bin, /boot, /dev, /etc, /home, /lib ve /lib64, /media, /mnt, /opt, /proc, /root, /run, /sbin, /srv, /sys, /tmp, /usr, /var, /lost+found, /etc/fstab, /proc/meminfo, /var/log**
# **LINUX KOMUTLARI**
# **1-cd Komutu**

Linux dosya sistemi içerisinde gezinmek için kullanılır. Büyük küçük harfe duyarlıdır. Bu sebep ile dizin adı tam olarak girilmelidir. Dizin adı aranırken tam arama yapmadan TAB tuşuna basarak dizin adı tamamlanabilir. Ancak klavyeden girilen dizin adı ile aynı isimle başlayan farklı bir dizin varsa iki kere TAB tuşuna basılmalıdır.  

**man-cd**

**`man -cd`** komutu ile hakkında detaylı bilgi ve parametrelere ulaşılabilir.

Örnek kullanımı;

**`cd home/Desktop`**

Böylece home dizini altındaki Desktop dizinine girecektir.
# **2-pwd Komutu**

Pwd komutu o an hangi dizin içerisinde bulunduğumuzu gösterir. Kesin ve net bir konum bilgisi sağlar. Kullanımı;

**`pwd`**
# **3-man komutu**
Komutun alabileceği tüm parametreleri ve neler yapabileceğini gösterir. Örneğin;

**`man ls`**
# **4-ls komutu**
Ls komutu bulunan dizin içerisinde ki dizin ve dosyaları listeler.

**`ls`  dizin içerisinde bulunan dizin ve dosyaları listeler**

**`ls *.htm`  uzantısı htm olan dosyaları listeler.**

**`l -`** parametresi kullanıldığında dosya ve klasörleri ayrıntılı listeler.

**`l -F`** parametresi kullanıldığında dizin içerisinde ki dosya türlerinin ne olduğunu gösterir.



![](img/Aspose.Words.b6e0df8a-337a-49f3-bb0c-f932a633c435.003.png) 

Çıktıda en solda ki harfler belirli anlamlar barındırır.

İlk harf ögenin dosya mı yoksa klasör mü olduğunu gösterir.
**d** ise klasör, 
**-** ise dosyadır

**r**: Okuma iznini belirtir.
**w**: Yazma iznini belirtir.
**x**: Yürütme iznini belirtir.

Yani **boot** klasöründen örnek verecek olursak;

`drwxr-xr-x`  -> Bu bir klasör olduğu ve sahibinin okuma,yazma,yürütme  -  grubunun okuma,yürütme  -  diğerlerinin  yürütme izni vardır.





# **LINUX DOSYA VE DIZIN IZINLERI**
## **1-(chmod)Dosya ve Dizin yetkilendirmesi yapmak**

Linux’ta ki her şey dosya olduğu için dosya sistem güvenliği çok önemlidir. Her dosyaya verilen erişim izni sayesinde sistem yönetimi oldukça kolaydır. Sistem üzerinde ki kullanıcıların erişim hakları belirli izinlere göre yönetilir. Bunlar;

- **r -  Okuma izni(read)**
- **w - Yazma izni(write)**
- **x - Çalıştırma izni(execute)**

Dosya ve dizinlerin izinlerini öğrenmek için **`stat`** veya **`ls -l`** komutunu kullanabiliriz. **`ls-l`** komutu ile dizin içerisinde ki bütün dosyaların izinlerini görebiliriz. **`stat`** komutu ile istediğimiz dosyanın erişim iznini görebiliriz.

![](img/Aspose.Words.b6e0df8a-337a-49f3-bb0c-f932a633c435.004.png)

Dosya ve dizin erişim hakkı 3 grupta incelenir;

- **Dosya sahibi**
- **Dosya sahibinin grubu**
- **Diğer kullanıcılar**

Dosya izinleri için bir örnek;

**-rwxrw-r--**   Burada ki kodda şu anlatılmaktadır. İlk harf dosya türünü söyler.

Tire harfi ise dosya , d harfi ise dizindir

- '-' : dosya
- 'd' : dizin

daha sonra gelenler ise 3 ayrı parçaya ayrılır. Burada ki örnekte 3 parçaya ayırırsak;

(rwx) – (rw-) – (r--)

Yani;

- (rwx) -> Dosya sahibi okuma, yazma ve çalıştırma iznine sahiptir
- (rw-) -> Dosya sahibi grubu okuma ve yazma iznine sahiptir.
- (r--) -> Diğer kullanıcılar ise yalnızca okuma iznine sahiptir.

**Peki dosya izinlerini nasıl yönetiriz?**

Dosya ve dizin izinleri yönetmek için **chmod** komutu kullanılmaktadır. **chmod** komutunun aldığı belirli parametreler ile bu izinler düzenlenebilir, çıkarılabilir ve eklenebilir.

2 ayrı kullanım şekli vardır.

1. **Kullanımı**

chmod komutunun aldığı parametrede ki anlamsal ifadeler;

- **u** - dosya sahibi(user)
- **g** - dosya sahibinin grubu(group)
- **o** - diğer kullanıcılar(others)
- **a** - tüm haklar
- **+** - yetki ekle
- **-** - yetki çıkar
- **r** - okuma yetkisi(read)
- **w** - yazma yetkisi(write)
- **x** - çalıştırma yetkisi(execute)

**`chmod o+w <dosyaAdi>`** Diğer kullanıcılara yazma yetkisi verir.

**`chmod ug+rwx <dosyaAdi>`** Dosya sahibi ve grubuna okuma,yazma ve çalıştırma yetkisi verir.

**`chmod o-w <dosyaAdi>`** Diğer kullanıcıların yazma yetkisini kaldırır

2. **Kullanımı**

Chmod da sayısal ifadelerle de yetkilendirme yapabiliriz.

- **4** – okuma yetkisi
- **2** – yazma yetkisi
- **1** – çalıştırma yetkisi
- **0** – yetki kaldırma

**Chmod [dosyaSahibi] [Grubu] [DiğeKullanıcılar] <dosyaAdi.>**

İlk rakam dosya sahibine aittir, ikinci rakam grubuna, üçüncü rakam diğer kullanıcılara aittir.

Örneğin dosya sahibine okuma,yazma çalıştırma yetkisi verelim

Yani o halde 4+2+1 = **7** rakamını vereceğiz.

Grubuna okuma ve yazma yetkisi verelim. 4+2 = **6** vereceğiz

Diğer kullanıcılara da yalnızca okuma yetkisi verelim **4** vereceğiz

O halde **`chmod 764 <dosyaAdi>`** olacaktır.

#

## **2-(chown)Dosya ve Dizin sahibini değiştirmek**
**chown** komutu ile dosya veya dizin sahibini değiştirebiliriz.

**`chown <Kullanici> <dosyaAdi>`**
 ## **3-(chgrp)Dosya ve Dizin grubunu değiştirmek**
chgp komutu ile dosya veya dizin grubunu değiştirebiliriz.

**`chgrp <grup> <dosyaAdi>`**

Örnek olarak dosyamızın grubunu değiştirelim. Önce dosyamızın hangi guruba ve usera ait olduğuna bakalım;



![](img/useraddr17.png)

dosyanın **useri root**,     **grubu yeniGrup** olarak görünüyor. Şimdi grubumuzu **testGrup** yapalım;

![](img/useradd18.png)

```
chgrp testGrup 01-network-manager-all.yaml
```

Yazdığımız komut ile artık grubumuz **testGrup** adlı gruba geçti.

## **(chattr) Dosya Kilitlemek**

Bu komut bir dosyanın değiştirilme, **silinme** vb. gibi durumların yaşanmasını engellemektedir. Öyle bir komuttur ki **root** kullanıcısı bile dosya üzerinde bir değişiklik veya silme işlemi yapamaz. Hatta daha ileri gidersek **sistemin kendisi bile** dosya üzerinde bir değişiklik veya silme işlemi yapamaz.

Komutumuzun kullanımı **`chattr +i dosyaAdi`** şeklindedir. 

Bu tür kilitli dosyaları listelemek için **`lsattr`** komutunu kullanmaktayız. Şimdi öncelikle;

```
lsattr
```

komutunu kullanarak dosyalarımızı listeleyelim.

![](img/useradd19.png)

Dosyalarımız bu şekilde görünmektedir. Şimdi ise **test.txt** dosyamızı kilitleyelim

Bunun için ;

```
chattr +i test.txt
```

komutumuzu kullanalım.

![](img/useradd20.png)



 Şimdi tekrar  **`lsattr`** komutumuz ile dosyalarımızı listeleyelim. Bakalım istediğimiz şekilde **test.txt** dosyamız kilitlenmiş mi?



![](D:\LINUX-UBUNTU\img\useradd21.png)

Dosyamız sistem tarafından kilitlenmiş görünüyor. Şimdi **root olarak silmeyi deneyelim**

![](D:\LINUX-UBUNTU\img\useradd22.png)

**root** kullanıcı ile silmek istesek bile izin vermedi. 

Şimdi **dosyamızın kilidini kaldıralım**

Bunun için **`chattr -i dosyaAdi`** komutunu kullanırız.

```
chattr -i test.txt
```

![](D:\LINUX-UBUNTU\img\useradd23.png)

Böylece dosyamızın kilidini kaldırmış olduk.




# **LINUX DOSYA VE DIZIN KOMUTLARI**
# **1-touch**
Genel olarak dosya oluşturmak için kullanılır. Ancak komutun ana işlevi mevcut dosyaların tarih bilgisini değiştirmektir.

Parametre olarak verilen dosya mevcut değilse oluşturulur. Kullanımı;

**`touch <dosyaAdi>`**

**`touch dosya1`**

# **2-mkdir**
Klasör oluşturmak için kullanılır. Yeni bir dizin oluşturulabilir.

**`mkdir <dosyaAdi>`**

**`Mkdir klasor1`**
# **3-mv**
Dosya ve dizin taşımak veya yeniden adlandırmak için kullanılır.

**`mv <kaynak> <hedef>`**

**`mv dosya1  serdar/Desktop/`**

**`mv <eski\_isim> <yeni\_isim>`**

**`mv dosya1  dosya1Yeni`**

# **4-cp**
Dosya kopyalamak için kullanılır.

Dizin kopyalamak için **–r** parametresi almalıdır.

**`cp <kaynak> <hedef>`**

**`cp dosya1   serdar/Desktop/`**

**`cp -r dizin1/   home/serdar/`**

# **5-rm**
Dosya silmek için kullanılır.

Dosyayı silmeye zorlamak için **–f** parametresi kullanılır

Dizin silmek için **–r** parametresi almalıdır.

**`rm <dosyaAdi>`**

**`rm -r <dizinAdi>`**
# **6-cat**
Dosya içeriğini okumak için kullanılır. Ayrıca  dosya içerisine yazmak içinde kullanılabilir.

**`cat <dosyaAdi>`**          dosyayı okur.

**`cat -n <dosyaAdi>`**  -n parametresi ile dosya içine yazılabilir. Yazdıktan sonra çıkmak için **ctrl+c**
# **7-head**
Dosya içeriğini dosya başından itibaren okumak için kullanılır. Varsayılan olarak ilk 10 satırı okur. Satır sayısı belirtmek için -n parametresi kullanılır

**`head <dosyaAdi>` , `head -n20 <dosyaAdi>`**
# **8- tail**
Dosya içeriğini sonundan itibaren okumak için kullanılır. Varsayılan olarak ilk 10 satırı okur. Satır sayısı belirtmek için -n parametresi kullanılır

**`tail <dosyaAdi>` , `tail -n15 <dosyaAdi>`**
# **9-more**
Dosya içeriğini parça parça okumak için kullanılır. Sayfaları ilerlemek için **space**, komuttan çıkmak için **q** tuşu kullanılır

**`more <dosyaAdi>`**
# **10-less**
Dosya içeriğini **more** komutundan daha fazla seçenekle parça parça okumak için kullanılır. Yukarı aşşağı tuşu ile sıralı okunabilir.

**`less <dosyaAdi>`**
# **11-nl**
Dosya içeriğini satır numarası ekleyerek okuma yapar.
**`nl <dosyaAdi>`**
# **12-pr**
Dosya içeriğini sayfalayarak okumak için kullanılır.
**`pr <dosyaAdi>`**
# **13-file**
Dosya ile ilgili bilgi almak için kullanılır.
**`file <dosyaAdi>`**
# **14-stat**
Dosya ile ilgili detaylı bilgi almak için kullanılır.
**`stat <dosyaAdi>`**


# **LINUX ARAMA KOMUTLARI**
## **1-grep**
Dosya içerisinde harf veya kelimeyi arar. Dosya içerisinde arama yapar.
**`grep <aranacakKelime> <dosyaAdi>`**

**-v parametresi ile dosya içinde bulunmayan kelimeleri getirir.**
**`grep –v  <aranmayacakKelime> <dosyaAdi>`**

**-i parametresi ile büyük-küçük harf duyarlılığını kaldırır.**
**`grep –i  <aranacakKelime> <dosyaAdi>`**

**-r parametresi aramayı dizin altında ki tüm dosya ve dizinlerde yapar.**
**`grep –r  <aranacakKelime> <dizinAdi>`**

**-ir parametresi arama sırasında başlangıç (^) ve bitiş ($) karakterleri ile arama yapılabilir.**

**`grep -ir <^aranacakKelime> <dosyaAdi>`** 

**`grep -ir ‘Ka’ dosya1`**

## **2-find**
Geniş bir kullanımı olan arama komutudur.

-name ve -type opsiyonu genel olarak kullanılır

-type d = dizi   -type f =dosya

-type belirtmezsek o isme sahip dosya ve dizinleri listeler.

**`find <aramaYapilacakDizin> <opsiyon –name/-type> <aranacakOrgu>`**

**`find / -name “Error.log”`**

**`find / -type d  -name “dizinSerdar”`**

Belirli bir uzantıya ait dosyaları aramak için <\*.txt>  gibi kullanılabilir.

Aranacak dosya veya dizin adı tam olarak bilinmiyorsa <aran\*> gibi kullanılabilir.

Boş dosya veya dizinleri bulmak için sonuna  **-empty** parametresi kullanılır. 

**`find <arama\_yeri> -name <aranan> -empty`** gibi

Bulunan ifadeler için komut çalıştırmak için **exec** parametresi kullanılır.

Örneğin rm komutu ile bulunanı sileceğiz..

**`find<aramaYapilacakDizin>  -name <aranacak> -exec rm -r {} \;`**

Boyuta göre KB cinsinden arama yapması için;

**`find  /etc  -size 500`**

**Sunucuda tüm .log dosyaları bulmak istersek, \* işaretini kullanırız**

**`find / -name “\*.log”`**
## **3- Locate**
Locate komutu find komutu gibi dosya adı ile arama yapmamızı sağlar ancak find komutundan çok daha hızlıdır. Çünkü find taramaları gerçek zamanlı yaparken **locate dosyayı daha önce katoglanmış veritabanından tarar.**

Locate komutu **var/lib/mlocate/mlocate.db** isimli veritabanını kullanmaktadır.

Locate komutunu kullanmadan önce **updatedb** komutunu çalıştırmalıyız. Sebebi ise mlocatedb veritabanını **updatedb** komutu oluşturur ve günceller. Veritabanının güncel kalması için sorgulama sırasında çalıştırılması gerekir.

Ancak updatedb komutunu root kullanıcısı veya sudo olarak çalıştırmamız gerekmektedir.

Bunun için root olarak giriş yapmalı veya sudo ile;

**`sudo updatedb`** Komutunu kullanmalıyız.

Eğer terminalde komut tanınmaz ise sistem tarafından ön yüklü değildir. Bunun **için mlocate paketini** kurmalıyız. 

Linux dağıtımı olan Ubuntu için :  `sudo apt install mlocate` 

Böylece mlocate paketini kurmuş olacağız. Ardından updatedb komutunu kullanıp veritabanımızı güncelledik. Artık **locate** komutunu kullanabiliriz.

**`locate <dosyaAdi>`**

**`Locate dosyaAdi`**

Eğer küçük-büyük harf duyarlılığını istemiyorsak **-i** parametresini kullanabiliriz.

**`locate -i DOSYaADi`**
## **4-whereis ve which**

# **LINUX SIKIŞTIRMA IŞLEMLERI**

Linux dağıtımlarında arşivleme veya yedekleme işlemleri için gzip, bzip2, lzma vb. yöntemler ve komutları mevcuttur.

## tar



Arşivleme ve dosyaları bir formatta tutmak için **tar** komutunu kullanırız.  işlemler **tar** komutuna çeşitli parametreler verilerek yapılır.

Komutun alabileceği parametrelerden bazıları;

**c** - arşiv oluşturmak için,

**f** - dosyaya yazdırmak için,(gerekli parametre) (hangi dosyaya yazılıacağı)

**t** - arşivdeki dosyaları listelemek için,

**v** - komut çıktılarını ekrana yazdırmak için,

**x** - arşiv dosyasını çıkarmak için,

**z** - arşiv yöntemi olarak gzip kullanmak için,

**p** - arşivdeki dosya ve dizin izinlerini de eklemek için,

**j** - arşiv yöntemi olarak bzip2 kullanmak için

**r**- var olan arşive yeni dosya ekler.

**`tar <parametre> <arsivinAdi.uzantisi>  <sıkıstırlacakDosyalar>`**

**`tar  -cf   dosyalar.tar   dosya1  dosya2`**

**`tar  -xf   dosyalar.tar   -C  /home/serdar/`   tüm dosyaları istenilen dizine çıkarır**

**`tar  -xf   dosyalar.tar    dosya1  -C /home/serdar/` yalnızca dosya1 i çıkarır**

**`tar  -rf   dosyalar.tar    dosya3`   var olan arşive dosya3 ü ekler**

**`tar  -tf   dosyalar.tar`      arşiv içindeki dosyaları listeler**

**Sadece belirli dosya uzantısına ait dosyaları arşivden çıkarmak istersek –wildcards kullanılabilir.**

**`tar  -xf  dosyalar.tar –wildcards   ‘\*.jpg’`**

## gzip-bzip2

**tar** komutu ile dosyalarımızı arşivledik. Şimdi ise **dosya sıkıştırma işlemlerini yapalım**

Sıkıştırma işlemi için iki temel aracımız var. Bunlar **`gzip`** ve **`bzip2`** dir.

Öncelikle birkaç normal dosyayı **sıkıştıralım**

```
gzip dosyaAdi
```

```
bzip2 dosyaAdi
```



![](img/useradd24.png)



**`gizp dosya1`** komutu ile dosya1'i `gzip` yöntemiyle sıkıştırdık.

**`bzip2 dosya2`** komutu ile dosya1'i `bzip2` yöntemiyle sıkıştırdık.

Peki sıkıştırmış olduğumuz dosyaları geri nasıl çıkartabiliriz?

Çok basit yalnızca komuta **`-d`** parametresini koymamız yeterli olacaktır. Ancak küçük bir fark var. **`bzip2`** dosyasını çıkarmak için dosyanın uzantısını yazmalıyız. Yani ==> **`bzip2 -d dosya2.bz2`** gibi.

Bu gzip için geçerli değildir. Ancak yine de önerim dosya uzantısını da eklemeniz.

Yani sıkıştırmış olduğumuz dosyaları geri çıkarmak için;

```
gzip -d dosya1.gz
```

```
bzip2 -d dosya2.bz2
```

Deneyelim;

![](img/useradd25.png)

Şimdi **ÖNEMLİ OLAN KISIMA GELDİK** **`tar`** komutu ile `gzip` ve `bzip2` sıkıştırma işlemini yapacağız. Yani;

**TAR ARŞİV DOSYASINI GZİP VEYA BZİP2 İLE SIKIŞTIRACAĞIZ** . Bunu konu başlığı olarak açıklamak isterim.

## tar Arşiv Dosyasını gzip Veya bzip2 Ile Arşivlemek

Bu işlem için İki farklı yolumuz mevcuttur.

Öncelikle basite indirgenmiş ancak dolaylı yolu göstermek isterim. 

### Dolaylı Yoldan Arşiv(tar) Dosyasını Sıkıştırmak

1- Öncelikle dosyalarımızı **tar** komutu kullanarak arşivleyelim.

```
tar -cf dosyalar.tar dosya1 dosya2 dosya3
```

![](img/useradd26.png)

Dosyalarımızı artık **`dosyalar.tar`** arşivine attık.

Şimdi bu arşiv dosyamızı `gzip` veya `bzip2` ile sıkıştırabiliriz.



2-Arşiv dosyasınız **gzip** veya **bzip2** ile sıkıştıralım ve daha sonra tekrar çıkaralım

```
gzip dosyalar.tar
```

```
gzip -d dosyalar.tar.gz
```

![](img/useradd27.png)

Bu şekilde **tar** dosyamızı sıkıştırıp daha sonra tekrar çıkarttık.

### tar Komutuyla Dosyaları Arşivleyip Sıkıştırmak

`gzip` ve `bzip2` araçlarını **tar** komutu yardımıyla arşivleme işlemi yapacağız. Ancak bu işlemi yaparken küçük farklılıklar var.

Bu fark şöyledir

`gzip` ile **tar** komutuyla arşivleme ve sıkıştırma yaparken;

```
tar -czf dosyalar.tar.gz dosyaAdi
```

`bzip2` ile **tar** komutuyla arşivleme ve sıkıştırma yaparken;

```
bzip2 -cjf dosyalar.tar.bz2 dosyaAdi
```

parametrelerini kullanmaktayız. Şimdi birlikte bu örneği **gzip** için uygulayalım.

![](img/useradd28.png)

Böylelikle **tar** komutu ile **gzip** işlemini yapmış olduk.



Şimdi de bu örneği **bzip2** için uygulayalım.

![](img/useradd29.png)

Böylelikle **tar** komutu ile **bzip2** işlemini yapmış olduk.

Eğer dosyalarımızı sıkıştırmış olduğumuz `gzip` ve `bzip2` den çıkartmak istersek, `-c` parametresi yerine `-x` parametresini kullanıyoruz.  İsterseniz çıkartma işlemi yaparken bu dosyaları aynı zamanda farklı bir dizine gönderelim. Yani;

 

```
tar -xzf dosyalar.tar.gz -C dosyalarim/
```

![](img/useradd30.png)



```
tar -xjf dosyalar.tar.bz2 -C dosyalarim/
```



![](img/useradd31.png)



Böylece **tar** komutuyla sıkıştırmış olduğumuz arşivimizin içerisinde ki dosya1 ve dosya2 yi dosyalarim/ dizini içerisine çıkarmış olduk.

# **LINUX METIN DUZENLEYICILER**

## **1-nano metin editörü**
Nano metin düzenleyicisi sistemde yüklü olmayabilir. Yüklü olup olmadığını

**`nano –version`** komutu ile öğrenebiliriz. 

Eğer nano metin düzenleyicisi yüklü değilse

Linux dağıtmı Ubuntu için : sudo apt-get install nano ile paketi kurabiliriz.

Nano ile bir dosya açmak için ;

**`nano <dosyaAdi>`** komutunu kullanmalıyız. Açılacak dosya ile aynı dizinde olmamız gerekmektedir.

Eğer dosya adı belirtmeden, yalnızca **nano** komutu kullanılırsa dosyayı yazdıktan sonra istediğimiz dosya adını verip ait olduğumuz dizinde oluşturabiliriz.
## **2-vi metin editörü**
Nanoya göre daha güçlü bir editördür ancak kullanımı daha zordur. Örneğin bir sistem çöktüğü zaman dosyaları nano ile açmak pek mümkün olmayabilir. **Kernel seviyesinde** işimize yarayacak sadece **vi** metin editörüdür. Sebebi ise **linux vi editör ile yazılmıştır**.

Vi editörü çalışma esnasında üç ayrı mod ile gelir. 

Birincisi bilgisayara komutların girdisi sırasında kullanılan vi modu,

İkincisi yazı yazarken kullanılan input modudur.

Üçüncüsü command modudur.

Komut modunda klavye üzerinde görevi olan tüm tuşlar, bilgisayar komut vermek için kullanılıyor. Yazı modunda ise diğer editörlerdekine benzer şekilde yazı yazmak mümkün olmaktadır. Klavye modu değiştirildiğinde klavye tuşlarının işlevleri de hemen değişmektedir. Vi editörünü ilk çalıştırdığınız anda komut moduna girilmektedir.

1. Menü(Menu)
1. Metin(Text) -> input modu.

İlk ekran Menü modu ile açılır. Daha sonra yazı moduna  ESC+i, a ve o ile geçilebilir.

**İ** = insert

**a** = append

**o** = open

Silme, geriye alma, aşağı satıra geçmek için tekrar yazı modundan **ESC ile Menü moduna geçilir.**

**Menü** modunda;

**a -> ile sağ tarafa bir karakter ilerler**

**o -> ile alt satıra geçilir**

**x -> ile silme işlemi yapılır**

**5+x -> ile 5 karakter soldan sağa doğru siler**

**dd -> ile  ilgili satırı siler**

**5+dd -> ile yukarıdan aşağıya 5 adet satır siler**

**u -> bir defaya mahsus geri getirir**

Menü modunda satırlar arası yön tuşları ile gezilebilir ancak kernel seviyesinde yapabilmek için; 

**Menü modunda “k” tuşu ile yukarı;**

**Menü modunda “j” tuşu ile aşağı;**

**Menü modunda “h” tuşu ile sola**

**Menü modunda “l” tuşu ile sağa**

Kelimeler de arama yapmak için;

**/ yani -> shift+7** tuşuna basmalıyız.

command kipine ise vi modundayken “:” ile girilir. İstisna olarak arama yapmak içinde “/” ile girilir.

Bir kelimeyi replace etmek için

**`:%s/EskiKelime/YeniKelime/g` NOT: BÜTÜN AYNI ISME SAHIP KELİMELERİ REPLACE ETMEKTEDİR.**

Bir metnin üst satırına yeni bir satır açıp yazı yazmak istersek;

**Shift+o** tuşunu kullanmalıyız

![](img/Aspose.Words.b6e0df8a-337a-49f3-bb0c-f932a633c435.005.png)





# LINUX KULLANICI  ISLEMLERI

## Kullanıcı Ekleme

Kullanıcı eklemenin 2 ayrı seçeneği ve komutu vardır;

- **useradd Komutu**
- **adduser Komutu**



#### 1-adduser komutu

Yeni bir kullanıcı eklemek istiyorsak **`adduser <kullaniciAdi>`**  komutunu kullanmalıyız. Bu komut ile beraber sistem yeni bir kullanıcı oluşturup, o kullanıcıya ait bir ev dizinini otomatik oluşturacaktır. Örnek olarak bir kullanıcı ekleme işlemi yapalım.

![](img/adduser1.png)

Böylece ornekkullanıcısı oluşturulmuş ve ornek grubuna dahil edildi. Yapılan işlemleri teyit etmek amaçlı, sistemde kullanıcı hesaplarının tutulduğu **`/etc/passwd`** dosyasına göz atabiliriz.

![](img/adduser2.png)

Dosya içerisinde ornek kullanıcısının eklenmiş olduğunu görmüş olduk.

**`/etc/group`** dosyasını da incelediğimizde kullanıcımızın kaydedildiği yerleri görebiliriz.

![](img/adduser4.png)

Aynı zamanda **`adduser`** komutunun kullanıcıya ait ev dizini oluşturduğunu da söylemiştik. Bunu da kontrol edecek olursak;

![](img/adduser3.png)





#### 2-useradd komutu

useradd komutu nasıl çalıştırıldığına gelmeden önce birkaç bilgi vermek isterim. Useradd komutu kullanıcı ekleme işlemleri için **`adduser`** komutuna nazaran daha düşük seviyelidir. **`useradd`** komutu ile yalnızca kullanıcıyı oluştururuz. Ev dizinine ekleme, şifre oluşturma vb. işlemleri farklı parametre ve komutlarla sağlamalıyız.



Kullanıcı oluşturma işlemi için  **`useradd <kullaniciAdi>`** komutunu yazmalıyız **ancak** bu işlemi yaparken kullanıcıya ait **home** dizini de oluşturmak istiyorsak **`-m`** parametresini kullanmamız gerekmektedir. 

```
useradd -m <kullaniciAdi>
```

Örnek olarak bir kullanıcı ekleyelim;

![](img/useradd1.png)

Böylece "ornek2" kullanıcımızı sisteme eklemiş olduk. 

Kullanıcımızı oluşturtan sonra ona ait bir şifre oluşturmak için **`passwd`** komutunu kullanmalıyız. Şimdi ornek2 kullanıcımız için bir şifre belirleyelim;

![](img/useradd2.png)

Böylece ornek2 kullanıcımızın artık bir şifresi oldu.

Grup oluşturma ve kullanıcıları görme konusu daha sonra ancak değinmişken kullanıcıyı gruba ekleme işlemi sağlayalım. 

Bir kullanıcıyı gruba eklemek için;

![](img/useradd3.png)

Şimdi kullanıcımız gruba gerçekten eklenmiş mi görelim;

**grep**  ile arama yapabilir veya direkt olarak **`/etc/group`** dosyasına girip inceleyebiliriz.

Böylece istediğimiz işlemi sağladık.



## Kullanıcı Arama Ve Listeleme

Eğer Linux kullanıcılarını listelemek istiyorsak ilk başvuracağımız yer **`/etc/passwd`** dosyası olacaktır.

Dosya içerisinden veya dosya içerisinde arama yaparak(**grep komudu**) kullanıcılarımızı görebiliriz.

Linux kullanıcısının var olup olmadığını görebilmek için;

```
id <userName>
```

komutunu kullanmalıyız. Bize çıktı olarak ya böyle bir kullanıcı olmadığını ya da kullanıcnın ait olduğu gruplara dair bilgiler verecektir.

Kullanıcının ait olduğu gruba dair vereceği bilgiden önce **grup sistemi ne olduğu**, hakkında bilgi vermek isterim.  Daha sonrasında bu işlemi grup sistemi konusu içerisinde yapalım.

## Kullanıcı Silme

Bir kullanıcıyı  **`deluser`** komutunu kullanırız.

 Ev diziniyle beraber kullanıcıyı silmek istiyorsak;

```
deluser --remove-home <kullaniciAdi>
```

komutunu kullanırız. **`man deluser`** ile aldığı parametreleri görebilirsiniz.

Kullanıcının silindiğinden emin olmak için **`/home`** dizinine `ls` ile bakarak,

**`/etc/group`** ve **`/etc/passwd`** dosyalarından sorgulayabiliriz.



## Kullanıcı Hesabını Aktif-Pasif Hale Getirmek



- #### **Kullanıcıyı Pasif Hale Getirmek**

Sistemde kayıtlı olan bir kullanıcıyı kilitleyebiliriz ve böylece kullanıcı sisteme giremeyecektir.

Bir kullanıcının hesabını kilitlemek için **`usermod`** komutunun **`-L`** parametresini kullanırız.

```
usermod -L <kullaniciAdi>
```

komutunu kullanırız.

Peki bu komutu girdiğimiz zaman sistemde nasıl bir işlem yapılır. Bildiğimiz üzere **Linux'ta her şey dosyadır.**

Sistemde kullanıcı hesaplarının parolaları **/etc/shadow** dosyası içerisindedir. Bu parolalar dosya içerisinde şifreli olarak gösterilir.

Biz **`usermod -L <kullaniciAdi>`** komutunu yazdığımız zaman sistem **`/etc/shadow`** dosyası içerisinde **kullanıcıya ait şifreli **parolasının önüne **`!`** işareti koyacaktır ve böylece **kullanıcı şifresi ile sisteme giriş yapamayacaktır.**

Sistemde **kullanici2** isimli kullanıcıyı kilitleyelim **ama öncesinde** bahsettiğimiz **shadow** dosyasına bakalım.

![](img/useradd11.png)

Gördüğümüz üzere **kullanici2** nin parolası şifreli bir şekilde görünüyor. Ancak **önünde `!` simgesi yok**. Yani şuan kullanıcımızı kilitlemedik. Şimdi kullanıcımızı kilitleyelim.

![](img/useradd12.png)

Kullanıcımızı kilitledik. Şimdi gerçekten kilitlenmiş mi diye **shadow** dosyamıza bakalım ve **!** işareti var mı kontrol edelim.

![](img/useradd13.png)

Evet yazdığımız komut sayesinde **kullanici2** yi kilitledik ve artık sisteme giriş yapamayacaktır.

- #### **Kullanıcıyı Aktif Hale Getirmek**

  Kullanıcımızın kilidini açmak ve aktif hale getirmek için **`usermod`** komutunun **`-U`** parametresini kullanırız.

  ```
  usermod -U <kullaniciAdi>
  ```

  Şimdi kilitli olan **kullanici2** adlı kullanıcımızın kilidini kaldıralım.

  ![](img/useradd14.png)

  **shadow** dosyasında ki **!** işareti kalkacaktır ve kullanıcımız artık giriş yapabilir.



## Kullanicilar Arasi Kimlik Degisimi

Sisteme yeni kullanıcı ekleme ve birden çok kullanıcının sistemde olabileceğini biliyoruz. Peki **kullanıcılar arası değişim** nasıl yapabiliriz?

Örneğin ben **serdar** kullanıcısıyla aktifim ve bir işlem yapmam gerekiyor ancak yetki alanımda değil ve **parolasını bildiğim** bir kullanıcının buna yetkisi var. Böyle bir durumda o kullanıcının kimliğine bürünerek gerekli işlemleri gerçekleştirebilir ve geri çıkabilirim.

Peki bunu nasıl yaparız. Bu işlem içi **`su`** komutunu kullanırız. Ancak bu komutun 2 farklı durumu mevcuttur.

**`su <kullaniciAdi>`** olarak işlemimizi gerçekleştirirsek, diğer kullanıcının kimliğine geçeriz.

**`su - <kullaniciAdi>`** olarak işlemimizi gerçekleştirirsek, diğer kullanıcının kimliğine geçer ve **kullanıcının KABUĞUNDA** çalışmaya başlar. 

Buradaki **detay** çok önemlidir. Bunu iyi anlayabilmek adına **normal kullanıcı** ve **root** kullanıcı arasında kimlik değişimleri yapalım.

**root**  adlı kullanıcıdan kimlik değişimi yaparak **serdar**  kullanıcısına geçelim.

![](img/useradd15.png)

**`su serdar`** komutu ile **serdar** kullanıcısına geçtik. Konsol ismine ve **/root** kısmına dikkat edelim lütfen.

**ŞİMDİ `su - serdar` YAZARAK GEÇİŞ YAPALIM**

![](img/useradd16.png)

Gördüğünüz üzere **`su serdar`** komutu kullanarak geçiş yaptığımızda konsolda **`serdar@serdar-VirtualBox:/root$`** yazıyordu.

Ancak **`su - serdar`** komutu kullanarak geçiş yaptığımızda konsolda **`serdar@serdar-VirtualBox:~$`**  yazdı.

Yani **`su -serdar`** komutunu kullandığımızda geçiş yaptığımız **hesabın kabuğunda çalışmaya başladı** ve tıpkı o hesapta oturum açmışız gibi bir tepkiyle karşılaştık.

#### 

# LINUX GRUP ISLEMLERI



## Grup Yönetimi Nedir Ve Faydaları

Linux'ta birçok kullanıcı hesabının var olduğu ve bu kullanıcılar arasında en yetkili kullanıcının **root** kullanıcısı olduğunu biliyoruz.

Ancak Linux sisteminde root kullanıcısı olmadan da root kullanıcısına dair yetkilere sahip olmamız mümkün. **Peki bunu nasıl yapıyoruz?**

Grup yönetimi sayesinde aynı grupta yer alan kullanıcılar aynı haklara sahip olmaktadırlar. Yani kullanıcıları belirli gruplara bölebilir ve gruplara da belli başlı yetkiler verebiliriz.

**Peki Linux'ta grup sisteminin faydaları nelerdir?**

Bunlardan en önemlisi kullanıcı yönetiminde oldukça fayda sağlaması. Grup üyeliği sistemi sayesinde yalnızca izin verilen dosya, dizin vs. erişim hakkı sağlamaktadır.

**Kısaca Grup sistemi bir çeşit yönetim ve kontrol mekanizmasıdır.**

Bir grup oluşturduğumuzda grubun bilgisi çokça duyduğumuz **`etc/group` dosyası içerisine eklenmekte ve kaydı tutulmaktadır.

Yani sistem üzerinde mevcut grupları görmek istersek doğal olarak **group** dosyasına bakmalıyız.

Hadi birlikte **group** dosyasına girerek hangi gruplarımızın olduğunu ve bu gruba ait hangi kullanıcıların olduğunu görelim.

![](img/useradd4.png)

Dosya içerisine girerseniz çok fazla grup olduğu ve bunların **kafa karıştırıcı geldiğini** düşünebilirsiniz ancak **sistem çok basit.**

Örnek birkaç tane grup seçelim ve bu karmaşık kelime ve harflerin **hangi mantıkla** verildiğini görelim.

![](img/useradd5.png)

Örneğin **sudo grubunu** ele alalım. 

**sudo: x :27:serdar,kullanici2**

Resimde belirtmiş olduğum numaraların açıklaması şöyledir;

**1.Grup ismi:** Gruba verilen isimdir. Yani grubumuzun ismi **sudo**

**2-Parola:** Grubun parolasıdır. Eğer grubun parolası yoksa **x** işareti ile gösterilir. Genel olarak gruplarda parola kısmı boştur ancak ayrıcalı gruplarda uygulanmaktadır.

**3-Grup Kimliği:** Gruba atanan kimlik numarasıdır.

**4-Grup Listesi:** Grupta yer alan kullanıcıları göstermektedir. "serdar" ve "kullanici2" **sudo grubunda** yer alıyor.

Ayrıca sudo grubuna kayıtlı kullanıcılar **sudo** komutunu parolası ile birlikte kullanabilmektedir.

Şimdi önceki konuda da bahsettiğimiz **`id <kullaniciAdi>`** komutu olan **kullanıcı gruplarını sorgulama** kısmına gelelim.

## Yeni Grup oluşturma

Şimdi ise yeni bir grup oluşturup, **group** dosyası içerisinde ki kaydını görelim.

Sistemde yeni bir grup oluşturmak için;

```
groupadd <grupAdi>
```

komutunu kullanırız. Şimdi yeni bir grup oluşturalım.

![](img/useradd6.png)

Grubumuzu oluşturduk. Peki grubumuz gerçekten oluşturulup **group dosyasına** kaydı yapıldı mı? Birlikte bakalım.

**group** dosyasından inceleyeceğimiz için küçük bir sorgu ile grubumuzun kaydını görebiliriz.

![](img/useradd7.png)

Evet grubumuz **group** dosyası içerisinde bulunuyor. Bir şifresi yok ve kimlik numarası 1006. İçerisinde ise herhangi bir üye yok.

Eğer gruba kendiniz bir kimlik numarası vermek isterseniz; **-g** parametresini kullanabilirsiniz;

```
groupadd -g 7890 <grupAdi>
```

gibi. Eğer aynı id ye sahip başka bir grup varsa hata verecek ve grubunuz oluşmayacaktır. Yani numarayı verirken herhangi bir tereddüt yaşamanıza gerek yok.

## Gruba Yeni Kullanıcı Ekleme

Gruba yeni bir kullanıcı eklemek için;

```
gpasswd -a <kullaniciAdi> <grupAdi> 
```

komutunu kullanabiliriz.  Şimdi yeni oluşturmuş olduğumuz gruba kullanıcımızı ekleyelim.

![](img/useradd8.png)

Grubumuza "serdar" kullanıcısını ekledik ve kontrolünü gerçekleştirdik. Artık oluşturmuş olduğumuz grubun yeni bir üyesi var :)

## Kullanıcı Gruplarını Sorgulama

Grup sistemini ve gruba yeni kullanıcı eklemeyi öğrenmiş olduk. Şimdi sistemde kayıtlı olan kullanıcıların hangi grupların üyesi olduğunu görelim.

Kullanıcının numarası ve hangi grupların aile ferdi olduğunu öğrenebilmek için;

```
id <kullaniciAdi>
```

komutunu kullanıyoruz. Şimdi "serdar" kullanıcımız hangi gruplara üyeymiş görelim.

![](img/useradd9.png)

Evet "serdar" kullanıcımız birçok gruba üye olduğunu görüyoruz. Öncelikle her grubumuzun bir **kimlik numarası** olduğunu biliyorduk. Ayrıca kullanıcıların da kendine ait bir **kimlik numarası** vardır. Bunu bir **TC kimlik numarası** gibi düşünebiliriz.

En başta gördüğümüz **`uid`** ve **`gid`** ne olduğunu açıklayalım.

**`uid`** --> **USER ID**  anlamına gelir. Yani kullanıcı numarası.

**`gid`**--> **GROUP ID** anlamına gelir. Yani grup numarası.

Mesela **`24 id li cdrom grubu`**   , **`27 id li sudo grubu`** gibi.

**"serdar"** kullanıcımızın **kullanıcı numarası(UID)=1000** miş.

**Peki kullanıcı numaraları yani UID neye göre verilmektedir??**

ID numaraları üçe ayrılır;

**Root Kullanıcısı:** ID(Kimlik numarası) **0** dır.

**Sistem Kullanıcısı:** ID(Kimlik numarası) **1-499** arası olur.

**Normal Kullanıcı:** ID(Kimlik numarası) 500-N olarak gider.

Böylece Kullanıcının **ne kullanıcısı** olduğunu anlayabiliriz.

## Kullanıcıyı Gruptan Çıkarmak

Eğer grup üyesi olan bir kullanıcıyı gruptan çıkarmak istersek **`gpasswd`** komutunun **`-d`** parametresini kullanırız.

Şimdi **serdar** kullanıcısını  eklemiş olduğumuz **yeniGrup** adlı gruptan çıkaralım.

```
sudo gspasswd -d <kullaniciAdi> <GrupAdi>
```

![](img/useradd10.png)

Böylece grubumuzdan **serdar** kullanıcısını çıkarmış olduk.





# **LINUX CONFIGURATION**
![](img/Aspose.Words.b6e0df8a-337a-49f3-bb0c-f932a633c435.006.png)

**İfconfig** komutu ile ipv4,ipv6,mac adresi öğrenilebilir.
## **1-Netplan kullanarak Static IP Yapılandırma**

Ip yapılandırma işlemi için netplan dosyasına erişmeliyiz. Bu dosya `/etc/netplan/` dizininin içerisinde bulunmaktadır.

Bu dosya Ubuntu 17.10 versiyonundan önce `etc/network/interfaces/` dizininin içerisinde bulunmaktaydı. Ancak yeni versiyonuyla beraber sistem değişikliğine gidildi.

Öncelikle ethernet cihaz adına bakalım;

![](img/Aspose.Words.b6e0df8a-337a-49f3-bb0c-f932a633c435.007.png)

Daha sonra belirtilen dosya yoluna;

**`cd /etc/netplan/`** komutu ile girebiliriz.

Kullandığınız metin editörü ile dosyayı açalım.  (nano ile açabilirsiniz)

![](img/Aspose.Words.b6e0df8a-337a-49f3-bb0c-f932a633c435.008.png)

![](img/Aspose.Words.b6e0df8a-337a-49f3-bb0c-f932a633c435.009.png)

![](img/Aspose.Words.b6e0df8a-337a-49f3-bb0c-f932a633c435.010.png)

Öncelik olarak ethernets: altına ifconfigden öğrendiğimiz cihaz adını yazıyoruz.

Static istedğimiz için **`dhcp4: no`** -> hayır olarak işaretliyoruz

**Addresses** kısmına istediğimiz ip adresini atıyoruz. **/24** olan kısım ise ağ maskemiz.  255=8bit toplam 24 bit edecektir. **255.255.255.0 olarak atama** işlemi yapacaktır.

**gateway4:** ağ geçitimizin IP adresini atıyoruz.

Son olarak **DNS için nameservers**: altına **addresses:** kısmına yazıyoruz.

Ip adreslerinin **virgül ile ayrılması** gerekmektedir. Örneğin;

[8.8.8.8(virgül)8.8.4.4]

Dosyayı kaydettikten sonra yapılandırma dosyasını test etmeliyiz. Bunun için;

**`sudo netplan try`** komutunu kullanabiliriz.

Eğer herhangi bir sorun yoksa yapılandırma dosyasının kabul edildiğine dair mesaj gelecektir. Enter tuşu ile işlemi tamamlayabiliriz.

Ardından **yapılandırmayı uygulamak** için **`sudo netplan apply`** komutunu çalıştıralım. Böylece yapmış olduğumuz ayarlar tamamlanacaktır.

Ağ hizmetini yeniden başlatmak, durdurmak veya başlatmak için;

```
sudo service network-manager restart
sudo service network-manager stop
sudo service network-manager start
```

kullanılabilir.

# 



