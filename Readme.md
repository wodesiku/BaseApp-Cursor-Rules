(@ işaretini kullanarak cursor'a yüklediğimiz dökümanları gir.)
Yukarıdaki dökümanları kullanarak bir Farcaster Mini App oluştur.

---

## UYGULAMA FİKRİ:

[BURAYA UYGULAMA FİKRİNİ YAZ]

---

## DOSYA YAPISI:

proje/
├── index.html
├── style.css
├── game.js
├── icon.html
├── package.json
└── .well-known/
    └── farcaster.json

Dosya yapısı uygulamaya göre değişiklik gösterebilir ama farcaster uyumlu ve gerekmedikçe değişmeyecektir.
---

## TEKNİK GEREKSİNİMLER:

### index.html:
- Meta tag: <meta name="fc:frame" content="vNext">
- Meta tag: <meta name="base:app_id" content="[SONRA EKLENECEK]">
- Mobil viewport: maximum-scale=1.0, user-scalable=no
- script type="module"

### game.js:
- Başlangıçta Farcaster SDK:
  import { sdk } from 'https://esm.sh/@farcaster/frame-sdk';
  sdk.actions.ready();
- Mobil touch kontrolleri

### icon.html:
- Canvas ile 200x200 icon.png oluştur
- Canvas ile 600x400 preview.png oluştur
- İndirme linkleri ekle

### package.json:
{
  "name": "mini-app",
  "version": "1.0.0",
  "scripts": {
    "dev": "npx serve . -p 3000"
  },
  "devDependencies": {
    "serve": "^14.2.0"
  }
}

### farcaster.json:
{
  "accountAssociation": {
    "header": "[FARCASTER'DAN ALINACAK]",
    "payload": "[FARCASTER'DAN ALINACAK]",
    "signature": "[FARCASTER'DAN ALINACAK]"
  },
  "frame": {
    "version": "1",
    "name": "[UYGULAMA ADI]",
    "subtitle": "[KISA AÇIKLAMA]",
    "description": "[DETAYLI AÇIKLAMA]",
    "iconUrl": "https://[DOMAIN]/icon.png",
    "homeUrl": "https://[DOMAIN]",
    "imageUrl": "https://[DOMAIN]/preview.png",
    "splashImageUrl": "https://[DOMAIN]/icon.png",
    "splashBackgroundColor": "#000000",
    "primaryCategory": "games",
    "tags": ["game", "arcade", "farcaster"],
    "tagline": "[MAX 30 KARAKTER]",
    "heroImageUrl": "https://[DOMAIN]/preview.png",
    "screenshotUrls": ["https://[DOMAIN]/preview.png"],
    "ogTitle": "[OG BAŞLIK]",
    "ogDescription": "[OG AÇIKLAMA]",
    "ogImageUrl": "https://[DOMAIN]/preview.png"
  }
}

Bu bilgileri farcaster adımında sana atarsa kullanıcı otomatik ekleyeceksin ve pushlamasını söyleyeceksin.
---

## ❌ YAPMA:
- SVG kullanma (PNG şart)
- Uzun tagline yazma
- webhookUrl ekleme
- noindex ekleme
- Gereksiz özellik ekleme

## ✅ YAP:
- Basit ve çalışır tut
- Mobil kontroller ekle
- Responsive tasarım yap

---

## LOKAL TEST:

Uygulama tamamlandıktan sonra şu komutları terminalde çalıştır:

npm install
npm run dev

Tarayıcıda http://localhost:3000 adresini aç ve test et.

Çalışıyorsa http://localhost:3000/icon.html adresinden:
- "Download icon.png" tıkla → icon.png indir
- "Download preview.png" tıkla → preview.png indir
- İndirilen dosyaları proje klasörüne taşı

---

## 🚀 İLK DEPLOY (GitHub + Vercel):

1. GitHub'da yeni repo oluştur
2. Terminalde şu komutları çalıştır:

git init
git add .
git commit -m "first commit"
git branch -M main
git remote add origin [REPO_URL]
git push -u origin main

3. Vercel'e git ve GitHub reposunu bağla
4. Deploy tamamlanınca URL'i al

---

## FARCASTER DOĞRULAMA:

1. https://warpcast.com/~/developers/mini-apps adresine git
2. URL'ini gir ve accountAssociation bilgilerini al
3. farcaster.json dosyasına bu bilgileri ekle
4. Tüm [DOMAIN] yerlerini Vercel URL'in ile değiştir

---

## BASE APP DOĞRULAMA:

1. Base App'te "Add Mini App" seç
2. URL'ini gir
3. Verilen base:app_id değerini al
4. index.html içindeki meta tag'i güncelle:
   <meta name="base:app_id" content="[ALINAN_ID]">

---

## DEĞİŞİKLİK SONRASI GÜNCELLEME:

Her değişiklikten sonra şu komutları çalıştır:

git add .
git commit -m "Update"
git push

Vercel otomatik deploy edecek.

---

Şimdi bu gereksinimlere uygun çalışan bir uygulama oluştur. Hiç bilmeyen biri yaptığı için sana attığında adım gösterme direkt çözüme ulaştır. Gereksiz bilgilerden kaçın.
