# Etraftaki Ağları Görmek
Burada anlatacağım saldırı modeli için öncelikle Kali Linux’umuza uyumlu bir WiFi kartına sahip olmamız gerekiyor. 
Bazı popüler Kali uyumlu WiFi kartları:
-	Ralink RT5370
-	TP-LINK TL-WN722N
-	Asus N14
-	Magbox Usb Stick
Öncelikle bu saldırıyı yapmadan önce şunu biliyor olmalıyız ki networkümüzün managed mod ve monitör mod adlı 2 farklı modu vardır. WiFi kartımız ile etrafımızdaki ağları görebilmek için bunu monitör moda çevirmemiz gerekir. Monitor modda iken internete bağlanamaz fakat etraftaki ağlar hakkında bilgi edinebiliriz. Terminal üzerinden monitör moda geçmek için, ağımızın ismini wlan0 kabul edersek:

**_airmon-ng start wlan0_**
monitor moda geçirir.

**_airmon-ng stop wlan0_**
modu managed moda geçirir.

Monitör moda geçtikten sonra etrafımızdaki ağları görmek için:
**_airodump-ng wlan0mon _**

Etraftaki tüm kablosuz ağları bulur ve onlar hakkında bilgiler verir. bu bilerin başında BSSID bize onların MAC adresini listeler.Bunun yanındaki PwR kısmı bize ne kadar yakınsa o kadar yüksek gözükür.
ESSID ise wifi'ın adıdır. CH kanalı gösterir. ENC şifreleme işlemi bilgisidir. 

**_airodump-ng --channel x --bssid x --write airodumptest wlan0mon_**
bunu yaptığımızda seçtiğimiz ağ hakkında bilgiler elde ederiz. bu bilgilerden:
en üst tarafta sadece 1 bssid gösteriliyor. 
Station bu modeme bağlı olan cihazların MAC adresi gösterilir. 
--write dediğimiz yere elde edilen sonuçlar yazılır. 

wireshark programı ile etraftaki ağların hareketlerinin analizini yapabiliriz.
wireshark içinde File-Open'dan kaydettiğimiz cap dosyasını açabiliriz.
