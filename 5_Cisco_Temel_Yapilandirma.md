# Cisco Temel Cihaz Yapılandırması (Basic Configuration)

Cisco yönlendirici (Router) veya anahtarlara (Switch) ilk bağlandığımızda cihazı güvenli hale getirmek ve isimlendirmek için kullanılan temel komutlar.

##  Cihaz Modları Arası Geçiş

* `enable` (veya `en`) : Kullanıcı modundan (User EXEC) ayrıcalıklı yönetici moduna (Privileged EXEC) geçirir. Sembol `>` iken `#` olur.
* `configure terminal` (veya `conf t`) : Cihazın ayarlarını değiştirebileceğimiz Küresel Yapılandırma moduna (Global Configuration) geçirir. Sembol `(config)#` olur.
* `exit` : Bir önceki moda geri döndürür.

## İsimlendirme ve Güvenlik (Şifreleme)

* `hostname R1` : Cihazın adını "R1" olarak değiştirir.
* `enable secret cisco` : Yönetici (enable) moduna geçerken sorulacak şifreyi "cisco" olarak ayarlar ve bunu kriptolar (kırılması zordur).

##  Konsol ve Uzak Bağlantı Şifreleri

* `line con 0` : Cihaza fiziksel olarak konsol kablosuyla bağlananlar için ayar moduna girer.
  * `password cisco` : Konsol şifresini "cisco" yapar.
  * `login` : Şifre sormayı aktif hale getirir.
* `line vty 0 4` : Cihaza uzaktan (Telnet/SSH ile) bağlanacak 5 kişi (0'dan 4'e kadar) için ayar moduna girer.
  * `password cisco` : Uzak bağlantı şifresini belirler.
  * `login` : Şifre sormayı aktif eder.

##  Karşılama Mesajı ve Kaydetme

* `banner motd # Yetkisiz Giris Yasaktir! #` : Cihaza bağlanan herkesin karşısına çıkacak yasal uyarı mesajını ayarlar.
* `write memory` (veya `wr`) : Yapılan tüm ayarları kalıcı hafızaya (NVRAM) kaydeder. Elektrik gitse bile ayarlar silinmez. (Alternatif: `copy running-config startup-config`)
