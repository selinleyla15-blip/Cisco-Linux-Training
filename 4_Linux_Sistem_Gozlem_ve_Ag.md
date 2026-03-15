# Linux Sistem Gözlem ve Ağ (Network) Komutları

Bilgisayarın ne kadar yorulduğunu, arkada hangi programların çalıştığını ve internet/ağ durumunu kontrol etmek için hayati komutlar.

##  Sistem ve Süreç (Process) Yönetimi

* `top` : Windows'taki "Görev Yöneticisi" gibi çalışır. RAM ve İşlemciyi en çok kullanan programları canlı olarak listeler (Çıkmak için 'q' tuşuna basılır).
* `ps aux` : Arka planda çalışan tüm süreçleri (uygulamaları) detaylıca listeler.
* `kill <PID>` : `top` veya `ps` komutuyla PID (Process ID - İşlem Numarası) değerini öğrendiğimiz, donan veya sorun çıkaran bir uygulamayı zorla kapatır.
* `df -h` : (Disk Free) Hard diskte ne kadar boş alan kaldığını okunabilir (`-h` : human readable) formatta MB/GB cinsinden gösterir.
* `free -m` : Sistemdeki RAM kullanımını (boş/dolu) Megabayt cinsinden gösterir.

## Temel Ağ (Network) Komutları

* `ifconfig` veya `ip a` : Bilgisayarın IP adresini, MAC adresini ve ağ kartlarını gösterir (Siber güvenlikte en çok kullanılan komuttur).
* `ping <ip_adresi_veya_site>` : Karşıdaki bilgisayarın veya sitenin ayakta olup olmadığını ve bağlantı hızını kontrol eder.
