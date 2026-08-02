# ÖZER BEND PRO — Gizlilik Politikası (yayın deposu)

Bu depo **sadece** ÖZER BEND PRO uygulamasının gizlilik politikasını barındırır.
Uygulama kaynak kodu burada değildir ve buraya konulmamalıdır.

## Neden ayrı bir depo?

Google Play, çalışır durumda ve herkese açık bir gizlilik politikası URL'i zorunlu
tutuyor. Ana depo (`ozer-bend-pro1`) **private** ve öyle kalmalı — içinde imzalama
anahtarı (`keystore/`), iş mantığı ve dağıtım yapılandırması var. Private bir depoda
GitHub Pages ücretli plan gerektirdiği için politika, içinde hiçbir gizli bilgi
olmayan bu ayrı **public** depodan yayınlanıyor.

## Yayınlama

1. GitHub'da `ozer-bend-pro-privacy` adında **public** bir depo aç.
2. Bu klasörü push et.
3. Settings → Pages → Source: `Deploy from a branch`, Branch: `main` / `(root)`.
4. Yayınlanan adres: https://halilozer03-dotcom.github.io/ozer-bend-pro-privacy/

Bu adres iki yerde geçiyor, ikisi de aynı olmalı:

- `src/main.jsx` içindeki `PRIVACY_POLICY_URL` sabiti (uygulama içi bağlantı)
- Play Console → App content → Privacy policy alanı

## Güncelleme

Politikanın kaynağı ana depodaki `docs/` klasörüdür. Değişiklik önce orada yapılır,
sonra `index.html` ve `en.html` buraya kopyalanıp push edilir. İki kopyanın da aynı
kalması gerekir — politika metni ile uygulamanın gerçekte yaptığı iş birbirini
tutmazsa bu bir uyumluluk sorunudur, kozmetik bir tutarsızlık değil.
