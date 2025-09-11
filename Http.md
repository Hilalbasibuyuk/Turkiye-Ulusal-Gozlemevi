
## HTTP
HTTP (Köprü Metni Aktarım Protokolü), web üzerinden veri aktarımı için kullanılan temel protokoldür. Mesajların nasıl biçimlendirilip iletileceği ve web sunucularının ve tarayıcıların çeşitli komutlara nasıl yanıt vermesi gerektiğiyle ilgili kuralları tanımlar. HTTP, World Wide Web'de veri iletişiminin temelini oluşturur ve kullanıcıların web tarayıcıları aracılığıyla web sayfalarını görüntülemelerine, dosya indirmelerine ve çevrimiçi içerikle etkileşim kurmalarına olanak tanır. Web uygulamaları arasında veri paylaşımını sağlamak için kullanılan API’lar (Application Programming Interface) HTTP protokolünü temel alır. Bu sayede farklı uygulamalar arasında veri alışverişi protokol üzerinden gerçekleşir.

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
