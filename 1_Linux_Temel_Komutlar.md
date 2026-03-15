# 🐧 Linux Temel Komutlar Rehberi (Survival Guide)

Bu belge, siber güvenlik ve sistem yönetimi için en çok kullanılan temel Linux terminal komutlarını içermektedir.

## 📂 Dosya ve Dizin İşlemleri (Navigasyon)

* `pwd` : (Print Working Directory) Şu an hangi klasörde (dizinde) olduğumu gösterir.
* `ls` : (List) Bulunduğum klasördeki dosyaları ve klasörleri listeler.
    * `ls -l` : Dosyaları detaylı (izinler, boyut, tarih) listeler.
    * `ls -a` : Gizli dosyaları da gösterir.
* `cd <klasor_adi>` : (Change Directory) İstenilen klasörün içine girer.
    * `cd ..` : Bir üst klasöre (geriye) çıkar.
    * `cd ~` : Kullanıcının ana (home) dizinine döner.

## 📝 Dosya Oluşturma ve Silme

* `mkdir <klasor_adi>` : (Make Directory) Yeni bir klasör oluşturur.
* `touch <dosya_adi.txt>` : İçi boş yeni bir dosya oluşturur.
* `rm <dosya_adi>` : (Remove) Dosyayı siler.
* `rm -r <klasor_adi>` : Klasörü ve içindeki her şeyi siler (DİKKAT! Geri dönüşü yoktur).

## 🚚 Kopyalama ve Taşıma

* `cp <kaynak_dosya> <hedef_yer>` : (Copy) Dosyayı kopyalar.
* `mv <eski_ad> <yeni_ad>` : (Move) Dosyanın adını değiştirir veya başka bir yere taşır.

## 👁️ Dosya İçeriği Okuma

* `cat <dosya_adi>` : Dosyanın içindeki tüm metni terminale yazdırır.
* `less <dosya_adi>` : Uzun dosyaları sayfa sayfa okumayı sağlar (Çıkmak için 'q' tuşuna basılır).
* `clear` : Ekrandaki kalabalık yazıları temizler (Terminali ferahlatır).
