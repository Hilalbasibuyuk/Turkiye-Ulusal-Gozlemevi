# Turkiye-Ulusal-Gozlemevi

### 3 Katmanlı iletişim


<img width="684" height="400" alt="image" src="https://github.com/user-attachments/assets/575c38de-0ba4-49fc-bb35-c75793857a05" />



## TCP(Transmisson Control Protocol)/IP (Internet Protocol)
TCP (Transmisson Control Protocol), TCP/IP modelinde taşıma katmanı protokollerinden birisidir ve son güncellemesi Ağustos 2022 tarihi itibariyle RFC 9293 içerisinde tanımlanmıştır. TCP kısaca , veri paketlerini toplayan ve yeniden birleştiren bileşendir diyebiliriz.
IP (Internet Protocol), internet üzerinden veri alışverişi yapılırken gerçekleşen yönlendirmenin kurallarını düzenleyen protokoldür. Kısacası yönlendirme protokolü de diyebiliriz. IP, verinin içeriğiyle yada niteliğiyle ilgilenmez sadece gideceği adresi belirler.


<img width="452" height="428" alt="image" src="https://github.com/user-attachments/assets/e8308b2a-4749-414f-a1b3-0f8f81f348d0" />

<img width="1207" height="741" alt="image" src="https://github.com/user-attachments/assets/c153204f-c2dc-4a26-a703-270d33d30183" />

#### 4 Katmanı:

Uygulama Katmanı (Application Layer): Süreçler arası iletişim bu katmanda gerçekleşir. Bir tarafın Uygulama katmanı süreci tarafından üretilen bilgi, diğer tarafın Uygulama katmanı süreciyle iletişim kurularak iletilir. Kullanıcıya en yakın katmandır. HTTP, FTP, SMTP, DNS gibi protokoller burada çalışır. Veri bu katmanda oluşturulur. (HTTP, SMTP, FTP,SSH, Telnet)

Taşıma Katmanı (Transport Layer): Uygulama katmanının bakımından sorumludur. Bu katmandaki mantıksal bağlantı uçtan uca olarak adlandırılır. Uygulama katmanından alınan mesaj, Taşıma katmanına gönderilir ve parçalar halinde bölünür. Mantıksal olarak, alıcı tarafın Taşıma katmanına iletilir. Diğer taraf, parçayı bir mesaja dönüştürür ve ardından bunu kendi Uygulama katmanına gönderir. Veriyi paketlere böler (segment) ve iletim kontrolünü yapar. TCP (güvenilir, sıralı) ve UDP (hızlı, güvenilmez) buradadır. (TCP, UDP)

Network Layer : Paketlerin farklı ağlar üzerinden yönlendirilmesinden (routing) sorumludur. IP (Internet Protocol) bu katmanın temelidir. Paketlere IP adresleri ekler. Kaynak ve Hedef ana bilgisayarları arasında bağlantıyı kurmakla sorumludur. Bu katmandaki iletişime ana bilgisayarlar arası denir. Genel olarak, adresleme işleminin yani gideceği yerin IP adresinin verildiği katmandır.(IP, ICMP, Router, ARP, RARP, BOOTP)


Ağ Erişim Katmanı (Data Link Layer): Fiziksel ağ (Ethernet, Wi-Fi) üzerinden veri çerçevelerinin (frame) nasıl gönderileceğini tanımlar. Donanıma en yakın katmandır.Ağ katmanından alınan datagramları çerçeve biçiminde hatlar arasında taşır. Kablolu veya kablosuz ethernet kartımızın MAC adresini aldığımız ve ARP protokolünün çalıştığı katman olarak bilinir.(Ethernet, Switch, SLIP, PPP)


Fiziksel Katman(Physical Layer): Çerçeve içindeki bitleri hat boyunca iletmekten sorumludur. Diğer katmanlar gibi fiziksel katman da mantıksal bir bağlantı olarak değerlendirilebilir çünkü fiziksel katman, taşıma için bir iletim ortamı kullanır. Bu katmanda veriler, bir bilgisayara veya başka bir cihaza gönderilip okunabilecek bir şeye dönüştürülür. Örneğin, IEEE 802.3 protokolü, verileri Ethernet bağlantısında kullanılan verilere dönüştürmek için kullanılır. (Hub, Repeater, IEEE 1394, DSL, ISDN )


Avantajları
	Birçok Yönlendirme protokolü desteklenmektedir.
	Son derece ölçeklenebilirdir ve istemci-sunucu mimarisini kullanır.
	Hafiftir.
Dezavantajları
	Kurulumu biraz zor.
	Paketlerin teslimi taşıma katmanı tarafından garanti edilmez.
	Senkronizasyon saldırısına karşı savunmasız.






- TCP/IP, "mektubun zarfı, adresi ve posta servisidir." İçeriği umursamaz, sadece doğru yere ulaştırmakla ilgilenir.



<img width="1043" height="542" alt="image" src="https://github.com/user-attachments/assets/11c930aa-ee86-4f68-957a-83f68c1b5e3c" />



## OSI Modeli (Open System Interconnection)
OSI is a communication model standard determined by 
ISO (International Organization for Standardization). ISO is an organization, OSI is a 
model. 

<img width="462" height="312" alt="image" src="https://github.com/user-attachments/assets/07a32398-99bd-4e98-8fe8-604694c37a04" />

- TCP/IP'den farklı olarak ek iki katman daha vardır:




#### Sunum (Presentation)
- Veri şifreleme, sıkıştırma, dönüştürme. Sunum katmanı, verilerin şifrelenip şifresinin çözüldüğü ve uygulama katmanı tarafından erişilebilen bir forma dönüştürüldüğü yerdir. En önemli görevi ise yollanan verinin karşı bilgisayar tarafından anlaşılacak şekilde çevrilmesidir. Bu sayede farklı programların birbirlerinin verisini kullanabilmesi mümkün hale getirilir. (SSL/TLS, JPEG, ASCII,GIF, JPEG, TIFF, EBCDIC)

#### Oturum (Session)
- Oturum katmanı, uygulamalar arasında gerçekleşen oturumları yöneten bir bağlantıya sahiptir. Oturum katmanı, cihazlar arasındaki bağlantıları kontrol eder. Yereldeki ve uzaktaki bağlantıları kurabilir, yönetebilir veya sonlandırabilir. Ağ üzerinde bir bilgisayara bağlanarak oturum açmak gibi işlemlerin yapıldığı bu katman da çift yönlü haberleşme yapılır.(RPC, NFS, X WİNDOWS SYSTEM)


Avantajları
	Bağlantı odaklı servislerin yanı sıra bağlantısız servisler de desteklenmektedir.
	Oldukça esnektir.
	Tüm katmanlar bağımsız olarak çalışır.
Dezavantajları
	Bir model kurmak zorlu bir iştir.
	Bazen yeni bir protokolü bu modele uydurmak zor olabiliyor.
	Sadece referans model olarak kullanılmaktadır.




TCP/IP, belirli iletişim zorluklarını ele alan ve standartlaştırılmış protokollere dayanan pratik bir modeldir. Buna karşılık, OSI, çeşitli ağ iletişim yöntemlerini kapsayacak şekilde tasarlanmış, protokolden bağımsız, kapsamlı bir çerçeve görevi görür. Debug OSI'de daha kolaydır.

Birçok kullanıcı için, diğer tüm koşullar eşit olduğunda, OSI modeli tercih edilen seçenektir. Ağın işlevlerini daha fazla katmana ayırması, sorun gidermeyi ve ağ performansını iyileştirmeyi daha kolay hale getirir.

Ancak TCP/IP, daha fazla uygulamaya sahip olma avantajına sahiptir ve daha güncel ağ yapılarında da yaygın olarak kullanılmaktadır.


TCP/IP ile OSI arasındaki Farklar Nelerdir?
OSI modelinde yedi katman varken, TCP / IP modelinde dört katman kullanılır.
TCP/IP haberleşme görevini daha basit alt görevlere böler.Her bir alt görev diğer alt görevler için belirli servislere sunulur. OSI modeli de aynı kavramı kullanır ,ancak OSI modelinde her bir katmandaki protokollerin özellikleri ve birbiri ile ilişkileri kesin bir dille tanımlanmıştır. Bu özellik OSI modeli ile çalışmayı daha verimli kılar. TCP/IP ise böyle bir kısıtlama getirmediğinden, gerektiğinde yeni bir protokol mevcut katmanlar arasına rahatlıkla yerleştirilebilir.
OSI modelinde gerekmeyen bir katmanın kullanılmaması gibi esnek bir yapıya izin vermez. TCP/IP ise katı kurallarla tanımlı olmadığından gereksinim duyulmayan katmanların kullanılmamasına izin verir.
Bilgisayar ağlarında TCP / IP hala kullanılıyorken, OSI Katman modeli artık kullanılmamaktadır.
Üst katmanların işlevselliğini tanımlamak için, OSI üç ayrı katman kullanır (uygulama, sunu ve oturum), TCP / IP ise tek katman (uygulama) kullanır.
OSI de alt katların işlevselliğini tanımlamak için iki ayrı katman (Fiziksel ve Veri bağlantısı) kullanırken, TCP / IP de bunun için tek bir katman (Bağlantı) kullanır.
Yönlendirme protokollerini ve standartlarını tanımlamak için, OSI Ağ katmanını kullanırken, TCP / IP İnternet katmanını kullanır.
TCP / IP modeline kıyasla, OSI modeli iyi belgelenmiştir ve standartları ve protokolleri daha ayrıntılı olarak açıklamaktadır.
OSI modeline göre katmanların bazıları TCP/ IP modelinde birleştirilerek kolaylık sağlanır.
TCP/IP haberleşmeyi daha basit hale getirir. OSI modelindeki oturum, sunum ve uygulama katmanına karşılık TCP/IP sadece uygulama katmanını kullanır.
TCP/IP modeli UDP bağlantıları kullandığı zaman, iletim katmanında güvenililik kontrolü yapmaz. OSI modelinde ise bu güvenlik işlemi daima yapılır.



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





## Microservice Mimarisi + Docker Konteyner Teknolojisi

<img width="903" height="559" alt="Ekran görüntüsü 2025-09-09 091725" src="https://github.com/user-attachments/assets/b3264511-5c83-485c-b70d-7781d6718542" />


#### Mikroservis Mimarisi Nedir?
Bir uygulamayı, birbiriyle loosely coupled (gevşek bağlı) ve tek bir sorumluluğu olan küçük, bağımsız servislere bölme yaklaşımıdır. Her mikroservis kendi veritabanına sahip olabilir ve diğer servislerle API'ler (genellikle REST API) üzerinden iletişim kurar.

Microservice tek başına tek sorumluluğu olan ve tek iş yapan sadece o işe ait işleri yürüten modüler projelerdir. Bir yazılım uygulamasında belirli özellik ya da fonksiyonu sağlayan, tek bir amaca hizmet eden, birbirinden bağımsız yazılım servisleridir.Bu hizmetler bağımsız olarak bakımı yapılabilir, izlenebilir ve dağıtılabilir yapıya sahip olmalıdır.

Microservice mimarisinin başlangıç noktası SOA’dır. Microservice, SOA yani "Services Oriented Architecture" üzerine kurulmuş bir mimaridir. Service oriented architecture (SOA), uygulamaların birbirleriyle tek bir makine veya ağ üzerinden birden çok makineye dağıtıldığında, servislerin dağıtım sistemde iletişim kurmasını sağlayabilen bir mimaridir.

Microservice mimarisi, tek bir uygulama geliştirirken modüler bir yapıda her biri küçük servis olarak düşünülmesi gereken ve her bir servisinde kendi işini ve iletişimini yürütebilen, çok karmaşık olmayan ve başka servislere bağımlılığı az olan mekanizmalara sahip bir yaklaşımdır. Bu servisler kendilerinin sorumlu olduğu tek bir işe odaklı ve bağımsız çalışabilen, otomatize bir deployment mekanizmasına sahip bir yapıdadır. Merkezi yönetim mekanizmalarından oldukça arındırılmış olmalıdır. Farklı programlama dillerinde geliştirilebilir ve farklı veri tabanı teknolojileri kullanılabilir.

Her bir microservice diğer hizmetler ile (loosely coupled) oldukça az bağımlılığa sahip bir şekilde çalışmaktadır. Bu hizmetler kendi kendine yeten ve tek bir işlevsellik (veya bir grup ortak işlevsellik) sunmaktadır.

Microserviceler farklı makinelerde çalışabilir ve tüm servisler birbirleriyle kendi başlarına iletişim kurabilir olmalıdır. Yeni bir servis diğer servislerde bir değişikliğe neden olmadan geliştirilebilir ve deploy edilebilir olmalıdır.
Bağımsız Deployment — Servisler birbirinden bağımsız olarak, herhangi bir platformda ayrı ayrı deploy edilebilir.

Microserviceler, otomatize bir biçimde gerekli aşamalardan geçerek (Unit Tests, Integration Tests, Sonarqube,Automation Tests) deploy edilmelidir. Bu mekanizma, projede kaliteyi artırır.

Bağımsız Geliştirme — Tüm microservice kendi işlevselliğine göre kolayca geliştirilebilir.
Hata İzolasyonu — Projenin herhangi bir servisinde oluşacak bir sorun, projenin diğer servislerini etkilemeyeceği için, sistem hala çalışmaya devam eder.
Ölçeklenebilir — Her bir bileşen kendi ihtiyacına göre ölçeklenebilir, tüm bileşenleri ölçeklendirmeye gerek yoktur.
Teknoloji Çeşitliliği — Aynı projenin farklı servislerini geliştirirken farklı diller ve teknolojiler kullanılabilir.


Tüm microserviceler birbirleriyle REST veya Message Bus üzerinden haberleşmelidir. İkisi birden de kullanılabilir. Microserviceler tarafından gerçekleştirilen tüm işlevler API Gateeway üzerinden istemcilere iletilebilir olmalıdır. Tüm iç end-pointler API Gateway’e bağlanır. Böylece, API Gateway’e bağlanan herhangi biri otomatik olarak tüm sisteme bağlanabilmelidir.



Microservicelerin Temel Özellikleri Nelerdir ?

Decoupling — Bir sistemdeki servisler büyük ölçüde birbirinden bağımsızdır.
Componentization — Microserviceler, kolayca değiştirilebilen ve versiyonları artırılabilen bağımsız bileşenlerdir.
Business Capabilities — Bir microservice basit bir yapıdadır ve tek bir göreve odaklanır.
Autonomy — Geliştiriciler ve ekipler birbirlerinden bağımsız olarak çalışabilir, böylece hızlıca geliştirme ve test süreçleri yürütülebilir.
Continuous Delivery — Yazılım geliştirme, test etme ve onaylama sistematik otomasyonu ile sık sık yazılım sürümlerini canlıya almaya otomatik bir biçimde izin verir. Servisler ayrı ayrı deploy edilebileceği için, deployment süresi kısalır ve maliyet zamanla azalır.
Decentralized Governance — Odak, doğru iş için doğru aracı kullanmaktır. Bu, standart bir teknoloji veya yapıyı zorunlu kılmadığı anlamına gelir. Geliştiriciler, sorunlarını çözmek için en iyi teknolojiyi seçme özgürlüğüne sahiptir.
Agility — Microserviceler çevikliği destekler. Herhangi bir yeni özellik hızla geliştirilip sisteme adapte edilebilir.



Mikroservis stilini açıklamaya başlamak için onu monolitik stille karşılaştırmak faydalıdır: tek bir birim olarak oluşturulmuş monolitik bir uygulama. Kurumsal Uygulamalar genellikle üç ana bölümden oluşur: istemci tarafı kullanıcı arayüzü (kullanıcının makinesindeki bir tarayıcıda çalışan HTML sayfaları ve javascript'ten oluşur), veritabanı (ortak ve genellikle ilişkisel bir veritabanı yönetim sistemine yerleştirilmiş birçok tablodan oluşur) ve sunucu tarafı uygulaması. Sunucu tarafı uygulaması HTTP isteklerini işler, etki alanı mantığını yürütür, veritabanından veri alır ve günceller ve tarayıcıya gönderilecek HTML görünümlerini seçer ve doldurur. Bu sunucu tarafı uygulaması bir monolitiktir - tek bir mantıksal yürütülebilir dosya 2. Sistemde yapılan herhangi bir değişiklik, sunucu tarafı uygulamasının yeni bir sürümünün oluşturulmasını ve dağıtılmasını içerir.



Böylesine monolitik bir sunucu, böyle bir sistem kurmanın doğal bir yoludur. Bir isteği işlemek için kullandığınız tüm mantık tek bir işlemde çalışır ve dilinizin temel özelliklerini kullanarak uygulamayı sınıflara, işlevlere ve ad alanlarına ayırmanıza olanak tanır. Biraz özenle, uygulamayı bir geliştiricinin dizüstü bilgisayarında çalıştırıp test edebilir ve değişikliklerin doğru şekilde test edilip üretime dağıtıldığından emin olmak için bir dağıtım kanalı kullanabilirsiniz. Bir yük dengeleyicinin arkasında birçok örnek çalıştırarak monolitik yapıyı yatay olarak ölçeklendirebilirsiniz.




#### Container Teknolojisi ve Docker

Microservice mimarisinde servisleri birbirinden bağımsız olması gerekir demiştik. Containerlar bu bağımsızlığı process seviyesinde sağlar. Servisleri bu containerların içine koyup birbirinden soyutlayabiliriz. Containerların içeriği kolay yedeklenip, geri yüklenebilir. Farklı containerlarda farklı kütüphane, framework sürümleri, farklı dilde yazılmış uygulamalar çalışabilir ve bunlar birbirinden bağımsızdır.


Konteynerlar, bir uygulamayı ve tüm bağımlılıklarını (kütüphaneler, çalışma ortamı vb.) tek bir pakette (image) toplayarak, herhangi bir ortamda (geliştirici makinesi, test sunucusu, production) tutarlı ve izole bir şekilde çalıştırmayı sağlayan bir teknolojidir.


Containerlar sayesinde projenin ihtiyacına göre cpu, ram gibi değerli bilgisayar bileşenlerini o servis için kısıtlayabiliriz veya arttırabiliriz. Bu işlemi sanal makineler yardımıyla da gerçekleştirebiliriz. Sanal makine bir host işletim sistemi üzerinde yeni bir işletim sistemi olarak çalışır. Docker containerları ise doğrudan host işletim sisteminin çekirdeğini kullanır. Bu durumdan dolayı aralarında büyük performans farkı ve yönetim kolaylığı vardır. Bunlardan bazıları;

- Uygulama platform fark etmeksizin sunucuda da yazılım geliştirici kişinin bilgisayarında da aynı şekilde çalışır.
- Containerların boyutu 100 Mb civarlarındayken bir sanal makinenin Gb ‘lar seviyesindedir.
- Bir sanal makinenin ayağa kalkma süresi dakikaları bulurken containerların ayağa kalkma süresi milisaniyeler mertebesindedir.
- Sanal makinenin çalışması için yüksek ram miktarı gerekir ve işgal etmiş olur bu ram sanal makine tarafından kullanılmasa da diğer bir sanal makine yada host işletim sistemi tarafından kullanılamaz.
- Containerların sanal makinelerle karşılaştırınca tek eksi yön olarak sayabileceğimiz özelliği sanal makine donanım seviyesinde izolasyon sağlarken containerlar proses seviyesinde izolasyon sağlar. Bundan dolayı sanal makine güvenlik açısından daha güvenilirdir.
- Docker, rkt, cri-o, lxd gibi çeşitli konteynır teknolojileri vardır. Ama bunlar arasında yaygın kullanılan geniş topluluk desteği ve açık kaynak kodlu olması nedeniyle docker’dır.

Docker’ın çalışma sistematiği kısaca şekildeki gibidir. Konteynırda çalıştıracağımız kendi uygulamalarımız için dockerfile yazılması gerekir. (Başka yöntemleri de bulunmaktadır.) Bu bizim için containerda çalışacak uygulamamız için image oluşturmamızı sağlar. Bu oluşturulan image aslında bizim uygulamamızın container içerisinde çalıştırılabilir halidir. Sonrasında bu image’ i containera koymamız yeterlidir.

### Docker'ın Dört Ana Bileşeni

Kapsayıcı : Kapsayıcı, bir uygulamayı ve kitaplıklar, çerçeveler ve yapılandırma dosyaları gibi tüm bağımlılıklarını içeren bağımsız bir yürütülebilir pakettir. Kapsayıcılar, birbirlerinden ve ana bilgisayar sisteminden izole edilmiştir; bu da tutarlı davranış sağlar ve farklı uygulamalar arasında çakışmaları önler.
Görüntü : Görüntü, bir konteynerin içeriğini ve yapılandırmasını tanımlayan salt okunur bir şablondur. Konteyner oluşturmak için bir şablon görevi görür ve paylaşılabilir ve sürümlenebilir. Görüntüler, temel görüntüyü, uygulama kodunu ve gerekli yapılandırmaları belirten bir Dockerfile'da sağlanan bir dizi talimattan oluşturulabilir.
Docker Motoru : Docker Motoru, konteynerleri oluşturmak, çalıştırmak ve yönetmekten sorumlu temel bileşendir. Geliştiricilerin konteynerler ve imajlarla etkileşim kurmak için kullandığı Docker daemon'ı (bir arka plan hizmeti) ve Docker CLI'dan (Komut Satırı Arayüzü) oluşur.
Kayıt Defteri : Docker görüntüleri, merkezi depolar görevi gören kayıt defterlerinde saklanabilir ve paylaşılabilir. Docker Hub, popüler bir genel kayıt defteridir; kuruluşlar ise genellikle dahili kullanım için özel kayıt defterleri oluşturur. Kayıt defterleri, görüntülerin ekipler ve ortamlar arasında kolayca dağıtılmasını sağlar.

### Docker Mimarisi
Docker, istemci-sunucu mimarisi kullanır. Docker istemcisi, Docker konteynerlerinizi oluşturma, çalıştırma ve dağıtma gibi ağır işleri yapan Docker daemon'ı ile iletişim kurar. Docker istemcisi ve daemon aynı sistemde çalışabilir veya bir Docker istemcisini uzak bir Docker daemon'ına bağlayabilirsiniz. Docker istemcisi ve daemon, bir REST API kullanarak, UNIX soketleri veya bir ağ arayüzü üzerinden iletişim kurar. Bir diğer Docker istemcisi ise konteynerlerden oluşan uygulamalarla çalışmanıza olanak tanıyan Docker Compose'dur.


Mimari, kapsayıcıları oluşturmak ve yönetmek için birlikte çalışan çeşitli bileşenlerden oluşur. Bunlar şunlardır:

Docker Daemon (Dockerd)
Docker Daemon, Docker API isteklerini dinler ve imajlar, container'lar, ağlar ve birimler gibi Docker nesnelerini yönetir.
Ana bilgisayar sistemindeki Docker kapsayıcılarını yöneten bir arka plan hizmetidir
2. Docker İstemcisi (Docker)

Docker Client, birçok Docker kullanıcısının Docker ile etkileşime girmesinin temel yoludur.
Docker komutlarını, bunları yürüten Docker Daemon'a gönderir.
Docker Client birden fazla Daemon ile iletişim kurabilir.
Kullanıcıların Docker Daemon ile etkileşime girmesini sağlayan bir CLI (Komut Satırı Arayüzü) aracıdır
3. Docker Görüntüleri

Docker Görüntüleri, kapsayıcıların içeriklerini ve yapılandırmalarını tanımlayan salt okunur şablonlardır.
Her biri belirli bir dosya sistemi değişikliğini veya yapılandırmasını temsil eden birden fazla katmandan oluşur.
Görüntüler, temel görüntüden görüntü oluşturma, dosya ekleme ve ayarları yapılandırma talimatlarını içeren Dockerfiles'tan oluşturulabilir.
4. Docker Konteynerleri

Docker konteynerları, Docker görüntülerinin çalıştırılabilir örnekleridir.
Konteynerler, bir uygulamayı ve onun bağımlılıklarını kapsülleyerek yalıtım ve tutarlılık sağlar.
Her konteynerin, diğer konteynerlerden ve ana bilgisayar sisteminden izole edilmiş kendi dosya sistemi, işlemleri ve ağ yığını vardır.
5. Docker Kayıt Defteri

Docker kayıt defteri, Docker görüntüleri için merkezi bir depodur ve kullanıcıların GitHub depolarını kullanarak kod tabanlarını paylaşmaya benzer şekilde görüntüleri depolamasına, paylaşmasına ve dağıtmasına olanak tanır.
Docker Hub popüler bir kamu kayıt defteridir ve kuruluşlar genellikle iç kullanım için özel kayıt defterleri oluştururlar.
Geliştiriciler, kayıt defterlerinden görüntüleri itebilir (yükleyebilir) ve çekebilir (indirebilir).
AWS EC2 Container Registry (ECR), Google Artifacts Registry (GCR), GitHub Package Registry, Azure Container Registry (ACR) vb. gibi başka Docker Kayıtları da mevcuttur.
6. Docker Compose

Docker Compose, tek bir yapılandırma dosyası (docker-compose.yml) kullanarak çoklu konteyner uygulamalarını tanımlamak ve çalıştırmak için kullanılan bir araçtır.
Birden fazla birbirine bağımlı konteynerin yönetimi ve yapılandırılması sürecini basitleştirir.
7. Docker Ağ Oluşturma

Docker, konteynerleri birbirine bağlamak için çeşitli ağ seçenekleri sunarak, bunların iletişim kurmasını ve veri paylaşmasını sağlar.
Ağlar, konteynerler arasında izole iletişim sağlamak veya konteynerleri ana bilgisayara veya harici ağlara bağlamak için oluşturulabilir.
8. Docker Birimleri

Docker birimleri, verileri kalıcı hale getirmek ve bunları konteynerler arasında veya bir konteyner ile ana bilgisayar sistemi arasında paylaşmak için kullanılır.
Birimler, konteynerler yok edildiğinde veya yeniden oluşturulduğunda bile verilerin korunmasını sağlar.





Mikro Hizmetler için Docker Görüntüleri Oluşturun
Mikroservis mimarisinde, bağımsız olarak dağıtılabilen ve yönetilebilen farklı servislerimiz olacak. Mikroservis mimarisine göre oluşturulmuş bir uygulamamız olduğunu varsayalım. Biri Sepeti almak, diğeri Ürünleri almak için iki servisimiz olsun.

Mikroservis 1 — Sepet Mikroservisi — Kullanıcının sepetindeki ürünlerin kimliklerini verir — Düğüm Uygulaması

Mikroservis 2- Ürün Mikroservisi — ürün kimliklerini kullanarak ürünün ayrıntılarını verir — Java Spring MVC

Sepetteki ürünün ayrıntılarını almak için sepet mikro servisi, ürün ayrıntılarını ürün mikro servisinden alır. NodeJS ve Java Spring MVC gibi farklı teknoloji yığınlarıyla iki mikro servis için Docker imajlarını nasıl oluşturabiliriz? Tek ihtiyacımız olan güçlü bir Dockerfile.






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





## KAYNAKÇA
https://martinfowler.com/articles/microservices.html?source=post_page-----948e30cf65b1---------------------------------------
https://gokhana.medium.com/microservice-mimarisi-nedir-microservice-mimarisine-giri%C5%9F-948e30cf65b1
https://kerembilim.medium.com/microservice-mimarisi-ve-docker-fb78af9d7fce
https://www.geeksforgeeks.org/system-design/how-to-design-a-microservices-architecture-with-docker-containers/
https://medium.com/@jesuva/running-microservices-as-docker-containers-9be2808f346f
https://medium.com/@jesuva/running-microservices-as-docker-containers-9be2808f346f
https://www.geeksforgeeks.org/system-design/how-to-design-a-microservices-architecture-with-docker-containers/

