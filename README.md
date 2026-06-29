# Müşteri Arşivleme Sistemi

Bu proje, Spring Boot tabanlı, JWT (JSON Web Token) ile güvenliği sağlanan, müşteri ve dosya yönetimi odaklı bir REST API uygulamasıdır

## 🛠 Kullanılan Teknolojiler
* **Java 17+**
* **Spring Boot**
* **Spring Security & JWT:** Güvenli kimlik doğrulama ve yetkilendirme.
* **Spring Data JPA:** Veritabanı işlemleri için ORM yapısı.
* **Lombok:** Kod kalabalığını azaltmak için kullanılmıştır.
* **Validation:** API isteklerinde veri doğrulaması (Jakarta Validation).
* **Swagger (OpenAPI):** API dokümantasyonu.

## 🚀 Temel Özellikler
* **Kimlik Doğrulama:** * `/register`: Kullanıcı kaydı oluşturma.
    * `/authenticate`: Giriş yapma ve JWT token alma.
    * `/refresh-token`: Süresi dolan token'ları yenileme.
* **Müşteri Yönetimi:** Müşteri ekleme, listeleme, güncelleme ve silme işlemleri.
* **Dosya Arşivleme:** Müşteriye özel dosya ekleme, listeleme, tekil görüntüleme ve silme işlemleri.
* **Hata Yönetimi:** `@ControllerAdvice` ile merkezi ve anlamlı hata mesajları.

## 🚀 Kurulum

Projeyi kendi bilgisayarınızda çalıştırmak için aşağıdaki adımları takip edebilirsiniz:

### Ön Gereksinimler
Uygulamayı derlemek ve çalıştırmak için sisteminizde şunların yüklü olması gerekir:
  - **Java 17 veya daha üstü** (JDK 17+)
  - **Maven** (Projenin bağımlılıklarını yönetmek için)
  - **Veritabanı:** Proje Spring Data JPA kullandığı için yerel bir veritabanı (PostgreSQL veya MySQL önerilir) veya test için H2 kullanabilirsiniz.

### Adım Adım Çalıştırma
  #### 1. Projeyi Klonlayın:
  ```bash
  git clone https://github.com/huriyekrtkn/customer-archiving-backend.git](https://github.com/huriyekrtkn/customer-archiving-backend.git
  ```
  #### 2. Proje dizinine gidin:
  ```bash
  cd customer-archiving-frontend
  ```
  #### 3. Veritabanı Ayarlarını Yapılandırın:
  `src/main/resources/application.properties` dosyasını açarak veritabanı bağlantı bilgilerinizi kendi yerel veritabanınıza göre güncelleyin.
  #### 4. Bağımlılıkları Yükleyin ve Derleyin:
  Proje dizininde terminali açın ve şu komutu çalıştırın:
  ```bash
  mvn clean install
  ```
  #### 5. Uygulamayı Başlatın:
  ```bash
  mvn spring-boot:run
  ```
  
## ⚙️ Yapılandırma
* **Veritabanı:** `Customer`, `CustomerFile`, `User` ve `RefreshToken` varlıkları ile çalışmaktadır.
* **Güvenlik:** `SecurityConfig` sınıfı ile Swagger yolları ve kimlik doğrulama gerektiren uç noktalar tanımlanmıştır.

## 📖 API Dokümantasyonu
Uygulama çalıştıktan sonra API uç noktalarını incelemek ve test etmek için:
`http://localhost:8080/swagger-ui.html` adresini ziyaret edebilirsiniz.