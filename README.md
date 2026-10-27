# NovaStore E-Ticaret Veri Yönetim Sistemi 🛒

Bu proje; SQL Server (T-SQL) eğitim sürecinde edinilen ilişkisel veritabanı tasarımı, tablo kısıtlamaları (Constraints), karmaşık sorgular (Complex Joins, Subqueries, Group By), View yapıları ve yedekleme (Backup) becerilerini gerçek hayat senaryosuna dayalı bir e-ticaret altyapısı üzerinde uygulamak amacıyla geliştirilmiştir.

---

## 🚀 Proje Mimarisi ve İçeriği

Proje, kurumsal standartlara uygun olarak şu ana bölümlerden oluşmaktadır:

1. **Veritabanı ve Tablo Tasarımı (`NovaStoreDB`):**
   - `Collation`: Türkçe karakter uyumu için `Turkish_CI_AS`
   - `Kategoriler (Categories)`
   - `Urunler (Products)`
   - `Musteriler (Customers)`
   - `Siparisler (Orders)`
   - `SiparisDetaylari (OrderDetails)`
   - *Not:* Identity, NOT NULL, DEFAULT değerler, UNIQUE (Email) ve Foreign Key ilişkileri eksiksiz olarak kurgulanmıştır.

2. **Örnek Veri Seti (Data Seeding):**
   - Kategoriler, ürünler, aktif müşteriler, siparişler ve sipariş detayları (`N'...'` formatıyla Türkçe karakter kaybı olmadan) sisteme eklenmiştir.

3. **Gelişmiş T-SQL Sorguları:**
   - Filtreleme ve Sıralama (`WHERE`, `ORDER BY`)
   - Tablo Birleştirme (`INNER JOIN`)
   - Zincirleme Çoklu İlişki Sorguları (`Multiple Joins`)
   - Gruplama ve Agregat Fonksiyonlar (`LEFT JOIN`, `GROUP BY`, `SUM`)
   - Tarih Fonksiyonları ve Hesaplamalar (`DATEDIFF`)

4. **Görünüm (View) ve Veritabanı Güvenliği:**
   - `vw_SiparisOzet` isimli, sipariş detaylarını müşteri ve ürün bilgileriyle birleştiren dinamik bir View.
   - SQL Server üzerinde `BACKUP DATABASE` komutu ile alınabilen tam yedekleme senaryosu.

---

## 🛠️ Kurulum ve Çalıştırma Adımları

1. SQL Server Management Studio (SSMS) uygulamasını açın.
2. `C:\Yedek\` adında bir klasör oluşturun (Backup komutunun çalışabilmesi için gereklidir).
3. `SametOzdemir_NovaStore_Proje.sql` dosyasını SSMS içerisinden açın.
4. Kod bloğunu çalıştırarak veritabanını, tabloları, verileri ve sorguları oluşturun.

---

## 📂 Dosya Yapısı

- `SametOzdemir_NovaStore_Proje.sql` -> Tüm SQL kodları (Tablolar, Insertler, Sorgular, View, Backup)
- `SametOzdemir_NovaStore_Proje.docx` -> Proje raporu ve ekran görüntüleri
- `SametOzdemir_NovaStore_Proje.png` -> Veritabanı İlişki Şeması (ER Diagram)

---
*Hazırlayan: Samet Özdemir*
