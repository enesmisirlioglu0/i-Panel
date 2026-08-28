# Değişiklik kaydı

Bu proje, [Keep a Changelog](https://keepachangelog.com/tr/1.1.0/) yaklaşımına yakın, kısa ve doğrulanabilir notlar tutar.

## 1.0 (Build 1) — 28 Ağustos 2026

### Eklendi

- macOS için ilk SwiftUI `MenuBarExtra` tabanlı i-Panel iskeleti
- Menü çubuğu simgesinden açılan, referans alınan kart düzenine yakın lavanta tonlu büyük panel
- CPU, bellek, disk, batarya sıcaklığı/durumu ve indirme/yükleme için beş simülasyon kartı
- 1,5 saniyelik simülasyon yenilemesi, doğrudan sürükle-bırak sıralama ve sıfırlama
- Dış tıklamada kapanan macOS popover paneli, `Ayar` düğmesi, Dock görünürlüğü tercihi ve girişte açılma isteği

### Doğrulama sınırı

- Xcode 26.6 ile imzalama kapalı Faz 1 temiz Debug derlemesi başarılı.
- Manuel menü çubuğu açılması ve sürükle-bırak etkileşimi henüz doğrulanmadı.
- Bu sürüm gerçek macOS sistem metriklerini okumaz; tüm kart değerleri simülasyondur.
- Henüz DMG veya GitHub Release yayımlanmadı.
- Girişte açılma, geçerli uygulama imzası isteyen macOS özelliğidir; imzasız paket için garanti edilmez.
