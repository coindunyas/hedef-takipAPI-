# Binance TR Hedef Takip

Supabase ile ortak veri kullanan hedef takip uygulamasi.

## Ozellikler
- Kayit ekleme, kopyalama, silme
- Kayit arama
- Binance TR sembolu ile fiyat cekme
- Asagi/Yukari hedef kontrolu
- Verileri Supabase uzerinde ortak saklama
- JSON yedek alma ve geri yukleme
- Ayni linki acan herkesin ayni kayitlari gorebilmesi

## Kurulum
Bu proje statik bir uygulamadir.

### Gerekli ayarlar
`index_supabase.html` icinde su bilgiler tanimli:
- Supabase URL
- Supabase publishable key

Bu bilgiler dogrudan dosya icine eklenmistir.

## Calistirma
### Secenek 1
`index_supabase.html` dosyasini dogrudan tarayicida ac.

### Secenek 2
GitHub'a yukle ve statik olarak kullan.

## GitHub'a yukleme
1. GitHub'da yeni bir repo olustur.
2. `index_supabase.html` dosyasini ve diger gerekli dosyalari repoya yukle.
3. GitHub Pages ile yayinla veya statik olarak kullan.

## Veri saklama
Veriler Supabase icinde tutulur.
Bu yuzden:
- Ayni linki acan herkes ayni veriyi gorur.
- Farkli cihazlardan erisim saglanabilir.
- Tarayici verileri silinse bile kayitlar durur.

## Tablo yapisi
Supabase tarafinda `targets` tablosu kullanilir.
Alanlar:
- `id`
- `created_at`
- `coin`
- `symbol`
- `date`
- `lower_target`
- `upper_target`
- `note`
- `status`

## Not
- Sitede sadece `sb_publishable_` ile baslayan anahtar kullanilmalidir.
- `sb_secret_` ile baslayan gizli anahtar asla HTML dosyasina konulmamalidir.
- Binance TR fiyat cekebilmek icin gecerli sembol kullanilmalidir. Ornek:
  - `BTCTRY`
  - `ETHTRY`
  - `SOLTRY`
