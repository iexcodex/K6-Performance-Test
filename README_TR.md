# 🛡️ K6 Web Penetrasyon Test Aracı

**Profesyonel Web Güvenlik Tarama Sistemi - Türkçe İnteraktif Menü**

---

## 📋 Hakkında

K6, web uygulamalarının güvenliğini test etmek için tasarlanmış kapsamlı bir penetrasyon testi aracıdır. Etik hacking ve güvenlik araştırması için geliştirilmiştir.

**Versiyon:** 2.0  
**Dil:** Python 3  
**Lisans:** Eğitim & Etik Hacking Amaçlı

---

## ⚠️ ÖNEMLİ UYARILAR

### ⚖️ YASAL SORUMLULUK

Bu araç **sadece yasal ve yetkili güvenlik testleri** için kullanılmalıdır.

**Türkiye'de Yasalar (TCK 5237):**
- Madde 243: Bilişim sistemine girme → 1-3 yıl hapis
- Madde 244: Sistemi engelleme/bozma → 1-5 yıl hapis
- Madde 245: Verileri yok etme/değiştirme → 6 ay-3 yıl hapis

**Uluslararası Yasalar:**
- ABD (CFAA): 250,000$ para cezası + 10 yıl hapis
- AB (GDPR): 20 milyon € veya yıllık gelirin %4'ü

### ✅ YASAL KULLANIM

```
✅ Kendi web siteniz
✅ Şirketinizin sistemi (yazılı izinle)
✅ Test ortamları (DVWA, bWAPP, WebGoat)
✅ Bug bounty programları
✅ Eğitim amaçlı (izin aldığınız sistemlerde)

❌ Başkasının sitesi
❌ İzinsiz sistemler
❌ Ticari siteler
❌ Devlet siteleri
❌ Eğitim kurumları (izinsiz)
```

---

## 🚀 KURULUM

### Gereksinimler
- Python 3.7+
- pip (Python paket yöneticisi)

### Adım 1: Gerekli Paketleri Yükle

```bash
pip install requests urllib3
```

### Adım 2: Script'i İndir

```bash
git clone https://github.com/[username]/k6-pentest.git
cd k6-pentest
```

### Adım 3: Çalıştır

```bash
python3 k6_pentest_tr.py
```

---

## 📊 ÖZELLİKLER

### 11 Farklı Tarama Modülü

| # | Modül | Açıklama |
|---|-------|----------|
| 1 | 🎯 Hedef URL Belirleme | Hedef sistemi tanımla |
| 2 | 🔍 Keşif & Bilgi Toplama | Sunucu, CMS, teknoloji tespiti |
| 3 | 💉 SQL Injection | 50+ payload ile SQL zafiyet testi |
| 4 | 🎭 XSS Taraması | 75+ payload ile XSS testi |
| 5 | 📁 LFI/RFI Taraması | Dosya okuma zafiyet testi |
| 6 | 🗂️ Dizin Keşfi | 200+ yol ile bruteforce |
| 7 | 🔐 SSL/TLS Analizi | Sertifika ve şifreleme kontrolü |
| 8 | 🌐 Port Tarama | 30+ yaygın port taraması |
| 9 | 📋 HTTP Header Analizi | Güvenlik başlıkları kontrolü |
| 10 | 🔓 Kimlik Doğrulama Testi | Zayıf şifre testi |
| 11 | 🚀 Komut Enjeksiyonu | Komut çalıştırma zafiyet testi |

### Raporlama

- 📊 **Kapsamlı Rapor Oluştur** - Detaylı güvenlik raporu
- ⚡ **Tam Tarama** - Tüm modülleri sırayla çalıştır
- 📁 **Otomatik Dosya Kaydetme** - `k6_rapor_YYYYMMDD_HHMMSS.txt`

---

## 💻 KULLANIM KILAVUZU

### Temel Kullanım

```bash
python3 k6_pentest_tr.py
```

### Menü Seçenekleri

```
[1]  🎯 Hedef URL Belirle
[2]  🔍 Keşif ve Bilgi Toplama
[3]  💉 SQL Injection Taraması
[4]  🎭 XSS Taraması
[5]  📁 LFI/RFI Taraması
[6]  🗂️ Dizin Keşfi
[7]  🔐 SSL/TLS Analizi
[8]  🌐 Port Tarama
[9]  📋 HTTP Header Analizi
[10] 🔓 Kimlik Doğrulama Testi
[11] 🚀 Komut Enjeksiyonu
[12] 📊 Kapsamlı Rapor Oluştur
[13] ⚡ TÜM TARAMALARI ÇALIŞTIR
[14] ⚙️ Ayarlar
[0]  ❌ Çıkış
```

### Örnek Senaryo

```bash
# 1. Script'i başlat
python3 k6_pentest_tr.py

# 2. Hedef URL'yi gir
Seçim: 1
URL: http://localhost:8000

# 3. Keşif yap
Seçim: 2

# 4. SQL Injection testa
Seçim: 3

# 5. XSS testa
Seçim: 4

# 6. Rapor oluştur
Seçim: 12

# 7. Rapor dosyası oluşturulur
k6_rapor_20260311_143022.txt
```

---

## 🧪 TEST ORTAMLARI

Güvenli test için önerilen platformlar:

### Lokal Test
```bash
# Python HTTP sunucusu
python3 -m http.server 8000

# Node.js
npm start

# PHP
php -S localhost:8000
```

### Online Platformlar
- **DVWA** - http://www.dvwa.co.uk/
- **bWAPP** - http://www.itsecgames.com/
- **WebGoat** - https://owasp.org/www-project-webgoat/
- **HackTheBox** - https://www.hackthebox.eu/
- **TryHackMe** - https://tryhackme.com/

---

## 📈 SONUÇLAR NASIL OKUNUR?

### İstek İstatistikleri
```
Toplam İstek: 5000
Başarılı: 4950
Başarısız: 50
Başarı Oranı: 99.00%

✅ İyi: %95+ başarı
⚠️ Orta: %80-95% başarı
❌ Kötü: %80 altı başarı
```

### Zafiyet Bulguları
```
[!] ZAFİYET BULUNDU!
URL: http://example.com/page?id=1
Parametre: id
Payload: ' OR '1'='1
Tip: SQL Injection (Hata Tabanlı)
```

### Rapor Dosyası
```
k6_rapor_20260311_143022.txt

İçeriği:
- Özet (Toplam/Kritik Zafiyet)
- Keşif Sonuçları
- Tüm Tarama Sonuçları
- Öneriler
- Sorumluluk Reddi
```

---

## 🔧 AYARLAR

### Timeout Değiştirme
```
Seçim: 14 (Ayarlar)
1 - Timeout Değiştir
Yeni timeout: 15 (saniye)
```

### Thread Sayısı Değiştirme
```
Seçim: 14 (Ayarlar)
2 - Thread Sayısı Değiştir
Yeni thread sayısı: 20
```

### User-Agent Değiştirme
```
Seçim: 14 (Ayarlar)
3 - User-Agent Değiştir
Yeni User-Agent: Custom-Agent/1.0
```

---

## 🎯 BEST PRACTICES

### 1. İzin Alın
```
✅ Yazılı izin belgesi
✅ Test kapsamı belirleme
✅ Yasal sözleşme
```

### 2. Sorumlu Açıklama
```
Zafiyet buldunuz mu?

1. Hemen şirkete bildirin
2. Detayları GİZLİ tutun
3. Düzeltme için süre tanıyın (90 gün)
4. Sonra kamuya açıklayın
```

### 3. Zarar Vermeyin
```
❌ Veritabanını silmeyin
❌ Kullanıcı verilerini çalmayın
❌ Sistemi çökertmeyin
❌ DDoS yapmayın
```

### 4. Düzenli Test
```
✅ Deployment öncesi
✅ Güvenlik güncellemesi sonrası
✅ Yeni özellik eklendikten sonra
✅ Yoğun sezon öncesi
```

---

## 📚 ÖĞRENME KAYNAKLARI

### Türkçe Kaynaklar
- BTK Akademi - Siber Güvenlik
- Udemy - Etik Hacking Kursları
- YouTube - Siber Güvenlik Kanalları

### İngilizce Kaynaklar
- PortSwigger Web Security Academy
- OWASP Testing Guide
- PentesterLab
- Cybrary

### Kitaplar
- "The Web Application Hacker's Handbook"
- "Web Security Testing Cookbook"
- "Penetration Testing"

---

## 🐛 SORUN GİDERME

### Problem: "Bağlantı Hatası"
```
Çözüm:
1. Hedef URL'yi kontrol edin
2. İnternet bağlantısını kontrol edin
3. Firewall ayarlarını kontrol edin
4. Hedef sunucunun çalışıp çalışmadığını kontrol edin
```

### Problem: "Timeout"
```
Çözüm:
1. Timeout değerini artırın (Ayarlar → 1)
2. Ağ bağlantısını kontrol edin
3. Hedef sunucunun yavaş olup olmadığını kontrol edin
```

### Problem: "Zafiyet Bulunamadı"
```
Çözüm:
1. Hedef sistemin gerçekten zafiyet içerip içermediğini kontrol edin
2. Farklı tarama modüllerini deneyin
3. Parametreleri değiştirmeyi deneyin
4. Test ortamında deneyin (DVWA, bWAPP)
```

---

## 📞 DESTEK

### Sorular & Öneriler
- GitHub Issues: [Proje Linki]/issues
- Email: [Email Adresi]
- Discord: [Discord Sunucusu]

### Bug Raporlama
```
Lütfen şunları belirtin:
1. Hata mesajı
2. Kullanılan komut
3. Hedef sistem
4. Python versiyonu
5. İşletim sistemi
```

---

## 🤝 KATKIDA BULUNMA

Projeyi geliştirmek için katkıda bulunabilirsiniz:

```bash
# 1. Fork et
git fork https://github.com/[username]/k6-pentest.git

# 2. Branch oluştur
git checkout -b feature/yeni-ozellik

# 3. Değişiklikleri commit et
git commit -m "Yeni özellik eklendi"

# 4. Push et
git push origin feature/yeni-ozellik

# 5. Pull Request aç
```

---

## 📄 LİSANS

Bu proje **Eğitim ve Etik Hacking** amaçlı açık kaynak yazılımdır.

```
MIT License

Copyright (c) 2026 K6 Pentest Team

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.
```

---

## ⚠️ SORUMLULUK REDDİ

```
Bu araç sadece EĞİTİM ve YASAL AMAÇLARLA kullanılmalıdır.

Geliştirici, bu aracın kötüye kullanılmasından sorumlu DEĞİLDİR.

Yetkisiz erişim, veri hırsızlığı veya sistem hasarı için:
- Yasal sonuçlardan siz sorumlusunuz
- Cezai ve hukuki yaptırımlar uygulanabilir
- Uluslararası yasalar geçerlidir

SORUMLU KULLANIM SİZİN ELİNİZDE!
```

---

## 🎓 BAŞLAMAK İÇİN

### 1. Adım: Kurulum
```bash
pip install requests urllib3
python3 k6_pentest_tr.py
```

### 2. Adım: Test Ortamı Hazırla
```bash
# DVWA Docker
docker run --rm -it -p 80:80 vulnerables/web-dvwa

# Veya lokal sunucu
python3 -m http.server 8000
```

### 3. Adım: İlk Tarama
```
Seçim: 1
URL: http://localhost:8000

Seçim: 2 (Keşif)
Seçim: 3 (SQL Injection)
Seçim: 12 (Rapor)
```

### 4. Adım: Sonuçları Analiz Et
```
k6_rapor_YYYYMMDD_HHMMSS.txt dosyasını aç
Bulguları incele
Önerileri uygula
```

---

## 🌟 ÖZELLIKLER ÖZETI

✅ **11 Tarama Modülü** - Kapsamlı güvenlik testi  
✅ **Türkçe Menü** - Kolay kullanım  
✅ **Renkli Çıktı** - Okunması kolay sonuçlar  
✅ **Otomatik Rapor** - Detaylı güvenlik raporu  
✅ **Multi-threading** - Hızlı tarama  
✅ **Ayarlanabilir** - Timeout, thread, user-agent  
✅ **Eğitim Amaçlı** - Güvenlik öğrenin  
✅ **Açık Kaynak** - Geliştirin ve katkıda bulunun  

---

## 📊 PERFORMANS

- **Keşif:** ~2-5 saniye
- **SQL Injection:** ~30-60 saniye
- **XSS Taraması:** ~30-60 saniye
- **Dizin Keşfi:** ~20-40 saniye
- **Tam Tarama:** ~5-10 dakika

---

## 🔐 GÜVENLİK

- SSL/TLS sertifikası doğrulanmaz (test amaçlı)
- Proxy desteği yok (gelecek sürümde)
- Kimlik doğrulama desteği sınırlı (gelecek sürümde)

---

## 📝 CHANGELOG

### v2.0 (Mevcut)
- ✅ 11 tarama modülü
- ✅ Türkçe menü
- ✅ Otomatik rapor
- ✅ Multi-threading
- ✅ Ayarlanabilir parametreler

### v1.0
- ✅ Temel tarama modülleri
- ✅ İngilizce menü

---

## 🎯 SONRAKI SÜRÜMLER

- 🔄 Proxy desteği
- 🔄 Kimlik doğrulama (Basic, Digest, OAuth)
- 🔄 Stres testi (Load Testing)
- 🔄 Grafik arayüz (GUI)
- 🔄 API desteği
- 🔄 Veritabanı entegrasyonu

---

## 👨‍💻 GELIŞTIRICI

**K6 Pentest Team**

- GitHub: [@username](https://github.com/username)
- Twitter: [@username](https://twitter.com/username)
- Email: [email@example.com](mailto:email@example.com)

---

## 🙏 TEŞEKKÜRLER

Bu projeyi mümkün kılan tüm açık kaynak kütüphanelere ve topluluğa teşekkür ederiz.

---

**Güvenli kalın! 🛡️**

*Son güncelleme: 11 Mart 2026*
