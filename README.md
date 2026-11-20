# KopGuard Mobile — React Native / Expo

ESP32-CAM + Reed Switch güvenlik sistemi için **mobil arayüz prototipi**.

## Çalıştırma

Node.js LTS kurulu bilgisayarda:

```bash
npm install
npx expo start
```

Telefonunuzda Expo Go ile QR kodu açabilirsiniz. Expo SDK 54 ile uyumlu Expo Go sürümü kullanın.

## Ekranlar

Ana Sayfa, Canlı İzleme, Olay Kayıtları, Olay Detayı, Cihazlar, Ayarlar, Güvenlik Ayarları, Kamera Ayarları, Bildirim Ayarları, Genel Ayarlar, Profil.

## Durum

- Navigasyon, olay filtreleri, kapı simülasyonu ve ayar anahtarları etkileşimlidir.
- Kamera, olay fotoğrafı, cihaz durumu ve bildirimler **demo** verisidir.
- Ağ istekleri, kullanıcı girişi, kalıcı ayarlar, gerçek kayıt, push bildirimleri ve gerçek ESP32-CAM bağlantısı henüz yoktur.
- Cihazın mevcut firmware'ine müdahale edilmez.
- Sabit ESP32-CAM'de PTZ olmadığından yön tuşları eklenmedi.

## Sonraki entegrasyon

Mevcut API'nizin endpoint'leri belirlendikten sonra olay listesi, fotoğraf URL'leri, canlı MJPEG akışı ve cihaz komutları bağlanabilir. Dış erişimde HTTPS ve yetkilendirme kullanın.

## Android APK (EAS Build)

```bash
npm install
npx eas-cli login
npx eas-cli build:configure
npx eas-cli build --platform android --profile preview
```

`build:configure` Expo hesabına ait proje kimliğini oluşturabilir ve `app.json` dosyasını güncelleyebilir. `preview` profili `eas.json` içinde APK olarak ayarlanmıştır. Derleme tamamlandığında EAS sayfasındaki APK bağlantısını Android telefonunuzda açarak yükleyin. Bu işlem için Expo hesabı ve internet bağlantısı gerekir. APK henüz oluşturulmamıştır.
