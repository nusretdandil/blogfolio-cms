# Blogfolio CMS

Modern, modular PHP 8.2 CMS for blogs and portfolios. Built with Slim 4, Twig, Eloquent (SQLite by default), and Tailwind CSS (CDN) + Alpine.js.

## Özellikler
- Slim 4 yönlendirme ve middleware
- Twig şablonlama
- Eloquent ORM (varsayılan SQLite)
- Tailwind CSS (CDN) ve Alpine.js (CDN)
- Basit klasör yapısı, kolay kurulum

## Gereksinimler
- PHP >= 8.2
- Composer
- (Opsiyonel) Apache veya Nginx. Apache için `public/.htaccess` eklidir.

## Kurulum
```bash
composer install
cp .env.example .env
# Varsayılan olarak SQLite kullanır. Veritabanı dosyası: storage/database.sqlite
mkdir -p storage && touch storage/database.sqlite
php -S localhost:8080 -t public
```

Ardından tarayıcıda http://localhost:8080 adresine gidin.

## Yapı
```
.
├── bootstrap/          # Uygulama bootstrap (Slim, Twig, Eloquent)
├── config/             # (İleride) yapılandırma dosyaları için
├── public/             # Web kökü (index.php)
├── routes/             # Rotalar
├── src/                # PHP kaynak kodu (Controller vb.)
├── storage/            # SQLite dosyası ve cache/log klasörleri
├── views/              # Twig şablonları
└── composer.json       # Bağımlılıklar
```

## Geliştirme
- Hızlı sunucu: `composer start` (PHP built-in server ile `public` klasörünü sunar)
- Lint: `composer lint`

## Notlar
- Bu başlangıç sürümü bir iskelet sağlar. Modül, tema, admin paneli ve SEO bileşenleri ilerleyen sürümlerde eklenecektir.

## Lisans
MIT
