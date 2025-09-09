# Turkiye-Ulusal-Gozlemevi

### 3 Katmanlı iletişim


<img width="684" height="400" alt="image" src="https://github.com/user-attachments/assets/575c38de-0ba4-49fc-bb35-c75793857a05" />



## TCP/IP Protocol


<img width="452" height="428" alt="image" src="https://github.com/user-attachments/assets/e8308b2a-4749-414f-a1b3-0f8f81f348d0" />

<img width="1207" height="741" alt="image" src="https://github.com/user-attachments/assets/c153204f-c2dc-4a26-a703-270d33d30183" />

#### 4 Katmanı:

Uygulama Katmanı (Application Layer): Kullanıcıya en yakın katmandır. HTTP, FTP, SMTP, DNS gibi protokoller burada çalışır. Veri bu katmanda oluşturulur.

Taşıma Katmanı (Transport Layer): İki cihaz arasındaki uçtan uca iletişimi yönetir. Veriyi paketlere böler (segment) ve iletim kontrolünü yapar. TCP (güvenilir, sıralı) ve UDP (hızlı, güvenilmez) buradadır.

İnternet Katmanı (Internet Layer): Paketlerin farklı ağlar üzerinden yönlendirilmesinden (routing) sorumludur. IP (Internet Protocol) bu katmanın temelidir. Paketlere IP adresleri ekler.

Ağ Erişim Katmanı (Link Layer): Fiziksel ağ (Ethernet, Wi-Fi) üzerinden veri çerçevelerinin (frame) nasıl gönderileceğini tanımlar. Donanıma en yakın katmandır.

- TCP/IP, "mektubun zarfı, adresi ve posta servisidir." İçeriği umursamaz, sadece doğru yere ulaştırmakla ilgilenir.



<img width="1043" height="542" alt="image" src="https://github.com/user-attachments/assets/11c930aa-ee86-4f68-957a-83f68c1b5e3c" />


#### Physical Layer 
- It is responsible for transmitting the bits within the frame along the line. The physical 
layer, like other layers, can be considered as a logical connection because the physical 
layer uses a transmission medium for transportation. There are two signal types: analog signals, digital signals.
(Hub, Repeater)

#### Data-link Layer 
- It transports datagrams received from the network layer between lines in frame form.
(Ethernet, Switch)
  
#### Network Layer 
- It is responsible for establishing the connection between Source and Destination hosts.
Communication at this layer is called host-to-host.
(IP, ICMP, Router)

#### Transport Layer 
- It is responsible for servicing the application layer. The logical link in this layer is
referred to as end-to-end. The message received from the Application layer is sent to 
the Transport layer and divided into segments. It is logically sent to the Transport layer 
of the receiving party. The other party transforms the segment into a message and 
then sends it to its Application layer.
(TCP, UDP)

#### Application Layer 
- Process-to-process communication takes place in this layer. The information produced 
by one side's Application layer process is transmitted by communicating with the other 
side's Application layer process.
(HTTP, SMTP, FTP)



## OSI Modeli (Open System Interconnection)
OSI is a communication model standard determined by 
ISO (International Organization for Standardization). ISO is an organization, OSI is a 
model. 

<img width="462" height="312" alt="image" src="https://github.com/user-attachments/assets/07a32398-99bd-4e98-8fe8-604694c37a04" />

- TCP/IP'den farklı olarak ek iki katman daha vardır:

#### Sunum (Presentation)
- Veri şifreleme, sıkıştırma, dönüştürme (SSL/TLS, JPEG)

#### Oturum (Session)
- İki cihaz arasındaki iletişim oturumunu yönetir (RPC)


It has a layered architecture. In the TCP/IP model, Session and Presentation layers are 
integrated with the Application layer.


## HTTP
HTTP (Köprü Metni Aktarım Protokolü), web üzerinden veri aktarımı için kullanılan temel protokoldür. Mesajların nasıl biçimlendirilip iletileceği ve web sunucularının ve tarayıcıların çeşitli komutlara nasıl yanıt vermesi gerektiğiyle ilgili kuralları tanımlar. HTTP, World Wide Web'de veri iletişiminin temelini oluşturur ve kullanıcıların web tarayıcıları aracılığıyla web sayfalarını görüntülemelerine, dosya indirmelerine ve çevrimiçi içerikle etkileşim kurmalarına olanak tanır.

Hypertext Transfer Protocol, bir Uygulama Katmanı protokolüdür. TCP/IP yığını üzerinde çalışır.


HTTP, web genelinde çeşitli senaryolarda kullanılır:

- Web Taraması: Bir kullanıcı tarayıcısına bir URL girdiğinde, web sitesini barındıran sunucuya bir HTTP isteği gönderilir ve sunucu, web sayfası verilerini tarayıcıya geri göndererek yanıt verir.
- API İstekleri: Birçok web hizmeti ve uygulama, istekleri göndermek ve API'lerden (Uygulama Programlama Arayüzleri) yanıt almak için HTTP kullanır ve bu da farklı yazılım sistemleri arasında veri alışverişini kolaylaştırır.
- Dosya İndirmeleri: HTTP, internetten dosya indirmek için yaygın olarak kullanılır; ister bir yazılım güncellemesi, ister bir belge, isterse de multimedya içeriği olsun.
- Akışlı Ortam: HTTP, kullanıcılara ses ve video içeriği sunmak için akış protokollerinde (HLS gibi) kullanılır ve kullanıcıların web üzerinden medya izlemelerine veya dinlemelerine olanak tanır.
- Form Gönderimleri: Kullanıcılar web sitelerindeki formları doldurup gönderdiğinde, form verileri işlenmek üzere sunucuya göndermek için HTTP kullanılır.
Bu örnekler, HTTP'nin basit web tarama işlemlerinden karmaşık veri alışverişlerine kadar çok çeşitli çevrimiçi etkinliklerin temelini nasıl oluşturduğunu göstermektedir.



HTTP, bir istemci (genellikle bir web tarayıcısı) ile bir sunucu arasında bir istek-yanıt modeli üzerinde çalışır:

- İstemci İsteği: Bir kullanıcı bir URL yazarak veya bir bağlantıya tıklayarak bir web sayfası istediğinde, tarayıcı sunucuya bir HTTP isteği gönderir. Bu istek, bir HTML sayfası, resim veya video gibi istenen kaynağı belirtir.
- Sunucu Yanıtı: Sunucu isteği işler ve bir HTTP yanıtı gönderir. Bu yanıt, istenen kaynak ve durum bilgilerini içerir (örneğin, başarılı bir istek için "200 OK" veya kaynak eksikse "404 Bulunamadı").
- Durumsuz Protokol: HTTP durumsuzdur, yani bir istemciden sunucuya yapılan her istek önceki isteklerden bağımsızdır. Bu tasarım iletişimi kolaylaştırır, ancak oturum bilgilerini korumak için çerezler gibi mekanizmalar gerektirir.
- Veri Aktarımı: HTTP, verileri düz metin veya şifreli formatlarda (HTTPS üzerinden) aktarır. HTML, CSS, JavaScript, resimler ve videolar dahil olmak üzere çeşitli veri türlerini destekler.
- Kalıcı Bağlantılar: HTTP/1.1 ve HTTP/2 gibi modern HTTP sürümleri, kalıcı bağlantıları destekleyerek tek bir bağlantı üzerinden birden fazla istek ve yanıt gönderilmesine olanak tanır, gecikmeyi azaltır ve verimliliği artırır.

##### Bu süreç, kullanıcıların web içeriğine hızlı ve güvenilir bir şekilde erişebilmelerini ve etkileşimde bulunabilmelerini sağlar.

#### Örnek çalışması:

1- İstemci (ör. Chrome) bir TCP bağlantısı açar (genellikle port 80/443).

2- Bir HTTP Request (İstek) gönderir (GET /api/users HTTP/1.1).

3- Sunucu isteği işler ve bir HTTP Response (Yanıt) döndürür (200 OK + JSON verisi).

4- TCP bağlantısı kapatılır (veya keep-alive ile açık kalır).

Özet: HTTP, TCP/IP'nin sağladığı güvenilir iletişim kanalını kullanarak "web içeriğinin" nasıl talep edileceğini ve sunulacağını tanımlar.


##### Yıllar geçtikçe HTTP, internetin artan taleplerini karşılamak için evrim geçirdi ve çeşitli versiyonlar ve türler ortaya çıktı:

- HTTP/1.0: Temel istek-yanıt modelini kuran ancak her istek için yeni bir bağlantı gerektiren HTTP'nin orijinal sürümü.
- HTTP/1.1: Kalıcı bağlantılar tanıtıldı, böylece tek bir bağlantı üzerinden birden fazla istek gönderilebiliyor ve performans önemli ölçüde artırılıyor.
- HTTP/2: Çoklama (paralel olarak birden fazla istek ve yanıt), başlık sıkıştırma ve önceliklendirmeyi tanıtan, hızı ve verimliliği daha da artıran önemli bir revizyon.
- HTTPS (HTTP Secure): İstemci ve sunucu arasında aktarılan verileri gizlice dinlemeye ve kurcalamaya karşı korumak için SSL/TLS şifrelemesini kullanan bir HTTP uzantısıdır.
- HTTP/3: QUIC protokolü üzerine kurulu en son sürümdür, özellikle mobil ve yüksek gecikmeli ağlarda gecikmeyi daha da azaltır, güvenliği ve performansı artırır.

HTTP'nin bu sürümleri ve türleri, protokolün verimli, güvenli kalmasını ve modern web trafiği taleplerini karşılayabilmesini sağlar.



## REST API (Web API)

Representational State Transfer, dağıtık sistemler için bir yazılım mimarisidir. Web API'leri bu mimari stilinde inşa edilir. Temelinde HTTP protokolünün mevcut özelliklerini (method'ları, status kodlarını) akıllıca kullanmak yatar.

Temel Prensipleri:

- İstemci-Sunucu: Arayüz ve veri depolama birbirinden ayrıdır.

- Durumsuzluk (Stateless): Her istek, kendinden önceki isteklerden bağımsızdır. Tüm gerekli bilgi istekte bulunur.

- Önbellekleme (Cacheable): Yanıtlar önbelleğe alınabilir olmalıdır.

- Tekdüzen Arayüz (Uniform Interface): Kaynaklara URI'ler ile erişilir. HTTP metodları (GET, POST, PUT, DELETE) ile işlem yapılır.

GET /users -> Tüm kullanıcıları getir.

POST /users -> Yeni kullanıcı oluştur.

GET /users/123 -> 123 ID'li kullanıcıyı getir.

PUT /users/123 -> 123 ID'li kullanıcıyı güncelle.

DELETE /users/123 -> 123 ID'li kullanıcıyı sil.


#### Python Client & Postman:

Python Client: requests kütüphanesi ile bir Python scripti yazarsınız. Bu script, HTTP istekleri atarak REST API ile iletişim kuran bir istemci olur.

Postman: REST API'leri test etmek, dokümante etmek ve paylaşmak için kullanılan bir GUI (grafiksel arayüz) tool'udur. Arka planda sizin yerinize HTTP istekleri atar. Geliştiriciler ve testçiler için vazgeçilmez bir araçtır.

İlişki: REST API, HTTP protokolünü bir "uygulama protokolü" olarak kullanır. Yani, HTTP'nin üzerine inşa edilmiş bir katmandır.







## Microservice Mimarisi + Docker Konteyner Teknolojisi

<img width="903" height="559" alt="Ekran görüntüsü 2025-09-09 091725" src="https://github.com/user-attachments/assets/b3264511-5c83-485c-b70d-7781d6718542" />


#### Mikroservis Mimarisi Nedir?
Bir uygulamayı, birbiriyle loosely coupled (gevşek bağlı) ve tek bir sorumluluğu olan küçük, bağımsız servislere bölme yaklaşımıdır. Her mikroservis kendi veritabanına sahip olabilir ve diğer servislerle API'ler (genellikle REST API) üzerinden iletişim kurar.


#### Docker Konteyner Teknolojisi Nedir?
Konteynerlar, bir uygulamayı ve tüm bağımlılıklarını (kütüphaneler, çalışma ortamı vb.) tek bir pakette (image) toplayarak, herhangi bir ortamda (geliştirici makinesi, test sunucusu, production) tutarlı ve izole bir şekilde çalıştırmayı sağlayan bir teknolojidir.





#### Neden Birlikte Mükemmeller?

1- Bağımsız Dağıtım: Her bir mikroservis, bir Docker konteyneri olarak paketlenebilir. Ürün Servisi'ni güncellediğinizde sadece onun konteynerini yeniden başlatırsınız, tüm uygulamayı değil.

2- Ortam Tutarlılığı: "Benim makinemde çalışıyordu" sorununu ortadan kaldırır. Geliştirme, test ve production ortamları birbirinin aynısı olur.

3- Ölçeklenebilirlik: Yoğunluğun arttığı servisin (ör. Ödeme Servisi) sadece o konteynerinden daha fazla açarak (scale) kaynak kullanımını optimize edebilirsiniz.

4- Teknoloji Çeşitliliği: Kullanıcı Servisi Python + Django, Sipariş Servisi Java + Spring Boot ile yazılabilir. Docker hepsini aynı sunucuda sorunsuzca çalıştırır.

#### İlişki:
Mikroservisler, birbirleriyle HTTP üzerinden konuşan REST API'ler aracılığıyla iletişim kurar. Bu servisler, Docker konteynerleri olarak paketlenip dağıtılır. Docker, bu iletişimi sağlamak için konteynerler arası sanal ağlar (networking) oluşturur.




#### Büyük Resim:
Bir kullanıcı mobil uygulamanızdan bir ürün aradığında olanları düşünelim:

1- Mobil Uygulama (İstemci), Ürün Servisine bir istek atar: GET https://api.sirket.com/products?search=telefon

2- Bu istek, HTTP protokolü kurallarına göre paketlenir.

3- HTTP paketi, TCP/IP yığınından geçer.

4- TCP katmanında güvenilir bir bağlantı kurulur ve veri segmentlere ayrılır.

5- IP katmanında bu segmentlere hedef ve kaynak IP adresleri eklenir ve yönlendirilir.

6- İstek, Ürün Servisi'nin çalıştığı Docker Konteynerine ulaşır.

7- Konteyner içindeki uygulama, bu REST API isteğini işler, veritabanından "telefon" ürünlerini arar.

8- Sonuçlar yine HTTP Response olarak, TCP/IP üzerinden mobil uygulamaya geri döner.

9- Tüm bu süreç, OSI Modeli kullanılarak her katmanda debug edilebilir veya analiz edilebilir.



#### Sonuç:

- TCP/IP: Verinin yolda nasıl ilerleyeceğinin otoyol kuralları.

- HTTP: Otoyolda giden kurye aracının içindeki mektubun yazım formatı.

- REST API: Kuryenin getirdiği mektupta yazan standartlaştırılmış iş emri.

- Mikroservisler: Bu iş emirlerine göre çalışan, şehrin farklı yerlerindeki uzmanlaşmış ekipler.

- Docker: Her ekibin kendi bağımsız, taşınabilir ofis konteyneri.

