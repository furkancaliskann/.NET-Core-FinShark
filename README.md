# .NET-Core-FinShark

Finshark, bir borsa uygulaması olup, kullanıcıların hisse senetleri hakkında yorum yapabilmesini sağlayan bir sistemdir.
Uygulama, iki ana tablodan oluşur: Stocks ve Comments. Kullanıcılar, belirli hisse senetlerine dair yorum yapabilir, hisse senetlerinin özelliklerini görebilir.

## Özellikler

- **Stocks Tablosu**: 
  - Firma adı, sembol, market hacmi gibi bilgilerle hisse senetlerini listeler.
  
- **Comments Tablosu**:
  - Kullanıcıların belirli hisselere yorum yapmalarını sağlar.
  
- **JWT Güvenliği**:
  - Tüm işlemler, geçerli bir token olmadan çalışmaz. Kullanıcıların kimlik doğrulaması **JWT** (JSON Web Token) ile yapılır.

- **Model Validasyonları**:
  - Veri doğrulama işlemleri yapılır. Hisse senedi ve yorum verileri için belirli kurallar uygulanır.

- **DTO'lar**:
  - Hisse senedi ekleme ve güncelleme işlemleri için farklı DTO'lar kullanılır.

## Teknolojiler

- **ASP.NET Core Web API**
- **Entity Framework Core**
- **JWT (JSON Web Token)**

**API Endpoint'leri**

GET /api/comment: Tüm yorumları listeleme.

GET /api/comment/{id}: ID'ye göre yorum getirme.

POST /api/comment{stockId}: Belirli stock id'sine göre yeni yorum oluşturma.

PUT /api/comment/{id}: Yorum güncelleme.

PATCH /api/comment/{id}: Kısmi yorum güncelleme.

DELETE /api/comment/{id}: Yorum silme.



GET /api/stock: Tüm hisseleri listeleme.

GET /api/stock/{id}: ID'ye göre hisse getirme.

POST /api/stock: Yeni hisse oluşturma.

PUT /api/stock/{id}: Hisse güncelleme.

PATCH /api/stock/{id}: Kısmi hisse güncelleme.

DELETE /api/stock/{id}: Hisse silme.


## Kurulum

1. Projeyi klonlayın:

   ```bash
   git clone https://github.com/furkancaliskann/.NET-Core-Finshark.git

2. Proje klasörüne gidin:

    ```bash
    cd .NET-Core-Finshark


3. Gerekli bağımlılıkları yükleyin:

    ```bash
    dotnet restore


4. Veritabanı bağlantısını appsettings.json dosyasındaki ConnectionStrings bölümüne uygun şekilde ayarlayın.


5. EF Core Migrations ile veritabanı oluşturun:

    ```bash
    dotnet ef database update


6. Uygulamayı başlatın:

    ```bash
    dotnet run

7. API'yi kullanmaya başlayabilirsiniz.