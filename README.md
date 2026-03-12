# Phone--verification--system
Node.js ve Express.js ile geliştirilmiş, MySQL veritabanı kullanan, telefon numarası doğrulama ve kullanıcı kayıt işlemleri yapan mikroservis uygulaması.
Bu proje, belirli matematiksel kurallara göre telefon numarası doğrulayan,
mikroservis mimarisiyle geliştirilmiş bir web uygulamasıdır.

## Kullanılan Teknolojiler
- Node.js (Backend API)
- Express.js
- MySQL 8.0
- Docker & Docker Compose
- HTML / CSS / JavaScript (Frontend)

### Gereksinimler
- Docker Desktop
- Docker Compose

### Adımlar

1. Proje klasörüne girin:

cd project-root

//Servisleri calıstırır:
docker-compose up --build

//Servisler çalıştıktan sonra:
Frontend: http://localhost:8080
Backend API: http://localhost:3000

// API Endpointleri
1. Telefon Numarası Doğrulama
Endpoint: POST /api/phone
Örnek İstek (JSON):
{
  "phone": "222222"
}
Örnek Başarılı Yanıt:
{
  "status": "kabul edildi",
  "message": "Telefon numarası geçerli."
}
Örnek Hatalı Yanıt:
{
  "status": "red edildi",
  "message": "Telefon numarası geçersiz."
}

2. Kullanıcı Kayıt
Endpoint: POST /api/registration
Örnek İstek (JSON):
{
  "name": "Ali",
  "email": "ali@example.com",
  "phone": "222222"
}

Örnek Başarılı Yanıt:
{
  "status": "Kabul edildi",
  "message": "Kayıt başarıyla oluşturuldu."
}

3. Kayıtlı Telefon Sayısı
Endpoint: GET /api/phone
Örnek Yanıt:
{
   "message": "Bu numara zaten kayıtlı"
}


Veritabanı Bilgileri:
Veritabanı: phone_db
Tablo: registrations
Alanlar: id, name, email, phone, created_at



!!! MySQL veritabanı Docker container içinde çalışmaktadır.



