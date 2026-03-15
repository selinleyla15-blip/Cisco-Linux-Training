#  Cisco Arayüz (Interface) ve IP Yapılandırması

Bir Router'ın ağlara bağlanabilmesi için üzerindeki portlara (arayüzlere) IP adresi atanması ve bu portların aktif edilmesi gerekir.

##  Porta İp Adresi Verme

* `interface gigabitEthernet 0/0` (veya `int g0/0`) : İşlem yapmak istediğimiz fiziksel portun (arayüzün) içine girer.
* `ip address 192.168.1.1 255.255.255.0` : Girdiğimiz bu porta IP adresini ve Alt Ağ Maskesini (Subnet Mask) tanımlar.
* `no shutdown` (veya `no shut`) : Cisco portları güvenlik gereği varsayılan olarak kapalıdır. Bu komut portu açar (kırmızı ışığı yeşile çevirir).

##  Durum Kontrolü (Hata Ayıklama)

* `show ip interface brief` (veya `sh ip int br`) : Cihaz üzerindeki tüm portların bir özetini listeler. Hangi portta hangi IP var ve port açık mı (Status: up) kapalı mı (Status: down) tek ekranda görmemizi sağlar. Çok kritik bir komuttur!
