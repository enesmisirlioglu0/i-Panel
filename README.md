# i-Panel

i-Panel, Mac'in menü çubuğunda çalışan küçük bir durum göstergesi ve hızlı kontrol panelidir.

## Durum

- Sürüm: `1.0 (Build 1)`
- Platform: macOS 13 ve sonrası
- Uygulama modeli: SwiftUI `MenuBarExtra`
- Derleme doğrulaması: 28 Ağustos 2026'da Xcode 26.6 ile temiz Debug derlemesi başarılı
- Manuel menü çubuğu etkileşim testi: Henüz yapılmadı
- Dağıtım: TestFlight veya App Store sürümü değildir.

## Nedir?

i-Panel, üst sağdaki Denetim Merkezi alanının yanında çalışan kendi menü çubuğu göstergesini ve küçük bir kontrol penceresini sunar. Apple'ın kendi Denetim Merkezi içine üçüncü taraf modül eklemek için genel kullanıma açık bir API'si yoktur; proje bu nedenle desteklenen `MenuBarExtra` yaklaşımını kullanır.

## İlk doğrulanmış temel

- Menü çubuğunda i-Panel göstergesi
- Açılır küçük kontrol penceresi
- Odak modu, tasarruf modu ve panel seviyesi için yerel önizleme kontrolleri
- Son yenileme zamanını gösteren durum alanı

İlk kontroller macOS sistem ayarlarını değiştirmez, sistem verisi toplamaz, ağa bağlanmaz ve bulut hesabı kullanmaz.

## Depo sınırı

Bu açık depo yalnızca i-Panel belgelerini, yol haritasını ve değişiklik kaydını içerir. Swift/Xcode kaynak kodu ve olası hassas yapılandırmalar özel kaynak deposunda tutulur.

## Belgeler

- [Değişiklik kaydı](CHANGELOG.md)
- [Yol haritası](ROADMAP.md)
