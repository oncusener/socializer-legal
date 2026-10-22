# Socializer — Yasal Metinler

Socializer mobil uygulamasının herkese açık yasal metinleri.
GitHub Pages ile yayınlanır.

Yayın adresi: https://oncusener.github.io/socializer-legal/

| Sayfa | Türkçe | İngilizce |
| --- | --- | --- |
| Gizlilik Politikası | `index.html` | `en/index.html` |
| Kullanım Şartları | `kullanim-sartlari.html` | `en/terms.html` |
| Çocuk Güvenliği Standartları (Google Play CSAE) | `cocuk-guvenligi.html` | `en/child-safety.html` |
| Hesap ve Veri Silme | `hesap-silme.html` | `en/account-deletion.html` |

Notlar:

- Adresler uygulamada `src/config/legal.ts` içinde tek yerde tutulur ve mağaza
  konsollarına girilen adreslerle aynı olmalıdır. Dosya adını değiştirme.
- Kullanım Şartları sürümü (`2026-10-22`) API'deki `TERMS_VERSION` ve uygulamadaki
  `CURRENT_TERMS_VERSION` ile aynı olmalıdır. Şartlar değişince üçünü birlikte güncelle;
  kullanıcılardan yeniden onay istenir.
- Metinler uygulamanın gerçek davranışını anlatır (saklama süreleri, silinen veriler,
  üçüncü taraflar). Kodda bu davranış değişirse ilgili sayfayı da güncelle.
- Kullanım Şartları'ndaki kurucu üye programı (`#kurucu-uye` / `#founding-members`)
  "şu an ilk 5.000 kişi" ve "şu an 365 gün" der. Paneldeki `founderCap`,
  `founderPlanType` veya `founderDurationDays` değişirse bu iki ifadeyi de güncelle.
- **Yayın sırası (Ekim 2026 sürümü):** Bu metinlerin anlattığı silme, temizlik görevi, push
  jetonu, çevrimiçi durum gizleme ve panelden silme davranışları API `42d956e`, `befffba`,
  `47f2ddf` (migration'lar `20261022200000_founder_live`, `20261022220000_push_tickets`), admin
  backend `551043f` ve admin frontend `ec0fefb` canlıya çıkınca doğru olur.
  Sıra: önce API ve admin deploy, sonra bu repo push ile uygulama OTA'sı aynı anda. Uygulama
  `src/config/legal.ts` ile `kullanim-sartlari.html` ve `en/` sayfalarına bağlanır; bu repo
  push edilmeden OTA çıkarsa şartlar onay ekranı 404 sayfasına gider.
- Gizlilik 7. bölümdeki "SMS sağlayıcısı" satırı sağlayıcı adını vermez; canlıda sağlayıcı
  seçilince (`SMS_PROVIDER`: Netgsm Türkiye'de, Twilio ABD'de) adını yaz. Twilio seçilirse
  numara ve kod yurt dışına aktarılır; KVKK md. 9 güvencesini de belirt.
- Her sayfanın üstünde dört sayfa arasında ve TR/EN karşılığına giden bağlantılar vardır.
  Bağlantılar görelidir; dış bağımlılık yoktur.
