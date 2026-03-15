# 🛡️ Linux Kullanıcı ve Yetki Yönetimi

Linux sistemlerde güvenlik her şeydir. Her dosyanın bir sahibi ve belirli izinleri vardır. Bu belgede kullanıcıları ve dosya izinlerini nasıl yöneteceğimizi inceliyoruz.

## 👤 Kullanıcı İşlemleri

* `su <kullanici_adi>` : (Substitute User) Başka bir kullanıcının hesabına geçiş yapar.
* `sudo <komut>` : (Superuser Do) Komutu "Root" (en yetkili yönetici) haklarıyla geçici olarak çalıştırır.
* `whoami` : Şu an terminalde hangi kullanıcı adıyla işlem yaptığımı gösterir.
* `passwd` : Mevcut kullanıcının şifresini değiştirir.

## 🔑 Dosya ve Dizin İzinleri (Permissions)

Linux'ta izinler 3 gruba ayrılır: **U**ser (Sahip), **G**roup (Grup), **O**thers (Diğerleri).
İzin tipleri: **r** (read/okuma), **w** (write/yazma), **x** (execute/çalıştırma).

* `chmod +x <dosya_adi>` : Dosyaya çalıştırma (execute) yetkisi verir (Özellikle script dosyaları için çok önemlidir).
* `chmod 777 <dosya_adi>` : Dosyaya herkesin okuma, yazma ve çalıştırma yetkisi vermesini sağlar (Güvenlik açısından tehlikelidir, sadece test için kullanılır).
* `chmod 755 <dosya_adi>` : Sahibine tam yetki, diğerlerine sadece okuma ve çalıştırma yetkisi verir.
* `chown <kullanici>:<grup> <dosya_adi>` : (Change Owner) Dosyanın sahibini ve grubunu değiştirir.
