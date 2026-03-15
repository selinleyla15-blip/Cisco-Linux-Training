# 🔎Linux Arama ve Metin İşleme (Filtreleme) Komutları

Siber güvenlikte veya sunucu yönetiminde, devasa log (kayıt) dosyalarının içinde sadece aradığımız kelimeyi veya hatayı bulmak için bu komutları kullanırız.

## Dosya ve Dizin Arama

* `find / -name "gizli_dosya.txt"` : Tüm sistemde (`/` kök dizininden itibaren) adı "gizli_dosya.txt" olan dosyayı arar.
* `find . -type d -name "test"` : Sadece bulunduğum dizinde (`.`) "test" adındaki klasörleri (`-type d`) arar.

##  Metin İçinde Arama ve Filtreleme

* `grep "hata" log_dosyasi.txt` : log_dosyasi.txt içindeki "hata" kelimesinin geçtiği tüm satırları ekrana basar.
* `grep -i "admin" users.txt` : Büyük/küçük harf duyarlılığını kapatarak (`-i`) "Admin", "ADMIN", "admin" kelimelerini arar.

## Dosya İçeriği İnceleme

* `head -n 10 <dosya>` : Dosyanın sadece ilk 10 satırını gösterir.
* `tail -n 10 <dosya>` : Dosyanın sadece son 10 satırını gösterir (Genellikle en son düşen logları görmek için kullanılır).
* `tail -f <dosya>` : Dosyaya yeni bir şeyler yazıldıkça canlı (real-time) olarak ekranda gösterir.
