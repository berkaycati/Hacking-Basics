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
cd

Bulunduğumuz dosya konumundan bir önceki konuma dönmek için kullanacağımız komut:
cd ..


Girdiğimiz klasörün içerisindeki dosya-klasörleri görüntülemek için:
ls

Klasörün aynı zamanda özelliklerini görüntülemek için:
ls -la
Bu komutu kullandığımız zaman dosya isminin yanında gözüken -r(readable)-w(writable) anlamına gelir. Bu klasöre mevcut yetkilerimiz ile yazabilir veya okuyabilir olduğumuzu belirtir. 
Örneğin:

![p2](https://github.com/barbaroskp/Kali_Linux_Commands/blob/main/images/p1.png)

Bu çıktıda, "dosya.txt" dosyası "rw-" karakterleri ile başlıyor. Bu, dosyanın sahibinin (kullanıcı) hem okuma hem de yazma izni olduğunu, ancak diğer kullanıcıların sadece okuma iznine sahip olduğunu gösterir. Bu nedenle, sahibi dosyayı hem okuyabilir hem de değiştirebilirken, diğer kullanıcılar sadece dosyayı okuyabilirler. Buradaki kullanıcı yazan kısım root veya diğer bir kullanıcıyı ifade eder. 

Bulunduğumuz konum klasördeki gizli dosyaları görmek için:
ls –a 

İçinde bulunduğumuz konuma yeni bir klasör oluşturmak için:
mkdir  klasör ismi

İçinde bulunduğumuz konumdaki bir dosyayı silmek için:
rm -r dizin adı 
Örneğin masaüstündeki test isimli bir klasörü silmek için:
rm -r /root/Desktop/test


Dosya dolu da olsa boş da olsa zorla silmek için:
rm -rf
bu komut kullanıldığında geri dönüşüm kutusunda veya başka bir yerde tekrar kurtarulamaz. Dikkatli kullanmak gerekir. 


Bulunduğumuz dizini(pathwayi) öğrenmek için:
pwd
 
![p3](https://github.com/barbaroskp/Kali_Linux_Commands/blob/main/images/p3.jpeg)

Kullandığımız işletim sistemi ve versiyonu gibi işletim sistemi bilgilerini öğrenmek için:
uname -a
Örneğin:
 
![p4](https://github.com/barbaroskp/Kali_Linux_Commands/blob/main/images/p2.jpg)

Bulunduğumuz konumdaki bir dosyanın içeriğini terminale yazdırmak ve okumak için:
cat dosya ismi
Örneğin:
 
![p5](https://github.com/barbaroskp/Kali_Linux_Commands/blob/main/images/p4.jpeg)

Bulunduğumuz konumdaki bir dosyanın içeriğini satır numaraları ile birlikte terminale yazdırmak ve okumak için:
cat -n
 
Bulunduğumuz konumdaki bir dosyanın içeriğini satır sonlarını işaretleyerek okumamızı kolaylaştırarak terminale yazdırmak ve okumak için:
'==cat -E=='

Bulunduğumuz dosyadaki bir kelimeyi filtrelemek ve içerisinde geçen yerleri ekrana getirmek için:
 cat dosyaadi | grep aranacakkelime
Örneğin:
 
![p6](https://github.com/barbaroskp/Kali_Linux_Commands/blob/main/images/p5.jpeg)

Bulunduğumuz konumdaki bir dosyayı kopyalamak için
cp
Bulunduğumuz konumdaki bir dosyanın içerisindeki alt dizinle birlikte kopyalamak için:
cp -R
içi boş bir dosyayı kopyalamak için:
cp -r

Bir dosyayı taşımak için:
mv kopyalanacak_dosya  kopyalanacağı_yer


Bir dosyanın içerisindeki ilk 10 satırı terminale yazdırmak için:
head yazdırılacak dosya

Bir dosyanın içerisindeki son 10 satırı terminale yazdırmak için:
tail yazdırılacak dosya


Bulunduğumuz konumda yeni bir text dosyası açmak için:
nano açılacak_dosyanın_ismi
dosya içine yazılacak text
Ctrl O
Enter
Ctrl X

Terminal penceresine sığmayan metinleri daha rahat okuyabilmek için:
more

Dosya içeriğini alfabetik olarak sıralamak için:
sort dosyaadi.txt

Dosya içeriğini ters sırada alfabetik olarak sıralamak için:
sort -r dosyaadi.txt

Dosya içeriğini sayısal olarak sıralamak için:
sort -n dosyaadi.txt

Dosya içeriğini satır uzunluğuna göre sıralamak için:
sort -k 2 dosyaadi.txt

Kullandığımız network, IP adresimiz, MAC adresimiz gibi bilgileri öğrenmek için:
İfconfig

Sadece wireless yani kablosuz ağımız hakkında bilgi almak istersek:
iwconfig
sadece wireless ağımız hakkında fakat daha detaylı bilgi verir. 

Herhangi bir IP adresine veya siteye ping gönderip networke bağlı olup olmadığını test etmek için:
ping siteismi.com
veya
ping IP adresi
