
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
