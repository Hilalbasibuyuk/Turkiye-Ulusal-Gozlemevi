# HTTP (Hypertext Transfer Protocol)

## HTTP Nedir?
**HTTP (Köprü Metni Aktarım Protokolü)**, web üzerinden veri aktarımı için kullanılan temel protokoldür.  
- Mesajların nasıl biçimlendirilip iletileceğini tanımlar.  
- Web sunucularının ve tarayıcıların komutlara nasıl yanıt vereceğini belirler.  
- **World Wide Web**’de veri iletişiminin temelini oluşturur.  
- **Uygulama Katmanı** protokolüdür ve **TCP/IP** üzerinde çalışır.  

HTTP sayesinde kullanıcılar:  
- Web sayfalarını görüntüleyebilir,  
- Dosya indirebilir,  
- Çevrimiçi içerikle etkileşim kurabilir.  

API’lar da veri paylaşımı için HTTP’yi kullanır.

---

## HTTP Kullanım Alanları
- **Web Taraması:** URL girildiğinde tarayıcı, sunucuya HTTP isteği gönderir ve yanıt olarak web sayfasını alır.  
- **API İstekleri:** Farklı yazılım sistemleri arasında veri alışverişini sağlar.  
- **Dosya İndirme:** Yazılım, belge veya medya dosyalarının indirilmesi.  
- **Akışlı Medya:** Ses ve video içeriği (örn: HLS protokolü).  
- **Form Gönderimi:** Web formlarındaki verilerin sunucuya iletilmesi.  

---

## HTTP Çalışma Mantığı
HTTP, **istemci-sunucu arasında istek-yanıt modeli** ile çalışır:

1. **İstemci isteği:** Tarayıcı, URL ile sunucuya HTTP isteği gönderir.  
2. **Sunucu yanıtı:** İstek işlenir, yanıt gönderilir (örn: `200 OK`, `404 Not Found`).  
3. **Durumsuzluk (Stateless):** Her istek bağımsızdır. Session için cookie gibi ek mekanizmalar gerekir.  
4. **Veri aktarımı:** HTML, CSS, JS, resim, video gibi farklı içerikler taşınabilir.  
5. **Kalıcı bağlantılar:** HTTP/1.1 ve üstü sürümlerde tek bağlantı üzerinden birden fazla istek/yanıt yapılabilir.  

### Örnek İşleyiş
1. İstemci (örn: Chrome) **TCP bağlantısı** açar (port 80/443).  
2. **HTTP Request** gönderir: `GET /api/users HTTP/1.1`  
3. Sunucu isteği işler, **HTTP Response** döner: `200 OK + JSON verisi`  
4. TCP bağlantısı kapatılır (veya **keep-alive** ile açık kalır).  

---

## HTTP’nin Evrimi ve Sürümleri
- **HTTP/1.0:** Her istek için yeni bağlantı gerektirir.  
- **HTTP/1.1:** Kalıcı bağlantılar ile performans artırıldı.  
- **HTTP/2:** Çoklama (parallel requests), başlık sıkıştırma, önceliklendirme özellikleri eklendi.  
- **HTTPS:** SSL/TLS ile şifrelenmiş güvenli HTTP.  
- **HTTP/3:** QUIC protokolü üzerine kurulu, mobil ve yüksek gecikmeli ağlar için daha hızlı ve güvenli.  

---

## Özet
HTTP, **TCP/IP’nin güvenilir iletişim kanalını** kullanarak web içeriklerinin nasıl talep edilip sunulacağını tanımlar.  
Modern web trafiği taleplerini karşılamak için sürekli geliştirilmiş ve yeni sürümlerle performans, güvenlik ve verimlilik artırılmıştır.
