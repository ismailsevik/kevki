# Kevki - Yöreswl RSS Okuyucu
<!--
Source - https://stackoverflow.com/q/41604263
Posted by zjffdu, modified by community. See post 'Timeline' for change history
Retrieved 2026-10-19, License - CC BY-SA 4.0
-->

![image](https://raw.githubusercontent.com/ismailsevik/kevki-reader/refs/heads/main/kevki-logo.png)


**Kevki**, popüler ve zarif RSS okuma servisi **Feedbin**'in minimalist, temiz ve odaklanmış tasarım estetiğini modern Android platformuna getiren bağımsız bir RSS okuma uygulamasıdır.

Uygulama derlenmiş ve imzalanmış Android APK dosyası olarak kullanıma hazırdır:
📁 **[`Kevki.apk`](file:///root/Kevki/Kevki.apk)**

---

## ✨ Özellikler

### 🎨 Arayüz
- **3 Sütunlu / Panelli Mimari**:
  - **Yan Menü (Abonelikler)**: Okunmamış, Yıldızlı ve Tüm Yazılar sayaçları, klasörlenmiş/kategorize edilmiş akışlar, faviconlar.
  - **Makale Listesi**: Feedbin tarzı mavi okunmadı noktası, temiz başlık ve 2 satırlı özet önizlemesi, göreceli zaman ("15d önce", "2s önce"), küçük görsel önizlemeleri.
  - **Okuyucu Paneli**: Feedbin'in ünlü dikkat dağıtmayan okuma deneyimi; serif / sans / mono yazı tipi seçenekleri, ayarlanabilir punto, satır aralıkları.
- **Temalar**:
  - ☀️ **Açık (Light)**: Klasik Feedbin beyaz/açık gri arayüzü ve mavi vurgu renkleri.
  - 📜 **Sepia**: Gözü yormayan sıcak krem ve kahverengi tonları.
  - 🌙 **Koyu (Dark)**: Şık grafit koyu tema.
  - 🖤 **Siyah (Midnight / OLED)**: Gerçek siyah AMOLED ekran dostu tema.
- **Dinamik Sistem Çubuğu**: Android durum ve gezinme çubukları seçilen temaya göre otomatik renk değiştirir.
- **Duyarlı (Responsive)**: Telefonlarda akıcı geçişli mobil tekil panel, tablet ve geniş ekranlarda tam Feedbin 3 sütun düzeni.

### ⚡ RSS & Multimedya Yetenekleri
- **📺 YouTube Video Takibi**:
  - YouTube kanal (@kanal_adi veya url), kullanıcı veya oynatma listesi URL'lerini otomatik algılar ve RSS formatına dönüştürür.
  - Okuyucu panelinde gömülü YouTube oynatıcı (iframe embed) ve tek dokunuşla YouTube uygulamasında açma düğmesi.
  - Makale listesinde kırmızı "▶ Video" rozeti ve yüksek çözünürlüklü video küçük resimleri (thumbnails).
- **🎙️ Podcast RSS & Dahili Ses Oynatıcı**:
  - Podcast RSS akışlarını (`<enclosure type="audio/...">`, iTunes etiketleri) tam olarak destekler.
  - Okuyucu içinde şık Feedbin tarzı ses kontrol kartı (Oynat/Duraklat, -15s geri / +30s ileri, ilerleme çubuğu, 1.0x - 2.0x hız ayarı).
  - **Kesintisiz Kayan Mini Oynatıcı (Global Mini-Player)**: Bir podcast çalarken menülerde ve yazı listelerinde gezinirken altta çalan ve durdurulmayan mini kontrol paneli.
- **🔔 Özelleştirilebilir Yeni Yayın Bildirimleri**:
  - Hem genel ayarlardan açılıp kapatılabilen, hem de akış bazında (akış düzenleme penceresinden) bağımsız olarak seçilebilen bildirim sistemi.
  - Yeni bir yazı, video veya podcast bölümü geldiğinde Android sistem bildirimi gönderilir; bildirime tıklayınca doğrudan ilgili içeriği açar.
- **✏️ Akış RSS URL'lerini Düzenleme & Düzeltme**:
  - Eklenmiş herhangi bir kaynağın RSS bağlantısını düzenleme penceresinden istediğiniz an değiştirip düzeltebilme imkanı.
  - URL değiştiğinde akış anında yeni adresten senkronize edilir.
- **CORS Sınırsız Yerel İndirme**: Android yerel `HttpURLConnection` motoru sayesinde herhangi bir sunucudan engelsiz, yönlendirme (redirect) ve gzip destekli akış indirme.
- **RSS 2.0 & Atom 1.0 Desteği**: Standart RSS, RDF ve Atom akışlarını otomatik algılayıp ayrıştırır.
- **Tam Metin Modu (Mercury / Full-Text Extractor)**: Sadece kısa özet veren RSS akışlarında tek tıkla orijinal web sayfasındaki makale gövdesini ayıklar.
- **Çevrimdışı Depolama (IndexedDB)**: İndirilen tüm makaleler ve durumları yerel veritabanında saklanır; internetsizken de okunabilir.
- **OPML İçe / Dışa Aktarım**: Mevcut RSS aboneliklerinizi tek tıkla OPML dosyası veya metni olarak içe/dışa aktarın.
- **Yerel Android Paylaşımı**: Android'in yerel paylaşım menüsü ile makaleleri dilediğiniz uygulamaya gönderin.
- **Hazır Akışlar**: İlk açılışta zengin içerik sunan teknoloji, haber, YouTube (Barış Özcan) ve Podcast (Fularsız Entellik, BBC Türkçe) yayınları önceden yüklenmiş gelir.

---

## 📦 Kurulum ve Çalıştırma

APK dosyasını Android cihazınıza yüklemek için:

```bash
# ADB üzerinden yüklemek için:
adb install /root/Kevki/Kevki.apk
```

veya `Kevki.apk` dosyasını cihazınıza aktarıp doğrudan dokunarak kurabilirsiniz (Bilinmeyen kaynaklardan kuruluma izin verilmiş olmalıdır).

---

## 🛠️ Derleme Mimarisi

- **Paket Adı**: `com.kevki.reader`
- **Hedef SDK**: Android API 33 (Android 13)
- **Minimum SDK**: Android API 21 (Android 5.0+)
- **İmza**: v1, v2 ve v3 şemalarıyla imzalanmış release anahtarı
- **Boyut**: ~50 KB (hafif ve yüksek performanslı)
