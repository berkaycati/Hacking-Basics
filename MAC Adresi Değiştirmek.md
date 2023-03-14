# MAC(Media Access Control address) Adresi Değiştirmek

MAC adresi, bir ağ arabirim kartının benzersiz tanımlayıcısıdır ve cihazların birbirleriyle iletişim kurabilmesi için kullanılır. Bu adresler genellikle cihazların üretildiği sırada ve üretici tarafından atanır ve kalıcıdır. MAC adresleri, ağdaki cihazların kimlik doğrulaması ve yetkilendirilmesi için kullanılabileceği gibi, ağ trafiği izleme, hata ayıklama ve diğer amaçlar için de kullanılabilir. Ancak, MAC adresleri sadece yerel ağda kullanılır.
Kali Linux’ta MAC adresi değiştirmek:
1.	Terminali açın ve "**_ifconfig_**" komutunu girin. Bu komut, mevcut ağ bağlantılarınızı ve MAC adreslerinizi gösterir.

2.	Değiştirmek istediğiniz ağ bağlantısının adını (genellikle "eth0" veya "wlan0") not edin.

3.	MAC adresinizi değiştirmek için "**_ifconfig [ağ bağlantısı adı] hw ether [yeni MAC adresi]_**" komutunu kullanın. Örneğin, "**_ifconfig wlan0 hw ether 00:11:22:33:44:55_**" komutuyla yeni bir MAC adresi oluşturabilirsiniz. Yeni MAC adresinizi istediğiniz şekilde belirleyebilirsiniz.


4.	"**_ifconfig [ağ bağlantısı adı]_**" komutuyla MAC adresinizin değiştiğini kontrol edin.

5.	Değişikliği kalıcı hale getirmek istiyorsanız, "**_nano /etc/network/interfaces_**" komutunu kullanarak ağ bağlantınızın ayar dosyasını açın ve "**_hwaddress ether [yeni MAC adresi]_**" satırını ekleyin. Son olarak, kaydedin ve çıkın.

Bu adımlar dışında kali linuxta yüklü olan macchanger toolunu da kullanabilirsiniz. İlgili tool’un kullanımı için macchanger **_–help komutu ile help dokümanını açabilir ve kullanımını inceleyebilirsiniz. 
Eğer kali makinanızda macchanger yüklü değil ise **_apt install macchanger_** komutu ile indirebilirsiniz. 
