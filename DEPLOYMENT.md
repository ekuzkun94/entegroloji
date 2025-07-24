# 🚀 Render Deployment Rehberi

Bu rehber, Entegroloji web sitesini Render'da deploy etmek için adım adım talimatları içerir.

## 📋 Ön Gereksinimler

- GitHub hesabı
- Render hesabı (ücretsiz)
- Proje dosyaları hazır

## 🔧 Adım Adım Deployment

### 1. GitHub'a Yükleme

```bash
# Git repository'yi başlat
git init

# Dosyaları ekle
git add .

# İlk commit
git commit -m "Initial commit: Entegroloji website"

# GitHub'da yeni repository oluştur (manuel olarak)
# Sonra remote'u ekle
git remote add origin https://github.com/KULLANICI_ADIN/entegroloji.git

# Push yap
git push -u origin main
```

### 2. Render'da Hesap Oluşturma

1. [render.com](https://render.com) adresine git
2. "Get Started" butonuna tıkla
3. GitHub ile giriş yap
4. Email doğrulamasını tamamla

### 3. Yeni Web Service Oluşturma

1. Render Dashboard'da "New +" butonuna tıkla
2. "Static Site" seçeneğini seç
3. GitHub repository'ni bağla:
   - "Connect a repository" tıkla
   - `entegroloji` repository'ni seç
   - "Connect" butonuna tıkla

### 4. Service Konfigürasyonu

Aşağıdaki ayarları yap:

```
Name: entegroloji
Branch: main
Root Directory: (boş bırak)
Build Command: (boş bırak)
Publish Directory: (boş bırak)
```

### 5. Environment Variables (Opsiyonel)

Şu an için environment variable'a gerek yok, boş bırakabilirsin.

### 6. Deploy

1. "Create Static Site" butonuna tıkla
2. Render otomatik olarak deploy işlemini başlatacak
3. 2-3 dakika içinde siteniz yayında olacak

## 🌐 Site URL'i

Deploy tamamlandıktan sonra şu formatta bir URL alacaksın:
```
https://entegroloji.onrender.com
```

## 🔄 Otomatik Deploy

Render, GitHub repository'ndeki her değişiklikte otomatik olarak yeni deploy yapar:

1. Kod değişikliği yap
2. GitHub'a push et
3. Render otomatik deploy eder

## 📊 Monitoring

Render Dashboard'da şunları görebilirsin:
- Deploy durumu
- Site performansı
- Error logları
- Traffic analytics

## 🔧 Custom Domain (Opsiyonel)

Özel domain eklemek için:

1. Render Dashboard'da service'ine git
2. "Settings" sekmesine tıkla
3. "Custom Domains" bölümünde domain ekle
4. DNS ayarlarını yap

## 🚨 Troubleshooting

### Yaygın Sorunlar:

**1. Build Hatası**
- `render.yaml` dosyasının doğru olduğundan emin ol
- Build command'ın boş olduğunu kontrol et

**2. 404 Hatası**
- `index.html` dosyasının root'ta olduğunu kontrol et
- Route ayarlarını kontrol et

**3. CSS/JS Yüklenmiyor**
- Dosya yollarının doğru olduğunu kontrol et
- Browser console'da hata var mı bak

### Debug İçin:

```bash
# Local'de test et
python -m http.server 8000
# http://localhost:8000 adresinde çalışıyor mu kontrol et
```

## 📈 Performance Optimizasyonu

Deploy sonrası performansı artırmak için:

1. **Image Optimization**
   - WebP format kullan
   - Lazy loading ekle

2. **CSS/JS Minification**
   - Production build için minify et

3. **Caching**
   - Browser cache ayarları
   - CDN kullanımı

## 🔒 SSL/HTTPS

Render otomatik olarak SSL sertifikası sağlar. HTTPS zorunlu.

## 📱 Mobile Testing

Deploy sonrası şunları test et:
- [ ] Mobile responsive
- [ ] Touch interactions
- [ ] Loading speed
- [ ] Form functionality

## 🎯 SEO Optimizasyonu

Deploy sonrası SEO için:

1. **Google Search Console**'a site ekle
2. **Google Analytics** kur
3. **Sitemap** oluştur
4. **Meta tags** kontrol et

## 📞 Destek

Sorun yaşarsan:
- Render Documentation: https://render.com/docs
- Render Support: support@render.com
- GitHub Issues: Repository'de issue aç

---

**🎉 Tebrikler!** Siteniz artık yayında ve dünyanın her yerinden erişilebilir! 