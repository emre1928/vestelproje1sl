Çalışan Yönetim Sistemi
Bu proje, ASP.NET Core ile geliştirilmiş bir Çalışan Yönetim Sistemidir. Çalışan verilerini yönetmek için RESTful API sağlar ve JWT token'ları kullanarak kimlik doğrulama içerir.
Özellikler

Çalışan yönetimi için CRUD işlemleri
Kullanıcı kimlik doğrulama ve yetkilendirme
Rol tabanlı erişim kontrolü
Hizmet yılına göre maaş hesaplama
API dokümantasyonu ve testi için Swagger UI

Kullanılan Teknolojiler

ASP.NET Core 6.0
Entity Framework Core (gösterim amaçlı InMemory provider ile)
Kimlik doğrulama için JWT
Swagger / OpenAPI

Başlangıç
Ön Koşullar

.NET 6.0 SDK
Visual Studio 2022 veya Visual Studio Code

Uygulamayı Çalıştırma

Depoyu klonlayın
Çözümü Visual Studio'da veya proje klasörünü Visual Studio Code'da açın
Terminal'de aşağıdaki komutları çalıştırın:
Copydotnet restore
dotnet run

Uygulama https://localhost:5001 ve http://localhost:5000 adreslerinde çalışmaya başlayacak

API Dokümantasyonu
Uygulama çalışır durumda olduğunda, Swagger UI'ya şu adresten erişebilirsiniz:
Copyhttps://localhost:5001/swagger
Bu, tüm mevcut endpoints'lerin detaylı bir görünümünü sağlar ve doğrudan tarayıcıdan test etmenize olanak tanır.
API Endpoints

POST /api/Auth/login: Bir kullanıcıyı doğrula ve JWT token al
GET /api/Employees: Tüm çalışanları getir (kimlik doğrulama gerektirir)
GET /api/Employees/{id}: ID'ye göre belirli bir çalışanı getir (kimlik doğrulama gerektirir)
POST /api/Employees: Yeni bir çalışan oluştur (Admin rolü gerektirir)
PUT /api/Employees/{id}: Mevcut bir çalışanı güncelle (Admin rolü gerektirir)
DELETE /api/Employees/{id}: Bir çalışanı sil (Admin rolü gerektirir)
GET /api/Employees/{id}/salary: Bir çalışanın maaşını hesapla (kimlik doğrulama gerektirir)
