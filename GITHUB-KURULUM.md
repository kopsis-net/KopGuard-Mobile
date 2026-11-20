# KopGuard — Android telefonla APK oluşturma

Bu paket Expo/React Native **demo arayüzü** içerir. Gerçek ESP32-CAM yayını ve push bildirimleri henüz bağlı değildir.

## GitHub üzerinden
1. Telefon tarayıcısında github.com/new adresinden **KopGuard-Mobile** adında yeni bir depo oluştur. Public veya Private olabilir. README ekleme.
2. Bu ZIP dosyasını telefonda çıkar. Depoya **dosyaların tamamını, klasör yapısını koruyarak** yükle. Özellikle `.github/workflows/android-apk.yml` dosyası depoda bulunmalı. GitHub mobil web arayüzünde gizli `.github` klasörünü yüklemek zor olursa GitHub web editörüyle tek tek oluştur veya GitHub'a ZIP yüklemek yerine dosyaları ekle.
3. Depoda **Actions** sekmesini aç, **KopGuard Android APK** iş akışını seç, **Run workflow** > **Run workflow** seç.
4. İşlem başarıyla tamamlandığında workflow çalışmasının en altındaki **Artifacts** bölümünden **KopGuard-Android-APK** dosyasını indir. GitHub artifact ZIP'ini açıp içindeki `app-debug.apk` dosyasını telefona kur.
5. Android 'bu kaynaktan yüklemeye izin ver' sorarsa yalnızca kendi derlediğin APK için izin ver.

Not: Bu yöntem test amaçlı **debug APK** üretir, mağaza yayınına uygun imzalı release sürümü değildir. Derlemenin başarılı olacağı bu ortamda doğrulanmadı. Android için internet erişimi ve GitHub Actions kotası gerekir. Workflow dosyası doğru konumda olmazsa Actions görünmez.
