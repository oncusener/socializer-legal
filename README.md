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
  "şu an ilk 5.000 kişi" ve "şu an 12 ay" der. Paneldeki `founderCap`,
  `founderPlanType` veya `founderDurationDays` değişirse bu iki ifadeyi de güncelle.
- Her sayfanın üstünde dört sayfa arasında ve TR/EN karşılığına giden bağlantılar vardır.
  Bağlantılar görelidir; dış bağımlılık yoktur.
