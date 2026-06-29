# Müşteri Arşivleme Sistemi

[cite_start]Bu proje, Spring Boot tabanlı, JWT (JSON Web Token) ile güvenliği sağlanan, müşteri ve dosya yönetimi odaklı bir REST API uygulamasıdır[cite: 16, 61, 107].

## 🛠 Kullanılan Teknolojiler
* **Java 17+**
* **Spring Boot**
* [cite_start]**Spring Security & JWT:** Güvenli kimlik doğrulama ve yetkilendirme[cite: 56, 1144].
* [cite_start]**Spring Data JPA:** Veritabanı işlemleri için ORM yapısı[cite: 614, 621, 629].
* [cite_start]**Lombok:** Kod kalabalığını azaltmak için kullanılmıştır[cite: 264, 400, 425].
* [cite_start]**Validation:** API isteklerinde veri doğrulaması (Jakarta Validation)[cite: 125, 198].
* [cite_start]**Swagger (OpenAPI):** API dokümantasyonu[cite: 105, 107].

## 🚀 Temel Özellikler
* [cite_start]**Kimlik Doğrulama:** * `/register`: Kullanıcı kaydı oluşturma[cite: 136].
    * [cite_start]`/authenticate`: Giriş yapma ve JWT token alma[cite: 141].
    * [cite_start]`/refresh-token`: Süresi dolan token'ları yenileme[cite: 146, 1034].
* [cite_start]**Müşteri Yönetimi:** Müşteri ekleme, listeleme, güncelleme ve silme işlemleri[cite: 166, 171, 176, 181, 187].
* [cite_start]**Dosya Arşivleme:** Müşteriye özel dosya ekleme, listeleme, tekil görüntüleme ve silme işlemleri[cite: 207, 212, 217, 222, 228].
* [cite_start]**Hata Yönetimi:** `@ControllerAdvice` ile merkezi ve anlamlı hata mesajları[cite: 543, 544].

## 🚀 Kurulum

Projeyi kendi bilgisayarınızda çalıştırmak için aşağıdaki adımları takip edebilirsiniz:

* Ön Gereksinimler
Uygulamayı derlemek ve çalıştırmak için sisteminizde şunların yüklü olması gerekir:
  - **Java 17 veya daha üstü** (JDK 17+)
  - **Maven** (Projenin bağımlılıklarını yönetmek için)
  - **Veritabanı:** Proje Spring Data JPA kullandığı için yerel bir veritabanı (PostgreSQL veya MySQL önerilir) veya test için H2 kullanabilirsiniz.

* Adım Adım Çalıştırma

### 1. Projeyi Klonlayın:
  ```bash
  git clone https://github.com/huriyekrtkn/customer-archiving-backend.git](https://github.com/huriyekrtkn/customer-archiving-backend.git
  ```
### 2. Proje dizinine gidin:
  ```bash
  cd customer-archiving-frontend
  ```
### 3. Veritabanı Ayarlarını Yapılandırın:
  src/main/resources/application.properties (veya application.yml) dosyasını açarak veritabanı bağlantı bilgilerinizi kendi yerel veritabanınıza göre güncelleyin.
### 4. Bağımlılıkları Yükleyin ve Derleyin:
  Proje dizininde terminali açın ve şu komutu çalıştırın:
  ```bash
  mvn clean install
  ```
### 5. Uygulamayı Başlatın:
  ```bash
  mvn spring-boot:run
  ```
### 6. API Testi:
  Uygulama ayağa kalktıktan sonra tarayıcınızdan şu adrese giderek Swagger dokümantasyonuna ulaşabilir ve API uç noktalarını test edebilirsiniz:
  http://localhost:8080/swagger-ui.html

## ⚙️ Yapılandırma
* [cite_start]**Veritabanı:** `Customer`, `CustomerFile`, `User` ve `RefreshToken` varlıkları ile çalışmaktadır[cite: 404, 435, 461, 489].
* [cite_start]**Güvenlik:** `SecurityConfig` sınıfı ile Swagger yolları ve kimlik doğrulama gerektiren uç noktalar tanımlanmıştır[cite: 62, 87].

## 📖 API Dokümantasyonu
Uygulama çalıştıktan sonra API uç noktalarını incelemek ve test etmek için:
[cite_start]`http://localhost:8080/swagger-ui.html` adresini ziyaret edebilirsiniz[cite: 109].