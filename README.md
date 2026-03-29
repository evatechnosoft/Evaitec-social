# ev@itec — Social Media & Brand Package

Sosyal medya içerik paketi ve brand varlıkları.  
GitHub'a atılıp, otomasyon araçlarıyla (Buffer, Hootsuite, GitHub Actions) platformlara dağıtılabilir.

## 📁 Klasör Yapısı

```
evaitec-social/
├── README.md
├── brand-assets/
│   ├── logo-square.svg          # 400x400 profil logosu (SVG)
│   ├── logo-square-400.png      # LinkedIn/Instagram profil fotoğrafı
│   ├── logo-square-800.png      # Yüksek çözünürlük profil
│   ├── banner-cover.svg         # 1584x396 kapak görseli (SVG)
│   ├── banner-linkedin-1584x396.png
│   └── banner-twitter-1500x500.png
├── linkedin/
│   └── posts.md                 # 5 post (TR/EN), hashtag setleri
├── instagram/
│   ├── 01-launch.png            # Grid 1: Lansman
│   ├── 02-ai-solutions.png      # Grid 2: AI Çözümleri
│   ├── 03-flutter-mobile.png    # Grid 3: Flutter + BLE
│   ├── 04-process-automation.png # Grid 4: Otomasyon
│   ├── 05-tech-legacy.png       # Grid 5: IP Havuzu / Miras
│   ├── 06-contact-cta.png       # Grid 6: İletişim CTA
│   └── *.svg                    # Kaynak SVG dosyaları
├── twitter/
│   └── tweets.md                # 10 tweet (tek + thread format)
└── upwork/
    └── profile-and-portfolio.md # Profil, 3 portföy, teklif şablonları
```

## 🎨 Brand Rehberi

| Öge | Değer |
|-----|-------|
| **İsim** | ev@itec |
| **Slogan** | Yazılım & Yapay Zeka Teknolojileri |
| **Primary** | `#0d9488` (Teal) |
| **Secondary** | `#06b6d4` (Cyan) |
| **Accent** | `#34d399` (Mint) |
| **Dark BG** | `#080c14` |
| **Surface** | `#0e1420` |
| **Gradient** | Mint → Cyan → Teal (135deg) |

## 🚀 Kullanım

### Manuel Yayın
1. `linkedin/posts.md` içinden postları kopyala
2. `instagram/*.png` dosyalarını direkt yükle
3. `twitter/tweets.md` tweetleri kopyala
4. `upwork/profile-and-portfolio.md` ile profili kur

### Otomasyon (Önerilen)
Buffer, Hootsuite veya GitHub Actions ile otomatik yayın:

```yaml
# .github/workflows/social-post.yml örneği
name: Schedule Social Posts
on:
  schedule:
    - cron: '0 9 * * 1,3,5'  # Pazartesi, Çarşamba, Cuma 09:00
  workflow_dispatch:

jobs:
  post:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
      - name: Post to LinkedIn
        # Buffer API veya LinkedIn API entegrasyonu
        run: echo "Post scheduled"
```

## 📊 Yayın Takvimi (Önerilen)

| Hafta | Pazartesi | Çarşamba | Cuma |
|-------|-----------|----------|------|
| 1 | LinkedIn #1 (Launch) | Instagram #1-2 | Twitter #1-2 |
| 2 | LinkedIn #2 (AS a Consult) | Instagram #3-4 | Twitter #3-6 (EV Thread) |
| 3 | LinkedIn #3 (Behind Scenes) | Instagram #5-6 | Twitter #7-8 |
| 4 | LinkedIn #4 (Vision) | Upwork profile go-live | LinkedIn #5 (CTA) + Twitter #9-10 |

---

*ev@itec — Yazılım & Yapay Zeka Teknolojileri*  
*"Sen yönetirsin, ben yazarım."*
