# Kali Linux
Siber güvenlik alanında kendimizi geliştirmek için kullanmamız gereken ve minimum temel seviyede bilmemiz gereken işletim sistemi Kali Linux’tur. Kali Linux’un diğer işletim sistemlerinden siber güvenlik alanı için en büyük olumlu farkı açık kaynak kodlu olması ve hemen hemen her şeyi terminal ekranından yapmamıza olanak sağlamasıdır. Ayrıca içerisinde hazır olarak onlarca siber güvenlik tool’ları bulunmaktadır. 
Kali Linux, Debian tabanlı bir işletim sistemi olup, özellikle güvenlik testleri için tasarlanmış bir dağıtımdır.
Debian, kullanıcılarına özgür yazılımın tüm avantajlarını sunar. İşletim sistemi, açık kaynak kodlu olduğu için isteyen herkes tarafından görüntülenebilir, düzenlenebilir ve dağıtılabilir. Debian, hem masaüstü hem de sunucu kullanımı için uygundur ve çoklu mimari desteği sunar.
Öncelikle bu işletim sisteminin terminalinde surf yapabilmek için bilmemiz gereken temel komutları öğrenelim.


# Temel Kali Linux Komutları
Kali Linux’ta gördüğümüz ifadelerin anlamları:
“$” : kullanıcı olduğunuzu belirtir.
“#”: root admin olduğununuzu belirtir.
 “~”: kullanıcının home dizinininde olduğunu belirtir.

Kali Linux’ta herhangi bir tool’un veya programın hakkında bilgi almak için:
tool ismi –help
veya 
tool ismi -h 
komutlarını kullanabilirsiniz. 


Bu parametreler genelde kullanılan fonksiyonun uzun ismi için çift tire “—“ baş harfi için tek tire “-“ şeklinde kullanılır ve help de bunlardan birisidir. Örneğin macchanger toolu için:
 
![p1](https://github.com/barbaroskp/Kali_Linux_Commands/blob/main/images/Resim1.jpg)
 
burada da gördüğünüz gibi örneğin toolun versiyonu için macchanger –version veya kısaltması olarak macchanger -v komutları eşdeğerdir. 
Bu kullanım hemen hemen her tool ve program için aynı şekilde yazılır. 

Kali linux’u her çalıştırdığımızda klavyeyi Türkçe yapmak için kullanmamız gereken komut:
setxkbmap tr 

Kali makinamızı çalıştırdığımızda kali.org sitesinden indirilmesi gereken ve güncellenmesi gereken bir şeyler olup olmadığını kontrol etmek için makinamızı ilk çalıştırdığımızda her zaman:
apt get upgrade
apt get update
çalıştırmak önemlidir. 

Bulunduğumuz konum altındaki herhangi bir dosyayı açmak, içine girmek için kullanacağımız komut:

**_cd_**

Bulunduğumuz dosya konumundan bir önceki konuma dönmek için kullanacağımız komut:

**_cd .._**


Girdiğimiz klasörün içerisindeki dosya-klasörleri görüntülemek için:

**_ls_**

Klasörün aynı zamanda özelliklerini görüntülemek için:

**_ls -la_**

Bu komutu kullandığımız zaman dosya isminin yanında gözüken -r(readable)-w(writable) anlamına gelir. Bu klasöre mevcut yetkilerimiz ile yazabilir veya okuyabilir olduğumuzu belirtir. 
Örneğin:

![p2](https://github.com/barbaroskp/Kali_Linux_Commands/blob/main/images/p1.png)

Bu çıktıda, "dosya.txt" dosyası "rw-" karakterleri ile başlıyor. Bu, dosyanın sahibinin (kullanıcı) hem okuma hem de yazma izni olduğunu, ancak diğer kullanıcıların sadece okuma iznine sahip olduğunu gösterir. Bu nedenle, sahibi dosyayı hem okuyabilir hem de değiştirebilirken, diğer kullanıcılar sadece dosyayı okuyabilirler. Buradaki kullanıcı yazan kısım root veya diğer bir kullanıcıyı ifade eder. 

Bulunduğumuz konum klasördeki gizli dosyaları görmek için:

**_ls –a _**

İçinde bulunduğumuz konuma yeni bir klasör oluşturmak için:

**_mkdir_**  klasör ismi

İçinde bulunduğumuz konumdaki bir dosyayı silmek için:

**_rm -r_** dizin adı 

Örneğin masaüstündeki test isimli bir klasörü silmek için:

**_rm -r_** /root/Desktop/test


Dosya dolu da olsa boş da olsa zorla silmek için:

**_rm -rf_**

bu komut kullanıldığında geri dönüşüm kutusunda veya başka bir yerde tekrar kurtarulamaz. Dikkatli kullanmak gerekir. 


Bulunduğumuz dizini(pathwayi) öğrenmek için:

**_pwd_**
 
![p3](https://github.com/barbaroskp/Kali_Linux_Commands/blob/main/images/p3.jpeg)

Kullandığımız işletim sistemi ve versiyonu gibi işletim sistemi bilgilerini öğrenmek için:

**_uname -a_**

Örneğin:
 
![p4](https://github.com/barbaroskp/Kali_Linux_Commands/blob/main/images/p2.jpg)

Bulunduğumuz konumdaki bir dosyanın içeriğini terminale yazdırmak ve okumak için:

**_cat_** dosya ismi

Örneğin:
 
![p5](https://github.com/barbaroskp/Kali_Linux_Commands/blob/main/images/p4.jpeg)

Bulunduğumuz konumdaki bir dosyanın içeriğini satır numaraları ile birlikte terminale yazdırmak ve okumak için:

**_cat -n_**
 
Bulunduğumuz konumdaki bir dosyanın içeriğini satır sonlarını işaretleyerek okumamızı kolaylaştırarak terminale yazdırmak ve okumak için:

**_cat -E_**

Bulunduğumuz dosyadaki bir kelimeyi filtrelemek ve içerisinde geçen yerleri ekrana getirmek için:

**_cat_** dosyaadi | grep aranacakkelime

Örneğin:
 
![p6](https://github.com/barbaroskp/Kali_Linux_Commands/blob/main/images/p5.jpeg)

Bulunduğumuz konumdaki bir dosyayı kopyalamak için

**_cp_**

Bulunduğumuz konumdaki bir dosyanın içerisindeki alt dizinle birlikte kopyalamak için:

**_cp -R_**

içi boş bir dosyayı kopyalamak için:

**_cp -r_**

Bir dosyayı taşımak için:

**_mv_** kopyalanacak_dosya  kopyalanacağı_yer



Bir dosyanın içerisindeki ilk 10 satırı terminale yazdırmak için:

**_head_** yazdırılacak dosya


Bir dosyanın içerisindeki son 10 satırı terminale yazdırmak için:

**_tail_** yazdırılacak dosya


Bulunduğumuz konumda yeni bir text dosyası açmak için:
nano açılacak_dosyanın_ismi
dosya içine yazılacak text

**_Ctrl O_**
**_Enter_**
**_Ctrl X_**

Terminal penceresine sığmayan metinleri daha rahat okuyabilmek için:

**_more_**

Dosya içeriğini alfabetik olarak sıralamak için:

**_sort_** dosyaadi.txt

Dosya içeriğini ters sırada alfabetik olarak sıralamak için:

**_sort -r_** dosyaadi.txt

Dosya içeriğini sayısal olarak sıralamak için:

**_sort -n_** dosyaadi.txt

Dosya içeriğini satır uzunluğuna göre sıralamak için:

**_sort -k_** 2 dosyaadi.txt

Kullandığımız network, IP adresimiz, MAC adresimiz gibi bilgileri öğrenmek için:

**_İfconfig_**

Sadece wireless yani kablosuz ağımız hakkında bilgi almak istersek:

**_iwconfig_**

sadece wireless ağımız hakkında fakat daha detaylı bilgi verir. 

Herhangi bir IP adresine veya siteye ping gönderip networke bağlı olup olmadığını test etmek için:

**_ping_** siteismi.com
veya
**_ping_** IP adresi
