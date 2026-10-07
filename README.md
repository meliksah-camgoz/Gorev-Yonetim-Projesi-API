# 📋 Görev Yönetim Sistemi

Görev Yönetim Sistemi, yazılım şirketleri içerisinde çalışanların görevlerini, sorumluluklarını ve görev durumlarını takip etmek amacıyla geliştirilmiş modern bir web uygulamasıdır.

Proje; görev oluşturma, görevleri çalışanlara atama, görev durumlarını takip etme, önceliklendirme, görevleri güncelleme ve silme gibi temel görev yönetimi işlemlerini desteklemektedir.

---

## 🎯 Projenin Amacı

Bir yazılım şirketinde aynı anda birden fazla proje yürütülebilir ve farklı çalışanlara çeşitli görevler atanabilir.

Bu proje ile görevlerin merkezi bir sistem üzerinden yönetilmesi ve çalışanların sorumluluklarının daha düzenli şekilde takip edilmesi amaçlanmıştır.

Sistem sayesinde;

- Yeni görevler oluşturulabilir.
- Mevcut görevler görüntülenebilir.
- Görev detayları incelenebilir.
- Görevler çalışanlara atanabilir.
- Görev durumları güncellenebilir.
- Görev öncelikleri belirlenebilir.
- Görevler düzenlenebilir.
- Görevler silinebilir.
- Çalışanlar ve görevler arasındaki ilişkiler yönetilebilir.

---

# 🚀 Temel Özellikler

### 📌 Görev Yönetimi

Sistem üzerinden görevlerin temel CRUD işlemleri gerçekleştirilebilir:

- Görev oluşturma
- Görev listeleme
- Görev detaylarını görüntüleme
- Görev güncelleme
- Görev silme

### 👥 Çalışan Yönetimi

Görevler sistemde bulunan çalışanlara atanabilir.

Bir çalışan birden fazla göreve sahip olabilir.

### 📊 Görev Durumları

Görevlerin mevcut durumları takip edilebilir:

| Durum | Açıklama |
|---|---|
| `pending` | Bekliyor |
| `in_progress` | Devam ediyor |
| `completed` | Tamamlandı |

### 🔥 Görev Öncelikleri

Görevlerin öncelik seviyeleri belirlenebilir:

| Öncelik | Açıklama |
|---|---|
| `low` | Düşük |
| `medium` | Orta |
| `high` | Yüksek |

---

# 🛠️ Kullanılan Teknolojiler

| Teknoloji | Kullanım Alanı |
|---|---|
| **Next.js** | Web uygulaması altyapısı |
| **React** | Kullanıcı arayüzü |
| **TypeScript** | Tip güvenli geliştirme |
| **Prisma** | ORM ve veritabanı işlemleri |
| **MySQL** | Veritabanı |
| **Tailwind CSS** | Kullanıcı arayüzü ve stillendirme |
| **Node.js** | JavaScript çalışma ortamı |
| **npm** | Paket yönetimi |
| **ESLint** | Kod kalitesi ve lint kontrolü |
| **Git / GitHub** | Versiyon kontrolü |

---

# 📁 Proje Yapısı

Proje Next.js App Router mimarisi kullanılarak yapılandırılmıştır.

```text
gorev-yonetim-main/
│
├── prisma/
│   └── schema.prisma
│
├── public/
│
├── src/
│   ├── app/
│   ├── components/
│   ├── lib/
│   └── ...
│
├── .gitignore
├── eslint.config.mjs
├── next.config.ts
├── package.json
├── package-lock.json
├── postcss.config.mjs
├── README.md
├── sentry.edge.config.ts
├── sentry.server.config.ts
├── tsconfig.json
└── ...
```

> Proje yapısındaki klasör ve dosyalar kullanılan Next.js, Prisma ve diğer geliştirme araçlarının yapılandırmasına göre oluşturulmuştur.

---

# ⚙️ Gereksinimler

Projeyi çalıştırmadan önce bilgisayarınızda aşağıdaki yazılımların kurulu olması gerekir:

- Node.js
- npm
- MySQL
- Git

Kurulumları kontrol etmek için:

### Node.js

```bash
node -v
```

### npm

```bash
npm -v
```

### Git

```bash
git --version
```

---

# 📥 Projeyi GitHub'dan Klonlama

Projeyi bilgisayarınıza almak için terminal veya PowerShell açın.

```bash
git clone <REPOSITORY_URL>
```

Daha sonra proje klasörüne girin:

```bash
cd Gorev-Yonetim-Projesi-API
```

> Repository adresini kendi GitHub repository adresiniz ile değiştirebilirsiniz.

---

# 📦 Bağımlılıkların Kurulması

Proje klasörünün içerisinde terminal açın ve:

```bash
npm install
```

komutunu çalıştırın.

Bu komut `package.json` içerisinde bulunan tüm gerekli bağımlılıkları yükler.

Kurulum tamamlandığında proje içerisinde:

```text
node_modules/
```

klasörü oluşacaktır.

Bu klasör GitHub'a gönderilmemektedir.

---

# 🗄️ MySQL Veritabanı Kurulumu

Projenin çalışabilmesi için bilgisayarınızda MySQL Server'ın çalışıyor olması gerekir.

MySQL Workbench, MySQL Command Line veya kullandığınız başka bir MySQL aracı üzerinden yeni bir veritabanı oluşturabilirsiniz.

Örneğin:

```sql
CREATE DATABASE gorev_yonetim;
```

Daha sonra:

```sql
USE gorev_yonetim;
```

komutu ile veritabanını seçebilirsiniz.

> Kullanılacak veritabanı adı `.env` içerisindeki `DATABASE_URL` ile uyumlu olmalıdır.

---

# 🔐 Environment Variables

Projenin ana dizininde `.env` isimli bir dosya oluşturun.

Proje yapısı:

```text
gorev-yonetim-main/
│
├── .env
├── package.json
├── prisma/
└── src/
```

`.env` dosyası içerisine veritabanı bağlantı bilgilerini ekleyin:

```env
DATABASE_URL="mysql://USERNAME:PASSWORD@localhost:3306/gorev_yonetim"
```

Örneğin MySQL kullanıcı adı `root` ve şifre `123456` ise:

```env
DATABASE_URL="mysql://root:123456@localhost:3306/gorev_yonetim"
```

Kendi MySQL kullanıcı adı, şifre ve veritabanı bilgilerinize göre bu alanları değiştirmelisiniz.

---

# ⚠️ .env Güvenliği

`.env` dosyası içerisinde veritabanı kullanıcı adı ve şifresi bulunabileceği için bu dosya GitHub'a gönderilmemelidir.

`.gitignore` dosyasında aşağıdaki satırların bulunması gerekir:

```gitignore
.env
.env.local
.env.development.local
.env.test.local
.env.production.local
```

Gerçek `.env` dosyası yerine isterseniz:

```text
.env.example
```

dosyası oluşturabilirsiniz.

Örneğin:

```env
DATABASE_URL="mysql://USERNAME:PASSWORD@localhost:3306/DATABASE_NAME"
```

Bu şekilde diğer geliştiriciler hangi environment değişkenlerinin gerekli olduğunu görebilir.

---

# 🔄 Prisma Kurulumu

Proje veritabanı işlemleri için Prisma ORM kullanmaktadır.

Bağımlılıkların kurulmasından sonra Prisma Client'ı oluşturmak için:

```bash
npx prisma generate
```

komutunu çalıştırın.

---

# 🧬 Prisma Migration

Veritabanı tablolarını oluşturmak ve Prisma schema'sını veritabanına uygulamak için:

```bash
npx prisma migrate dev
```

komutunu kullanabilirsiniz.

Yeni bir veritabanı değişikliği yaptığınızda migration oluşturmak için:

```bash
npx prisma migrate dev --name update_database
```

Örneğin görev tablosuna yeni bir alan eklendiğinde:

```bash
npx prisma migrate dev --name add_task_field
```

şeklinde migration oluşturulabilir.

Migration dosyaları:

```text
prisma/migrations/
```

klasöründe tutulmaktadır.

> `prisma/schema.prisma` ve migration dosyaları GitHub'a gönderilmelidir. `prisma/` klasörünün tamamı `.gitignore` içerisine eklenmemelidir.

---

# 🗃️ Prisma Studio

Veritabanındaki tabloları ve kayıtları görsel olarak incelemek için Prisma Studio kullanılabilir.

```bash
npx prisma studio
```

komutunu çalıştırdıktan sonra Prisma Studio açılır.

Buradan geliştirme ortamında veritabanındaki kayıtlar görüntülenebilir.

---

# ▶️ Projeyi Çalıştırma

Tüm kurulum işlemleri tamamlandıktan sonra geliştirme sunucusunu başlatmak için:

```bash
npm run dev
```

komutunu çalıştırın.

Başarılı bir şekilde çalıştığında terminalde buna benzer bir çıktı görülür:

```text
Local: http://localhost:3000
```

Uygulamayı tarayıcıdan açmak için:

```text
http://localhost:3000
```

adresine gidin.

---

# 🏗️ Production Build

Production build oluşturmak için:

```bash
npm run build
```

komutunu çalıştırabilirsiniz.

Build başarılı olduktan sonra production sunucusunu başlatmak için:

```bash
npm start
```

kullanılabilir.

---

# 🧪 Kod Kontrolü

Projede ESLint kullanılmaktadır.

Kod kontrolü yapmak için:

```bash
npm run lint
```

komutunu çalıştırabilirsiniz.

Bu işlem projedeki kodların belirlenen lint kurallarına uygunluğunu kontrol eder.

---

# 📋 Görev Veri Yapısı

Görevler temel olarak aşağıdaki bilgileri içermektedir:

- Görev ID
- Görev başlığı
- Görev açıklaması
- Atanan çalışan
- Görev durumu
- Görev önceliği
- Oluşturulma tarihi
- Güncellenme tarihi

Görev ve çalışan arasındaki ilişki Prisma üzerinden yönetilmektedir.

Genel ilişki:

```text
Çalışan
   │
   │ 1
   │
   │
   │ N
   ▼
Görev
```

Bir çalışan birden fazla göreve atanabilir.

---

# 🔄 Görev İş Akışı

Görevlerin temel iş akışı:

```text
Yeni Görev
    │
    ▼
 Pending
    │
    ▼
 In Progress
    │
    ▼
 Completed
```

Bu yapı sayesinde görevlerin hangi aşamada olduğu takip edilebilir.

---

# 🧪 Test Süreci

Projenin geliştirilmesi sırasında temel görev işlemleri test edilmiştir.

Test kapsamında:

- Görev oluşturma
- Görev listeleme
- Görev detaylarını görüntüleme
- Görev güncelleme
- Görev silme
- Görev durumunu değiştirme
- Görev önceliğini değiştirme
- Görevi çalışana atama

işlemleri kontrol edilmiştir.

---

# 🔍 Test Senaryoları

### 1. Görev Oluşturma

Yeni bir görev oluşturulur.

```text
Başlık
Açıklama
Çalışan
Durum
Öncelik
```

bilgileri girilir ve kayıt oluşturulur.

### 2. Görev Listeleme

Sistemde bulunan görevler listelenir.

### 3. Görev Detayı

Seçilen görevin detayları görüntülenir.

### 4. Görev Güncelleme

Mevcut görevin bilgileri değiştirilir.

### 5. Görev Silme

Artık kullanılmayan görev sistemden kaldırılır.

---

# 🧹 Git ve GitHub Kullanımı

Projede versiyon kontrolü için Git kullanılmaktadır.

Değişiklikleri Git'e eklemek için:

```bash
git add .
```

Commit oluşturmak için:

```bash
git commit -m "Yapılan değişiklik"
```

GitHub'a göndermek için:

```bash
git push
```

Örneğin:

```bash
git add .
git commit -m "Update task management"
git push
```

---

# 🚫 GitHub'a Gönderilmemesi Gereken Dosyalar

Aşağıdaki dosya ve klasörler repository'ye gönderilmemelidir:

```text
node_modules/
.next/
.env
.env.local
.vercel/
*.log
```

Özellikle `.env` dosyasının GitHub'a gönderilmemesi önemlidir.

Çünkü bu dosya veritabanı bağlantı bilgileri gibi hassas bilgiler içerebilir.

---

# 📌 Kurulumun Kısa Özeti

Projeyi ilk kez kuracak bir geliştirici için temel kurulum sırası:

```bash
# 1. Repository'yi klonla
git clone <REPOSITORY_URL>

# 2. Proje klasörüne gir
cd Gorev-Yonetim-Projesi-API

# 3. Paketleri yükle
npm install

# 4. .env dosyasını oluştur
# DATABASE_URL değerini kendi MySQL bilgilerinle doldur

# 5. Prisma Client oluştur
npx prisma generate

# 6. Veritabanı migrationlarını çalıştır
npx prisma migrate dev

# 7. Geliştirme sunucusunu başlat
npm run dev
```

Ardından tarayıcıdan:

```text
http://localhost:3000
```

adresine gidilebilir.

---

# 🛠️ Geliştirme Ortamı

Geliştirme sırasında:

```bash
npm run dev
```

komutu kullanılmalıdır.

Next.js geliştirme sunucusu çalışırken yapılan değişiklikler otomatik olarak algılanır ve uygulama güncellenir.

---

# 📈 Gelecekte Eklenebilecek Özellikler

Proje ilerleyen aşamalarda aşağıdaki özelliklerle geliştirilebilir:

- Kullanıcı giriş sistemi
- Yetkilendirme ve rol yönetimi
- Admin paneli
- Gelişmiş görev filtreleme
- Görev arama
- Son tarih ve hatırlatıcı sistemi
- E-posta bildirimleri
- Dashboard ve grafikler
- Proje bazlı görev gruplandırma
- Görev yorumları
- Dosya ekleme
- Aktivite geçmişi
- Detaylı raporlama

---

# 👨‍💻 Geliştirici

**Melikşah Camgöz**

Computer Technology and Information Systems

Backend / Full Stack Development

---

# 📄 Proje Bilgisi

Bu proje, Node.js / backend ve web geliştirme eğitimi kapsamında görev yönetimi senaryosunun uygulanması amacıyla geliştirilmiştir.

Projenin temel amacı modern web teknolojileri kullanılarak görevlerin ve çalışan sorumluluklarının merkezi bir sistem üzerinden yönetilmesini sağlamaktır.

---

## ⭐ Projeyi Çalıştırmak İçin

Kısaca:

```bash
npm install
npx prisma generate
npx prisma migrate dev
npm run dev
```

Ardından:

```text
http://localhost:3000
```

adresini açabilirsiniz.
