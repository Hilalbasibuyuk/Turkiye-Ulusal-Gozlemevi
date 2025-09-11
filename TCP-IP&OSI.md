# Computer Networks
## TCP(Transmisson Control Protocol)/IP (Internet Protocol)
### 3 Katmanlı iletişim


<img width="684" height="400" alt="image" src="https://github.com/user-attachments/assets/575c38de-0ba4-49fc-bb35-c75793857a05" />




TCP (Transmisson Control Protocol), TCP/IP modelinde taşıma katmanı protokollerinden birisidir ve son güncellemesi Ağustos 2022 tarihi itibariyle RFC 9293 içerisinde tanımlanmıştır. TCP kısaca , veri paketlerini toplayan ve yeniden birleştiren bileşendir diyebiliriz.
IP (Internet Protocol), internet üzerinden veri alışverişi yapılırken gerçekleşen yönlendirmenin kurallarını düzenleyen protokoldür. Kısacası yönlendirme protokolü de diyebiliriz. IP, verinin içeriğiyle yada niteliğiyle ilgilenmez sadece gideceği adresi belirler.


<img width="452" height="428" alt="image" src="https://github.com/user-attachments/assets/e8308b2a-4749-414f-a1b3-0f8f81f348d0" />

<img width="1207" height="741" alt="image" src="https://github.com/user-attachments/assets/c153204f-c2dc-4a26-a703-270d33d30183" />

#### 5 Katmanı:

- Uygulama Katmanı (Application Layer): Süreçler arası iletişim bu katmanda gerçekleşir. Bir tarafın Uygulama katmanı süreci tarafından üretilen bilgi, diğer tarafın Uygulama katmanı süreciyle iletişim kurularak iletilir. Kullanıcıya en yakın katmandır. HTTP, FTP, SMTP, DNS gibi protokoller burada çalışır. Veri bu katmanda oluşturulur. (HTTP, SMTP, FTP,SSH, Telnet)

- Taşıma Katmanı (Transport Layer): Uygulama katmanının bakımından sorumludur. Bu katmandaki mantıksal bağlantı uçtan uca olarak adlandırılır. Uygulama katmanından alınan mesaj, Taşıma katmanına gönderilir ve parçalar halinde bölünür. Mantıksal olarak, alıcı tarafın Taşıma katmanına iletilir. Diğer taraf, parçayı bir mesaja dönüştürür ve ardından bunu kendi Uygulama katmanına gönderir. Veriyi paketlere böler (segment) ve iletim kontrolünü yapar. TCP (güvenilir, sıralı) ve UDP (hızlı, güvenilmez) buradadır. (TCP, UDP)

- Network Layer : Paketlerin farklı ağlar üzerinden yönlendirilmesinden (routing) sorumludur. IP (Internet Protocol) bu katmanın temelidir. Paketlere IP adresleri ekler. Kaynak ve Hedef ana bilgisayarları arasında bağlantıyı kurmakla sorumludur. Bu katmandaki iletişime ana bilgisayarlar arası denir. Genel olarak, adresleme işleminin yani gideceği yerin IP adresinin verildiği katmandır.(IP, ICMP, Router, ARP, RARP, BOOTP)

- Ağ Erişim Katmanı (Data Link Layer): Fiziksel ağ (Ethernet, Wi-Fi) üzerinden veri çerçevelerinin (frame) nasıl gönderileceğini tanımlar. Donanıma en yakın katmandır.Ağ katmanından alınan datagramları çerçeve biçiminde hatlar arasında taşır. Kablolu veya kablosuz ethernet kartımızın MAC adresini aldığımız ve ARP protokolünün çalıştığı katman olarak bilinir.(Ethernet, Switch, SLIP, PPP)

- Fiziksel Katman(Physical Layer): Çerçeve içindeki bitleri hat boyunca iletmekten sorumludur. Diğer katmanlar gibi fiziksel katman da mantıksal bir bağlantı olarak değerlendirilebilir çünkü fiziksel katman, taşıma için bir iletim ortamı kullanır. Bu katmanda veriler, bir bilgisayara veya başka bir cihaza gönderilip okunabilecek bir şeye dönüştürülür. Örneğin, IEEE 802.3 protokolü, verileri Ethernet bağlantısında kullanılan verilere dönüştürmek için kullanılır. (Hub, Repeater, IEEE 1394, DSL, ISDN )


#### Avantajları
- Birçok Yönlendirme protokolü desteklenmektedir.
- Son derece ölçeklenebilirdir ve istemci-sunucu mimarisini kullanır.
- Hafiftir.
#### Dezavantajları
- Kurulumu biraz zor.
- Paketlerin teslimi taşıma katmanı tarafından garanti edilmez.
- Senkronizasyon saldırısına karşı savunmasız.






##### TCP/IP, "mektubun zarfı, adresi ve posta servisidir." İçeriği umursamaz, sadece doğru yere ulaştırmakla ilgilenir.



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


#### Avantajları
- Bağlantı odaklı servislerin yanı sıra bağlantısız servisler de desteklenmektedir.
- Oldukça esnektir.
- Tüm katmanlar bağımsız olarak çalışır.
#### Dezavantajları
- Bir model kurmak zorlu bir iştir.
- Bazen yeni bir protokolü bu modele uydurmak zor olabiliyor.
- Sadece referans model olarak kullanılmaktadır.




TCP/IP, belirli iletişim zorluklarını ele alan ve standartlaştırılmış protokollere dayanan pratik bir modeldir. Buna karşılık, OSI, çeşitli ağ iletişim yöntemlerini kapsayacak şekilde tasarlanmış, protokolden bağımsız, kapsamlı bir çerçeve görevi görür. Debug OSI'de daha kolaydır.

Birçok kullanıcı için, diğer tüm koşullar eşit olduğunda, OSI modeli tercih edilen seçenektir. Ağın işlevlerini daha fazla katmana ayırması, sorun gidermeyi ve ağ performansını iyileştirmeyi daha kolay hale getirir.

Ancak TCP/IP, daha fazla uygulamaya sahip olma avantajına sahiptir ve daha güncel ağ yapılarında da yaygın olarak kullanılmaktadır.


#### TCP/IP ile OSI arasındaki Farklar Nelerdir?
- OSI modelinde yedi katman varken, TCP / IP modelinde dört katman kullanılır.
- TCP/IP haberleşme görevini daha basit alt görevlere böler.Her bir alt görev diğer alt görevler için belirli servislere sunulur. OSI modeli de aynı kavramı kullanır ,ancak OSI modelinde her bir katmandaki protokollerin özellikleri ve birbiri ile ilişkileri kesin bir dille tanımlanmıştır. Bu özellik OSI modeli ile çalışmayı daha verimli kılar. TCP/IP ise böyle bir kısıtlama getirmediğinden, gerektiğinde yeni bir protokol mevcut katmanlar arasına rahatlıkla yerleştirilebilir.
- OSI modelinde gerekmeyen bir katmanın kullanılmaması gibi esnek bir yapıya izin vermez. TCP/IP ise katı kurallarla tanımlı olmadığından gereksinim duyulmayan katmanların kullanılmamasına izin verir.
- Bilgisayar ağlarında TCP / IP hala kullanılıyorken, OSI Katman modeli artık kullanılmamaktadır.
- Üst katmanların işlevselliğini tanımlamak için, OSI üç ayrı katman kullanır (uygulama, sunu ve oturum), TCP / IP ise tek katman (uygulama) kullanır.
- OSI de alt katların işlevselliğini tanımlamak için iki ayrı katman (Fiziksel ve Veri bağlantısı) kullanırken, TCP / IP de bunun için tek bir katman (Bağlantı) kullanır.
- TCP / IP modeline kıyasla, OSI modeli iyi belgelenmiştir ve standartları ve protokolleri daha ayrıntılı olarak açıklamaktadır.
- OSI modeline göre katmanların bazıları TCP/ IP modelinde birleştirilerek kolaylık sağlanır.
- TCP/IP modeli UDP bağlantıları kullandığı zaman, iletim katmanında güvenililik kontrolü yapmaz. OSI modelinde ise bu güvenlik işlemi daima yapılır.



<img width="1199" height="646" alt="image" src="https://github.com/user-attachments/assets/7aab6711-5bfb-4437-9e97-208856e041f7" />


### CİSCO Packet Tracer

Cisco Packet Tracer, ağ topolojileri oluşturmayı ve modern bilgisayar ağlarını taklit etmeyi öğretmek ve öğrenmek için kapsamlı bir ağ simülasyon yazılım aracıdır. Araç, gerçekçi simülasyon ve görselleştirme deneyimleri, değerlendirme ve etkinlik oluşturma yetenekleri ve çok kullanıcılı iş birliği ve yarışma fırsatlarının benzersiz bir kombinasyonunu sunar. Yenilikçi özellikleri, öğrencilerin ve öğretmenlerin ilgi çekici ve dinamik bir sosyal ortamda iş birliği yapmalarına, sorunları çözmelerine ve ağ kavramlarını öğrenmelerine yardımcı olur.

