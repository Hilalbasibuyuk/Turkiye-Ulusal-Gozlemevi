

## REST API (Web API)

#### API nedir?

Öncelikle ‘API nedir, nasıl çalışır?’ tanımlayacak olursak; bir API veya uygulama programlama arabirimi (Application Programming Interface), uygulamaların veya cihazların birbirine nasıl bağlanabileceğini ve birbirleriyle iletişim kurabileceğini tanımlayan bir dizi kuraldır. API entegrasyonu, veri alışverişi yapmak ve ortak bir işlev gerçekleştirmek için API’leri aracılığıyla birbirine bağlanan ve böylece uygulamalar arasında etkileşimi sağlayan birkaç uygulamayı (iki veya daha fazla) ifade eder.

REST, client-server arasındaki haberleşmeyi sağlayan HTTP protokolü üzerinden çalışan bir mimaridir. İstemci ve sunucu arasında XML ve JSON verilerini taşıyarak uygulamanın haberleşmesini sağlar. REST mimarisini kullanan servislere ise RESTful servis (RESTful API) denir. Amazon, Google, Facebook, LinkedIn ve Twitter gibi çeşitli web siteleri, kullanıcıların bu bulut hizmetleriyle iletişim kurmasını sağlayan REST tabanlı API’leri kullanır.

REST ile yazılmış bir servisle çalışmak için ihtiyacımız olan tek şey URL. Bir URL’e istek attığımızda, URL size JSON veya XML formatında bir cevap döndürür, dönen cevap parse edilir ve servis entegrasyonunuz tamamlanır. Yani client uygulama, REST bir servisin yapısını ve detaylarını bilmek zorunda değildir. Rest servisler; client ve server arasındaki ayrım sayesinde, REST protokolü, bir projenin farklı alanlarındaki geliştirmelerin bağımsız olarak gerçekleşmesini kolaylaştırır. REST API, operasyonel sözdizimine ve platforma göre ayarlanabilir ve geliştirme sırasında çok sayıda ortamı test etme olanağı sunar.Kullanıcılar, REST client-server farklı sunucularda barındırılsa bile kolayca iletişim kurabilir , bu da yönetim açısından önemli bir fayda sağlar.





Representational State Transfer, dağıtık sistemler için bir yazılım mimarisidir. Web API'leri bu mimari stilinde inşa edilir. Temelinde HTTP protokolünün mevcut özelliklerini (method'ları, status kodlarını) akıllıca kullanmak yatar.


1. Client(İstemci) : Client, API’yi kullanan kişi veya yazılımdır. Bir geliştirici olabilir, örneğin bir geliştirici olarak siz, Twitter API’sini Twitter’dan veri okumak ve yazmak, yeni bir tweet oluşturmak ve yazdığınız bir programda daha fazla işlem yapmak için kullanabilirsiniz. Programınız Twitter’ın API’sine istek atacak. İstemci ayrıca bir web tarayıcısı olabilir. Twitter web sitesine gittiğinizde, tarayıcınız Twitter API’sine istek atan ve döndürülen verileri ekranda bilgi işlemek için kullanan istemcidir.

2. Server (Sunucu): Tüm API ve işlevsellikleri üzerinde barındıran sistemdir. Client’den gelen istekleri işlemek ve gerekli cevapları yine istenen formatta dönmekle sorumludur.

3. Resource (Kaynak): Bir kaynak, API’nin bilgi sağlayabileceği herhangi bir nesne olabilir. Örneğin; Instagram’ın API’sinde bir kaynak: kullanıcı, fotoğraf ya da hashtag olabilir. Her kaynağın benzersiz bir tanımlayıcısı (unique identifier) vardır. Tanımlayıcı bir isim veya bir numara olabilir.



Temel Prensipleri:

#### İstemci-Sunucu: Arayüz ve veri depolama birbirinden ayrıdır.
- Client ve server bağımsız hareket eder, her biri kendi başına ve aralarındaki etkileşim yalnızca client tarafından başlatılan istekler ve server’ın yalnızca bir isteğe tepki olarak client’a gönderdiği yanıtlar biçimindedir. Server yalnızca client’dan gelen istekleri bekler. Server, bazı kaynakların durumu hakkında kendi başına bilgi göndermeye başlamaz. Bunun sonucunda client ve server birbirinden bağımsız olarak geliştirilir, server tarafında geliştirme basit ve ölçeklenebilirlik yüksek olur ve client tarafında ise kodun taşınabilirliği yüksek olur.

#### Durumsuzluk (Stateless): Her istek, kendinden önceki isteklerden bağımsızdır. Tüm gerekli bilgi istekte bulunur.
- REST’in stateless olması server’ın client hakkında session gibi bilgileri tutmaması demektir. Bu gibi bilgileri yalnızca client tutar. Dolayısıyla server, istek yapan client’ın daha önce kaç istek yaptığı veya hangi istekleri yaptığı gibi bilgileri tutmaz. Client ise yaptığı istekte server’ın ihtiyaç duyduğu tüm bilgileri verir.

Fakat aynı zamanda server, client’a ilişkin veri tutmadığı için client’ın her istekte bazı bilgileri göndermesi maliyeti artırır. Bu da stateless oluşunun dezavantajı olarak sayılabilir.


#### Önbellekleme (Cacheable): Yanıtlar önbelleğe alınabilir olmalıdır.
- Durum bilgisi olmayan bir API, çok sayıda gelen ve giden çağrıyı yöneterek istek yükünü artırabileceğinden , bir REST API tasarımı önbelleğe alınabilir verileri depolayabilmelidir. Bu API tasarım ilkesine göre, bir yanıttaki veriler dolaylı veya açık bir şekilde cacheable veya uncacheable olarak sınıflandırılmalıdır .

Bir yanıt önbelleğe alınabilirse, istemci önbelleğine gelecekte benzer istekler için bu yanıt verilerini geri dönüştürme hakkı verilir.

#### Tekdüzen Arayüz (Uniform Interface): Kaynaklara URI'ler ile erişilir. HTTP metodları (GET, POST, PUT, DELETE) ile işlem yapılır.
-  Aynı kaynak için tüm API istekleri, isteğin nereden geldiğine bakılmaksızın aynı görünmelidir. REST API, bir kullanıcının adı veya e-posta adresi gibi aynı veri parçasının yalnızca tek bir tek tip kaynak tanımlayıcısına (URI) ait olmasını sağlamalıdır. Kaynaklar çok büyük olmamalı, ancak karşı tarafın ihtiyaç duyabileceği her türlü bilgiyi içermelidir.


#### Layered System
- Client-Server mimarisinden bahsederken kastımız her zaman bir client’ın doğrudan bir server’a istek göndermesi ve ondan doğrudan cevap alması şeklinde değildir. Aralarda güvenlik katmanı, cache katmanı gibi katmanlar olabilir. Böyle bir sistemde aralardaki katmanlar request ve response’a etki etmemeli. Her katman yalnızca iletişime geçtiği katmanları bilmeli.


#### Code On Demand
- Zorunlu olmayan tek kısıt code on demand’dir. Client, serverdan kod talep edebilir ve daha sonra, yanıt HTML biçiminde olduğunda, serverden gelen yanıt, genellikle bir komut dosyası biçiminde bazı kodlar içerecektir. Client daha sonra bu kodu çalıştırabilir.

GET /users -> Tüm kullanıcıları getir.

POST /users -> Yeni kullanıcı oluştur.

GET /users/123 -> 123 ID'li kullanıcıyı getir.

PUT /users/123 -> 123 ID'li kullanıcıyı güncelle.

DELETE /users/123 -> 123 ID'li kullanıcıyı sil.


#### Python Client & Postman:

Python Client: requests kütüphanesi ile bir Python scripti yazarsınız. Bu script, HTTP istekleri atarak REST API ile iletişim kuran bir istemci olur.

Postman: REST API'leri test etmek, dokümante etmek ve paylaşmak için kullanılan bir GUI (grafiksel arayüz) tool'udur. Arka planda sizin yerinize HTTP istekleri atar. Geliştiriciler ve testçiler için vazgeçilmez bir araçtır.

İlişki: REST API, HTTP protokolünü bir "uygulama protokolü" olarak kullanır. Yani, HTTP'nin üzerine inşa edilmiş bir katmandır.


