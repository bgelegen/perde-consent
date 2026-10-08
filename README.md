# Perde

Çerez onayı ve gizlilik denetimi yapan bir SaaS ürününün tanıtım sitesi. Ders projesi olarak hazırlandı.

Bölüm yapısı ve görsel dili [inth.com](https://inth.com) örnek alınarak kuruldu. Metinler, marka, logo ve müşteri adları projeye özgüdür. Hız karşılaştırmasındaki sayılar örnek veridir; hiçbir gerçek ürünün ölçümü değildir.

## Sayfalar

| Dosya | İçerik |
|---|---|
| `index.html` | Tanıtım sayfası (İngilizce): hero, onay paneli, özellikler, analitik paneli, hız karşılaştırması, entegrasyonlar, kod örneği, uyum araçları, SSS, altbilgi |
| `tarama.html` | Çalışan araç (Türkçe): HTML kaynağı veya HAR ağ kaydından gizlilik taraması ve KVKK uyumlu çerez onay banner'ı oluşturucu |

## Çalıştırma

Derleme adımı yok. `index.html` dosyasını tarayıcıda açmanız yeterli.

GitHub Pages ile yayınlamak için: **Settings → Pages → Branch: `main` / `(root)`**.

## Tarama aracı ne yapar?

- Onay alınmadan çalışan analitik, reklam ve oturum kaydı betiklerini bulur (50+ hizmet tanınır).
- Çerez onay aracını (Cookiebot, OneTrust, Usercentrics ve diğerleri) tespit eder.
- Üçüncü taraflara giden e-posta, cep telefonu ve sağlama toplamı doğrulanmış TC kimlik numarasını yakalar.
- HAR kaydından çerezleri, sağlayıcılarını ve ömürlerini listeler.
- Her bulguyu kanıtı, düzeltme yolu ve ilgili KVKK maddesiyle raporlar.

Tarama tamamen tarayıcıda çalışır; yapıştırılan kod ve yüklenen dosya hiçbir sunucuya gönderilmez.

## Banner oluşturucu

Bölge kuralı (KVKK, GDPR, CCPA), konum, tema, renk ve kategoriler seçilir; önizlemede denenir. Üretilen kod `<head>` içine eklenir ve `type="text/plain" data-perde="analytics"` ile işaretlenen betikleri yalnızca ilgili kategoriye onay verildiğinde çalıştırır. Google Consent Mode v2 ve Global Privacy Control desteği vardır.

## Not

Bu proje hukuki görüş yerine geçmez.
