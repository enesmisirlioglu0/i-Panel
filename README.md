# i-Panel

i-Panel, Mac'in menü çubuğunda çalışan küçük bir durum göstergesi ve hızlı kontrol panelidir.

## Durum

- Sürüm: `1.1 (Build 2)`
- Platform: macOS 13 ve sonrası
- Uygulama modeli: SwiftUI + AppKit `NSStatusItem` ve geçici `NSPopover`
- Derleme doğrulaması: 28 Ağustos 2026'da Xcode 26.6 ile Faz 1 temiz Debug derlemesi başarılı
- Manuel menü çubuğu etkileşim testi: Henüz yapılmadı
- Dağıtım: Henüz indirilebilir DMG veya GitHub Release yoktur.

## Nedir?

i-Panel, üst sağdaki Denetim Merkezi alanının yanında çalışan kendi menü çubuğu göstergesini ve küçük bir kontrol penceresini sunar. Apple'ın kendi Denetim Merkezi içine üçüncü taraf modül eklemek için genel kullanıma açık bir API'si yoktur; proje bu nedenle yerel `NSStatusItem` ve geçici `NSPopover` yaklaşımını kullanır.

## Faz 1: simülasyon paneli

- Menü çubuğunda i-Panel göstergesi
- Sağ üst simgeye bağlı, turkuaz tonlu büyük açılır panel
- CPU, bellek, disk, batarya sıcaklığı/durumu ve anlık indirme/yükleme için beş kart
- Ayarlardan seçilen 1 / 3 / 5 saniyelik yenileme aralığıyla güncellenen, inandırıcı fakat tamamen simüle edilmiş değerler
- Kartların yerini her an doğrudan sürükle-bırak yöntemiyle değiştirme, sırayı yerelde hatırlama ve varsayılan sıraya dönme
- Alt sağda `Ayar` ve `Sıfırla` denetimleri
- Panel dışındaki bir arayüz öğesine tıklanınca otomatik kapanan yerel macOS popover davranışı
- Ayarlardan kalıcı Dock simgesi görünürlüğü, macOS girişinde açılma isteği, kart sırasını hatırlama ve yenileme sıklığı

Bu faz gerçek CPU/bellek/disk/batarya/ağ verisi toplamaz, ağa bağlanmaz ve bulut hesabı kullanmaz. Kart sırası, yenileme tercihi ve Dock görünürlüğü yalnız cihazdaki yerel tercih olarak saklanır; yeni bir gizlilik veya yönetici izni istenmez. Girişte açılma isteği yalnız kullanıcı ayarı açtığında macOS'a gönderilir.

### Başlangıçta açılma sınırı

Girişte açılma ayarı macOS 13+'ta `SMAppService.mainApp` kullanır. Apple bu kayıt için geçerli uygulama imzası ister; bu nedenle tamamen imzasız Debug/DMG paketi ayarı hata veya kullanılamaz olarak gösterebilir. İmzalı bir geliştirme paketiyle doğrulanmadan imzasız public DMG için bu özellik vaat edilmez.

## Dağıtım hedefi

Proje tamamlandığında GitHub Releases üzerinden indirilebilen **imzasız** bir `.dmg` hazırlanması hedeflenir. İlk paket Developer ID ile imzalanmış veya noterlenmiş olmayacaktır; bu nedenle macOS Gatekeeper uyarısı beklenir. Yayın notu, uygulamayı Uygulamalar klasörüne taşıma ve Finder'da sağ tıklayıp `Aç` seçeneğini kullanma adımlarını açıkça anlatacaktır.

Bu repo şu an indirilebilir uygulama paketi yayınlamaz. Public Release, tamamlanan sürümün son görsel/işlev kontrolü ile son yayın onayından sonra oluşturulur. İmzasız ilk paket için girişte açılma özelliğinin çalışmaması beklenebilir; bu özellik ileride ayrı bir imzalama kararı gerektirir.

## Depo sınırı

Bu açık depo yalnızca i-Panel belgelerini, yol haritasını ve değişiklik kaydını içerir. Swift/Xcode kaynak kodu ve olası hassas yapılandırmalar özel kaynak deposunda tutulur.

## Belgeler

- [Değişiklik kaydı](CHANGELOG.md)
- [Yol haritası](ROADMAP.md)
