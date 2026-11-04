# New Road Software — güncellenmiş statik site

Teklifino tanıtımı ve tüm site için Türkçe/İngilizce dil seçimi eklendi. Yayınlama veya derleme bağımlılığı yoktur.

## Yerel önizleme

ZIP’i açın, terminalde `NRSWeb.github.io` klasörüne geçin ve çalıştırın:

```sh
python3 -m http.server 8000
```

Tarayıcıda http://localhost:8000 adresini açın. Bağımsız sayfalar:
- http://localhost:8000/easyphone/privacy/
- http://localhost:8000/chaos-wheel/privacy/

GitHub Pages için bu klasörün içeriğini yayın köküne yerleştirin. CNAME ve app-ads.txt korunmuştur.

## Değişen dosyalar

- index.html: iOS/B2B anlatımı, Teklifino bölümü, örnek teklif, menü, Türkçe temel içerik, çeviri anahtarları ve metadata.
- assets/css/main.v4.css: Teklifino paneli, erişilebilir dil seçimi, uyarlanabilir header, animasyon kapalıyken görünür içerik.
- assets/js/functions.v4.js: mevcut menü, filtre, ikon yedeği ve animasyon davranışları korunarak çeviri entegrasyonu ve filtre seçili durumu.
- assets/js/i18n.js (yeni): merkezi TR/EN sözlüğü, güvenli metin/öznitelik güncellemesi, kalıcı dil tercihi, metadata, video etiketleri ve dile uygun demo konusu.
- easyphone/privacy/index.html ve chaos-wheel/privacy/index.html: bütün hukuki metinlerin çevirileri, dil seçimi, göreli dosya yolları ve metadata.

## Doğrulama

Gerçek tarayıcıda kontrol edilenler:
- İlk açılışta Türkçe temel içerik; TR/EN geçişi ve sayfa başlıkları.
- Dil tercihinin yenilemede ve iki bağımsız gizlilik sayfasında korunması.
- Teklifino menü bağlantısı, mobil menünün kapanması ve iki dilde uygulama filtreleri; dil geçişinde seçili filtre korunması.
- Üç YouTube kartının mevcut video kimlikleri ve dile uygun erişilebilir etiketleri.
- Demo bağlantısının iki dilde doğru alıcı ve konu içermesi; Teklifino adresi.
- Ana sayfa ve gizlilik sayfalarında 360, 768, 1440 piksel genişlikleri; sayfa yatay taşması görülmedi. Filtre şeridi dar ekranda yatay kaydırılabilir.
- Tarayıcı konsolunda JavaScript hatası veya eksik çeviri uyarısı görülmedi.

Kaynak/çalışma zamanı kontrolleri:
- Her üç HTML sayfasındaki 76 yerel bağlantı/dosya referansı mevcut.
- Çeviri anahtarlarının TR/EN eşleşmesi ve JavaScript sözdizimi doğrulandı.
- localStorage engellendiğinde ilk dil ve dil değiştirme, izole JavaScript testiyle doğrulandı; tarayıcı gizlilik ayarları değiştirilmedi.
- 15 mevcut uygulama kartı ve özgün App Store bağlantıları korunuyor. CNAME ve app-ads.txt özgün ZIP ile byte düzeyinde aynı.
- Örnek hesap: 2.000 ₺ − 200 ₺ indirim + 360 ₺ KDV = 2.160 ₺.
- Türkçe temel HTML ve animasyon olmadan görünürlük kaynakta kontrol edildi. JavaScript tamamen kapalı kullanıcı akışı ayrıca tarayıcıda denenmedi.

Sınırlar: GitHub Pages’e dağıtım yapılmadı; üretim alan adı, dış bağlantıların hizmet durumu, App Store hedeflerinin erişilebilirliği ve e-posta teslimatı test edilmedi. Gerçek e-posta gönderilmedi. Safari/Firefox, fiziksel telefon ve ekran okuyucu testleri yapılmadı. JavaScript ile güncellenen metadata iki ayrı dil URL’si oluşturmaz; hreflang eklenmedi. Hukuki kapsam, 10 Temmuz 2026 / 29 Ekim 2026 tarihleri ve iletişim bağlantıları korundu; Teklifino için yeni hukuki hüküm eklenmedi.

ZIP; .git, __MACOSX veya .DS_Store içermez.
