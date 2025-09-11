
## Microservice Mimarisi + Docker Konteyner Teknolojisi

<img width="903" height="559" alt="Ekran görüntüsü 2025-09-09 091725" src="https://github.com/user-attachments/assets/b3264511-5c83-485c-b70d-7781d6718542" />


# Mikroservis Mimarisi

## Mikroservis Nedir?
Mikroservis, bir uygulamayı **küçük, bağımsız ve tek sorumluluğu olan servisler** halinde geliştirme yaklaşımıdır.  
Her servis kendi veritabanına sahip olabilir ve genellikle **REST API veya mesajlaşma altyapısı** ile diğer servislerle haberleşir.  

### Temel Özellikler
- **Decoupling:** Servisler birbirinden bağımsızdır.  
- **Componentization:** Servisler kolayca değiştirilebilir, güncellenebilir.  
- **Tek işlev odaklılık:** Her servis belirli bir işlevi yerine getirir.  
- **Bağımsız geliştirme ve dağıtım:** Servisler ayrı ayrı deploy edilir.  
- **Ölçeklenebilirlik:** İhtiyaç duyulan servis ayrı ayrı ölçeklenebilir.  
- **Teknoloji çeşitliliği:** Farklı diller ve veritabanları kullanılabilir.  
- **Hata izolasyonu:** Bir servisteki sorun diğerlerini etkilemez.  

---

## Mikroservis vs. Monolitik Mimari
| Özellik | Monolitik | Mikroservis |
|---------|------------|-------------|
| **Yapı** | Tüm uygulama tek parça | Küçük, bağımsız servisler |
| **Dağıtım** | Tek deploy işlemi | Servisler ayrı ayrı deploy edilir |
| **Ölçeklenebilirlik** | Tüm sistem ölçeklenir | Sadece ihtiyaç duyulan servis ölçeklenir |
| **Teknoloji** | Tek dil/çerçeve | Farklı diller/teknolojiler kullanılabilir |
| **Hata İzolasyonu** | Bir hata tüm sistemi etkiler | Hatalar sadece ilgili servisi etkiler |

---

## Docker ve Mikroservisler
Mikroservisler genellikle **container** teknolojileri (özellikle **Docker**) ile paketlenir.  

### Docker Bileşenleri
- **Container:** Uygulama + bağımlılıkların izole paketi  
- **Image:** Container oluşturmak için kullanılan şablon  
- **Docker Engine:** Container’ları çalıştırır  
- **Registry (Docker Hub vb.):** Image’lerin depolandığı yer  
- **Docker Compose:** Çoklu container yönetim aracı  

### Avantajlar
1. **Bağımsız dağıtım:** Sadece güncellenen servis yeniden deploy edilir.  
2. **Ortam tutarlılığı:** Geliştirme, test, prod ortamları aynı olur.  
3. **Ölçeklenebilirlik:** Yük altında kalan servis ölçeklenebilir.  
4. **Teknoloji çeşitliliği:** Farklı diller ve frameworkler aynı sistemde çalışabilir.  
