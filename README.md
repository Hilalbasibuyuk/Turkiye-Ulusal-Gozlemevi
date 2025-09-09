# Turkiye-Ulusal-Gozlemevi

### 3 Katmanlı iletişim


<img width="684" height="400" alt="image" src="https://github.com/user-attachments/assets/575c38de-0ba4-49fc-bb35-c75793857a05" />



## TCP/IP Protocol


<img width="642" height="845" alt="image" src="https://github.com/user-attachments/assets/a4129432-5ce1-46af-9e40-2bff69850696" />


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

It has a layered architecture. In the TCP/IP model, Session and Presentation layers are 
integrated with the Application layer.

## Microservice

<img width="903" height="559" alt="Ekran görüntüsü 2025-09-09 091725" src="https://github.com/user-attachments/assets/b3264511-5c83-485c-b70d-7781d6718542" />
