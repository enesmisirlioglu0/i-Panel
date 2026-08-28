# i-Panel

<p align="center">
  <img src="assets/i-panel-icon.png" alt="Kırmızı, mavi ve yeşil üç karttan oluşan i-Panel simgesi" width="180">
</p>

i-Panel, Mac'in menü çubuğunda çalışan küçük bir durum göstergesi ve hızlı kontrol panelidir. Menü çubuğunda macOS'un kendi sade, tek renkli üçlü-kart sembolünü kullanır; yukarıdaki renkli işaret ise Finder, DMG ve proje görselidir.

## Geliştirme notu

i-Panel, proje sahibinin ürün fikri, kapsamı, görsel tercihleri ve gerçek Mac üzerindeki kabul testleri doğrultusunda geliştirildi. Swift/Xcode uygulama kodu, hata ayıklama ve dokümantasyon çalışmaları ise proje sahibinin yönlendirmesiyle **ChatGPT 5.6 Terra (OpenAI Codex)** yapay zekâ geliştirme asistanının desteği kullanılarak birlikte yürütüldü. Proje sahipliği ile tüm ürün ve yayın kararları proje sahibine aittir.

## İndir — 1.2 (Build 3)

[**i-Panel-1.2-build-3-unsigned.dmg dosyasını indir**](https://github.com/enesmisirlioglu0/i-Panel/releases/download/v1.2/i-Panel-1.2-build-3-unsigned.dmg)

- Platform: macOS 13 ve sonrası
- Tek DMG: Apple Silicon ve Intel Mac (`arm64` + `x86_64`)
- Paket: imzasız ve noterlenmemiş ilk public sürüm
- SHA-256: [`i-Panel-1.2-build-3-unsigned.dmg.sha256`](assets/i-Panel-1.2-build-3-unsigned.dmg.sha256)

## Kurulum

1. DMG dosyasını açın.
2. `i-Panel.app` uygulamasını `Applications` bağlantısına sürükleyin.
3. İlk açılışta macOS uyarı gösterirse uygulamaya Finder'da sağ tıklayın, **Aç** seçeneğini seçin ve ardından çıkan **Aç** düğmesine basın.
4. Uygulama Dock'ta görünmeyebilir; üst sağdaki menü çubuğu simgesinden panele ulaşırsınız.

Bu ilk paket Developer ID ile imzalanmış veya noterlenmiş değildir. Bu yüzden Gatekeeper uyarısı beklenir; Gatekeeper'ı kapatmanız gerekmez.

## Neler var?

- CPU, bellek, disk, batarya sıcaklığı/durumu ve anlık indirme/yükleme için beş kart
- Anında doğrudan sürükle-bırakla kart sıralama ve `Sıfırla` ile varsayılan sıraya dönüş
- `Ayar` düğmesinden girişte açılma isteği, Dock görünürlüğü, kart sırasını hatırlama ve 1 / 3 / 5 saniyelik yenileme aralığı
- Turkuaz tonlu kompakt panel ve panel dışına tıklanınca yerel macOS davranışıyla kapanma

Kartlarda gösterilen CPU, bellek, disk, batarya ve ağ değerleri bu ilk fazda **simülasyondur**. i-Panel gerçek sistem metriklerini toplamaz, ağa bağlanmaz veya bulut hesabı kullanmaz. Tercihler yalnızca cihazdaki yerel macOS tercihlerinde saklanır.

## Doğrulama

28 Ağustos 2026'da geliştirici Mac'inde şu kabul testleri tamamlandı:

- Menü çubuğu simgesinden paneli açma ve kapatma
- `Ayar` düğmesi ve Dock görünürlüğü ayarı
- Kartları doğrudan sürükleyerek sıralama
- `Sıfırla` ile varsayılan kart sırasına dönme
- Universal imzasız Release derlemesi, DMG bütünlük doğrulaması ve DMG içeriği denetimi

`Girişte i-Panel’i aç` ayarı macOS'un geçerli uygulama imzası isteyebilen `SMAppService` özelliğine dayanır. Bu nedenle imzasız public pakette bu ayarın çalışması garanti edilmez.

## Kaynak kod

Swift/Xcode kaynakları da artık açıktır: [i-Panel-Source](https://github.com/enesmisirlioglu0/i-Panel-Source). Kaynak kod [MIT Lisansı](https://github.com/enesmisirlioglu0/i-Panel-Source/blob/main/LICENSE) ile kullanılabilir, değiştirilebilir ve dağıtılabilir. İndirme ve sürüm notları ise bu depodaki GitHub Releases alanında tutulur.

## Belgeler

- [Değişiklik kaydı](CHANGELOG.md)
- [Yol haritası](ROADMAP.md)
