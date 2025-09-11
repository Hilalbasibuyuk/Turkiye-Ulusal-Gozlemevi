












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

