# Cisco Router Üzerinde DHCP Sunucu Kurulumu

DHCP (Dynamic Host Configuration Protocol), ağa bağlanan cihazlara otomatik olarak IP adresi, Alt Ağ Maskesi ve Varsayılan Ağ Geçidi (Default Gateway) dağıtan sistemdir.

## DHCP Havuzu Oluşturma Adımları

* `ip dhcp pool MY_POOL` : Dağıtılacak IP'ler için "MY_POOL" adında bir havuz oluşturur ve DHCP yapılandırma moduna girer.
* `network 192.168.1.0 255.255.255.0` : Havuzun hangi ağdaki IP adreslerini dağıtacağını belirler (Bu örnekte 192.168.1.1'den 192.168.1.254'e kadar dağıtabilir).
* `default-router 192.168.1.1` : Ağa bağlanan bilgisayarlara internete (veya başka ağlara) çıkış kapısı olarak Router'ın kendi IP adresini gösterir.
* `dns-server 8.8.8.8` : (Opsiyonel) Bilgisayarlara isim çözünürlüğü yapabilmeleri için bir DNS sunucusu adresi verir.
