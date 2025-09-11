
# REST API (Web API)

## API Nedir?
**API (Application Programming Interface)**, uygulamaların veya cihazların birbirine nasıl bağlanacağını ve iletişim kuracağını tanımlayan bir dizi kuraldır.  
API entegrasyonu, veri alışverişi yapmak ve ortak bir işlev gerçekleştirmek için iki veya daha fazla uygulamanın API üzerinden bağlanmasını ifade eder.

---

## REST Nedir?
**REST (Representational State Transfer)**, client-server arasındaki haberleşmeyi sağlayan HTTP protokolü üzerinden çalışan bir mimaridir.  
- JSON veya XML formatında veri taşır.  
- Bu mimariyi kullanan servislere **RESTful servis (RESTful API)** denir.  
- Amazon, Google, Facebook, LinkedIn, Twitter gibi dev platformlar REST API’leri kullanır.  

REST API ile çalışmak için tek ihtiyacımız olan **URL**’dir.  
Client, belirli bir URL’e istek atar ve sunucudan JSON/XML formatında cevap alır.

---

## REST’in Temel Kavramları
- **Client (İstemci):** API’yi kullanan kişi veya yazılım. (Örn: Tarayıcı, mobil uygulama, Python scripti)  
- **Server (Sunucu):** API’yi barındırır, gelen istekleri işleyip cevap döner.  
- **Resource (Kaynak):** API’nin sunduğu veri nesneleri (örn: kullanıcı, ürün, fotoğraf). Her kaynağın benzersiz bir **identifier**’ı (ID, isim vb.) vardır.  

---

## REST’in Temel Prensipleri
1. **İstemci-Sunucu (Client-Server):**  
   - Arayüz ve veri depolama ayrıdır.  
   - Client ve server bağımsız geliştirilebilir.  

2. **Durumsuzluk (Stateless):**  
   - Her istek bağımsızdır, gerekli bilgiler isteğin içinde taşınır.  
   - Server, client hakkında session bilgisi tutmaz.  

3. **Önbellekleme (Cacheable):**  
   - Yanıtlar cache’lenebilir olmalıdır.  
   - API, hangi verilerin cache’lenebilir olduğunu belirtmelidir.  

4. **Tekdüzen Arayüz (Uniform Interface):**  
   - Kaynaklara URI üzerinden erişilir.  
   - Standart HTTP metodları kullanılır: **GET, POST, PUT, DELETE**.  

5. **Katmanlı Sistem (Layered System):**  
   - Client ile server arasında cache, güvenlik, proxy gibi ara katmanlar olabilir.  
   - Katmanlar birbirini doğrudan bilmez, sadece komşu katmanla iletişim kurar.  

6. **Code on Demand (Opsiyonel):**  
   - Server, client’a çalıştırılabilir kod gönderebilir (örn: script).  

---

## REST API HTTP Metodları
- **GET /users** → Tüm kullanıcıları getir  
- **POST /users** → Yeni kullanıcı oluştur  
- **GET /users/123** → ID’si 123 olan kullanıcıyı getir  
- **PUT /users/123** → ID’si 123 olan kullanıcıyı güncelle  
- **DELETE /users/123** → ID’si 123 olan kullanıcıyı sil  

---

## REST API Test Araçları

### Python Client
`requests` kütüphanesi kullanılarak Python ile HTTP istekleri yapılabilir.  
Örn:  
```python
import requests

response = requests.get("https://api.example.com/users")
print(response.json())



