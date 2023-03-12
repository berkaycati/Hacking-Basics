

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


![Denemefoto](https://camo.githubusercontent.com/barbaroskp/Kali_Linux_Commands/main/images/p2.jpeg)

Bu parametreler genelde kullanılan fonksiyonun uzun ismi için çift tire “—“ baş harfi için tek tire “-“ şeklinde kullanılır ve help de bunlardan birisidir. Örneğin macchanger toolu için:
 
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
