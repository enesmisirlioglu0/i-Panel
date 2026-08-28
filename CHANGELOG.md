# Değişiklik kaydı

Bu proje, [Keep a Changelog](https://keepachangelog.com/tr/1.1.0/) yaklaşımına yakın, kısa ve doğrulanabilir notlar tutar.

## 1.3 (Build 4) — 28 Ağustos 2026

### Eklendi

- CPU, bellek, başlangıç diski, batarya doluluk/durumu ve Mac toplam ağ hızı için gerçek, yerel macOS metrik sağlayıcısı
- Disk alanı ve yerel tercihler için şeffaflık sağlayan `PrivacyInfo.xcprivacy` bildirimi

### Değiştirildi

- Simülasyon üreten tüm kart değerleri kaldırıldı; yenileme düğmesi artık gerçek sistem verilerini örnekliyor.
- Bellek ve disk kartları artık sabit kapasiteler yerine gerçek kullanılan/toplam kapasiteyi gösteriyor.
- Batarya kartından sıcaklık alanı çıkarıldı; yalnız güvenilir doluluk ve güç durumu gösteriliyor.
- Ağ kartı artık uygulama trafiği değil, Mac'in toplam indirme/yükleme hızını gösteriyor.

### Doğrulama sınırı

- Debug ve imzasız universal Release derlemeleri başarılı oldu.
- Geliştirici Mac'inde iki ardışık örnekle CPU, bellek, disk, batarya ve ağ metrikleri gerçek public macOS API'lerinden alındı.
- `i-Panel-1.3-build-4-unsigned.dmg`, `hdiutil verify` ile doğrulandı; pakette `1.3 (Build 4)`, `arm64` + `x86_64` ikilisi ve `PrivacyInfo.xcprivacy` denetlendi.
- Paket kasıtlı olarak imzasız ve noterlenmemiştir; ilk açılışta Gatekeeper uyarısı beklenir.

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
