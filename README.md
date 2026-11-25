# BURAK ERP

Alpin Endüstriyel Mutfak – Memorial sipariş ve fatura takibi.

- Arayüz: tek sayfa (`index.html`), GitHub Pages'te yayınlanır.
- Veritabanı: Supabase projesi `burak-erp` (eu-central-1).
- Giriş: Supabase Auth (e-posta + şifre). Verilere yalnızca `allowed_users` tablosundaki e-postalar erişebilir (RLS).
- Sayfadaki anahtar Supabase'in "publishable" anahtarıdır; tarayıcıda görünmesi normaldir, yetki RLS ile korunur.

## Sekmeler
Özet · Teslim edilenler · Kısmi teslim · Açık siparişler (GLF / İstanbul Kahve filtresi) · Açık ürünler · Tüm siparişler · Faturalar · Kontrol

## Veri akışı
- Memorial SAS sipariş formları: webmail'den günde 2 kez (07:39 ve 19:39) otomatik çekilir ve Supabase'e yazılır.
- EDM e-faturaları (gelen/giden XML): elle yüklenir.
