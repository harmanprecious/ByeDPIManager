# ByeDPI Manager

[Русский](README.md) | [English](README.en.md) | Türkçe

ByeDPI ve ProxiFyre çalıştırmak için mini bir program.

![Interface Screenshot](screens/screen_en.png)

## Gereksinimler

1. Windows 7+, [.NET Framework 4.7.2+](https://dotnet.microsoft.com/en-us/download/dotnet-framework/thank-you/net472-offline-installer)
2. [ProxiFyre](https://github.com/wiresock/proxifyre), [Windows Packet Filter](https://github.com/wiresock/ndisapi), [Visual C++ Redist 2022](https://learn.microsoft.com/en-us/cpp/windows/latest-supported-vc-redist?view=msvc-170#latest-microsoft-visual-c-redistributable-version)
3. [ByeDPI](https://github.com/hufrea/byedpi)

## Kurulum

### 1. Seçenek: Paket Programlar (Normal kullanıcılar için önerilir)

Bu seçenekte gerekli tüm programlar tek bir arşiv dosyasının içerisinde gelir.

1. **İndirme:**

   * İndirme sayfasına git: [https://github.com/romanvht/ByeDPIManager/releases/latest](https://github.com/romanvht/ByeDPIManager/releases/latest)
   * `All_In_One_w64.zip` dosyasını indir.

2. **Extraction:**

   * İndirilen dosyayı bilgisayarınızda bulun.
   * Sağ tıklayın ve  “Buraya ayıkla…” seçeneğini seçin.
   * Bir kurulum klasörü seçin. (Örneğin; `C:\APPS\ByeDPIManager`)

3. **Kurulum Gereksinimlerinin Yüklenmesi:**

   * Çıkarılan arşivin içindeki `redist` klasörünü açın.
   * Aşağıdaki iki uygulamayıda bu klasörün içerisinden yükleyin.

     * Windows Packet Filter (ProxiFyre için gerekli)
     * Visual C++ Redistributable 2022

### 2. Seçenek: Manuel Yükleme (Gelişmiş kullanıcılar için önerilir)

Programları ayrı ayrı yönetmeyi tercih ediyorsanız:

1. **Programları ayrı olarak indirin:**

   * [Manager](https://github.com/romanvht/ByeDPIManager/releases/latest)
   * [ByeDPI](https://github.com/hufrea/byedpi)
   * [ProxiFyre](https://github.com/wiresock/proxifyre)

2. **Gereksinimleri İndirin:**

   * [Windows Packet Filter](https://github.com/wiresock/ndisapi) (ProxiFyre için gerekli)
   * [Visual C++ Redistributable 2022](https://learn.microsoft.com/en-us/cpp/windows/latest-supported-vc-redist?view=msvc-170#latest-microsoft-visual-c-redistributable-version)

3. **Tüm programları uygun bir klasöre çıkarın**

4. **Uygulamayı çalıştırın ve diğer programların yollarını ayarlayın:**

   * ByeDPI sekmesinde `ciadpi.exe` için doğru yolu belirtin
   * ProxiFyre sekmesinde `proxifyre.exe` için doğru yolu belirtin

## Konfigürasyon

### İlk Kurulum

1. **Programı çalıştırın:**

   * `ByeDPI Manager.exe`'yi açın.
   * "Ayarlar" butonuna basın.

2. **ProxiFyre ayarları:**

   * “ProxiFyre” sekmesine gidin.
   * Beraber çalışmasını istediğiniz uygulamaları seçin. (Örneğin; Chrome, Firefox, vb.)

### Deneme ayarları

#### Önceden tanımlanmış denemeleri kullanmak

* “ByeDPI” sekmesindeki “Argümanlar” alanına istediğiniz denemey girin.

#### Deneme (opsiyonel)

Önceden tanımlanmış bir denemeniz yoksa, yerleşik test aracını kullanabilirsiniz:

1. **Test sekmesine gidin:**

   * “Denemeler (Beta)” sekmesine gidin

2. **Teste başlayın:**

   * “Başla” butonuna basın.
   * İlk kez çalıştırdığınızda, `ciadpi.exe` için ağ erişimine izin vermeniz istenecektir. “İzin Ver” seçeneğine tıklayın.

3. **Deneme seçin:**

   * Test tamamlandıktan sonra, %50'nin üzerinde başarı sağlayan deneme günlük kaydında listelenecektir.
   * En iyi olanı seçin ve kopyalayın. (Ctrl+C)

4. **Denemeyi uygulamak:**

   * “ByeDPI” sekmesine geri dönün.
   * Kopyalanan stratejiyi “Parametreler” alanına yapıştırın. (Ctrl+V)

5. **Testi özelleştirme (isteğe bağlı):**

   * `proxytest` klasöründeki dosyaları düzenleyin:

     * `sites.txt` - test etmek için kendi sitelerinizi ekleyin.
     * `cmds.txt` - kontrol etmek için kendi denemelerinizi ekleyin.

### Başlatma ve Test

1. **Etkinleştirme:**

   * Ana pencerede “Bağlan” butonuna tıklayın.
   * ProxiFyre ilk kez ağ erişimi isteyecektir. “İzin Ver” seçeneğine tıklayın.

2. **Çalıştığını doğrulayın:**

   * Yapılandırdığınız bir tarayıcı veya uygulamayı açın.
   * Kaynakların erişilebilir olup olmadığını kontrol edin.

## Sorun Giderme

* Uygulama başlamazsa, .NET Framework 4.7.2+'nın yüklü olduğundan emin olun
* Eğer DPI Bypass işe yaramazsa farklı bir deneme yapın ve onu kullanın.
* Bağlantı sorunları oluşursa, Windows Packet Filter'ın düzgün yüklendiğinden emin olun.
* Antivirüs veya güvenlik duvarınızın uygulamayı engellemediğinden emin olun.

## Special Thanks

* [ByeDPI](https://github.com/hufrea/byedpi)
* [ProxiFyre](https://github.com/wiresock/proxifyre)
* [Windows Packet Filter](https://github.com/wiresock/ndisapi)
* [SocksSharp](https://github.com/extremecodetv/SocksSharp)
