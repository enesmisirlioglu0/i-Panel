# Değişiklik kaydı

Bu proje, [Keep a Changelog](https://keepachangelog.com/tr/1.1.0/) yaklaşımına yakın, kısa ve doğrulanabilir notlar tutar.

## 1.2 (Build 3) — 28 Ağustos 2026

### Eklendi

- Finder, DMG ve GitHub görünümü için kırmızı, mavi ve yeşil üç karttan oluşan i-Panel uygulama ikonu
- Apple Silicon ve Intel Mac'ler için tek imzasız universal DMG
- DMG bütünlüğünü kontrol etmek için SHA-256 dosyası

### Değiştirildi

- Menü çubuğu uygulaması `MenuBarExtra(.window)` yapısına geçirildi; görünürlük için macOS'un kendi tek renkli üçlü-kart sembolü kullanılıyor.
- Kart sıralama doğrudan yerel sürükleme hareketiyle güvenilir hâle getirildi.
- `Sıfırla`, yalnız gösterge çubuklarını değil kart sırasını gerçekten varsayılan düzene döndürüyor.
- DMG dosya adına pazarlama sürümünün yanında build numarası da eklendi.

### Doğrulama sınırı

- Geliştirici Mac'inde menü simgesi/panel, `Ayar`, `Sıfırla` ve sürükle-bırak kabul testleri tamamlandı.
- Universal Release derlemesi başarılı; DMG `hdiutil verify` ile doğrulandı ve içeriğinde `i-Panel.app` ile `Applications` bağlantısı görüldü.
- Paket kasıtlı olarak imzasız ve noterlenmemiştir; ilk açılışta Gatekeeper uyarısı beklenir.
- Kartlardaki sistem değerleri hâlâ simülasyondur; gerçek macOS metrikleri okunmaz.

## 1.1 (Build 2) — 28 Ağustos 2026

### Eklendi

- Ayarlardan seçilebilen 1 / 3 / 5 saniyelik simülasyon yenileme aralığı
- Sürükle-bırakla seçilen kart sırasının cihazda yerel olarak saklanması

### Değiştirildi

- Menü çubuğu paneli, sabit 336 × 532 pt ölçüde daha kompakt turkuaz düzene taşındı.
- Alt sağdaki `Ayar` ve `Sıfırla` denetimleri daha okunaklı düğmelere dönüştürüldü.

## 1.0 (Build 1) — 28 Ağustos 2026

### Eklendi

- macOS için ilk menü çubuğu tabanlı i-Panel iskeleti
- Menü çubuğu simgesinden açılan, referans alınan kart düzenine yakın ilk panel
- CPU, bellek, disk, batarya sıcaklığı/durumu ve indirme/yükleme için beş simülasyon kartı
