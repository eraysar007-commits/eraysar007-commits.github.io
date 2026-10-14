# AGENT XI - web sitesi (GitHub Pages)

Tamamen statik site: harici script, yazı tipi, izleyici ve çerez yoktur. Her sayfada stil kendi içindedir (`<style>`).
Adres: https://eraysar007-commits.github.io (kullanıcı sitesi; bu klasörün içeriği deponun köküne konur).

| Dosya | İçerik |
| --- | --- |
| `index.html` | Tanıtım (TR + EN aynı sayfada), sayfalara bağlantılar, "App Store'da yakında" |
| `gizlilik.html` / `privacy.html` | Gizlilik Politikası (TR / EN) |
| `kullanim-sartlari.html` / `terms.html` | Kullanım Şartları (TR / EN) |
| `destek.html` / `support.html` | Destek e-postası + SSS (TR / EN) |

## Yayından önce doldurulacak yer tutucular

- `{{GELISTIRICI}}`: geliştirici / veri sorumlusu adı (gizlilik ve kullanım şartları sayfalarında, TR + EN).
- `{{TARIH}}`: yürürlük / son güncelleme tarihi (aynı dört sayfada).

Kontrol: `grep -n "{{" *.html` yayından sonra boş dönmeli.

## Nasıl güncellenir

1. İlgili HTML dosyasını düzenle. TR ve EN çiftleri (gizlilik/privacy, kullanım-şartları/terms, destek/support) aynı içerikte kalmalı; birini değiştirirsen ötekini de değiştir.
2. Metin uygulama içi yasal metinle (`lib/ui/l10n/yasal_metin.dart`) aynı içerikte olmalı; fark çıkarsa ikisini birlikte güncelle.
3. Yasal sayfada bir değişiklik yaptığında `{{TARIH}}` yerine yazılan tarihi güncelle.
4. İletişim e-postası değişirse tüm dosyalarda `eraygs001@hotmail.com` aranıp değiştirilir.
5. Mağaza yayınlanınca `index.html` içindeki "yakında" ibaresi (TR + EN) mağaza bağlantısıyla değiştirilir.
