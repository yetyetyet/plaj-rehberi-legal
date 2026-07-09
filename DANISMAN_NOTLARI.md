# Danışman Notları — danisman-taslak Branch'i

Bu branch, Codex hukuki denetim bulgularına göre hazırlanan TASLAK metin
güncellemelerini içerir. **main'e merge edilmeden önce danışman onayı ve
aşağıdaki boşlukların doldurulması gerekir.** "Son güncelleme" tarihleri
bilinçli olarak DEĞİŞTİRİLMEDİ; yayın gününde güncellenecek.

## Değişiklik Özeti

### gizlilik.html
- (#16) Yeni kalem: "İşletme ve değişiklik talepleri" (ad-soyad, e-posta,
  opsiyonel telefon, not, ilgili koy; amaç + Supabase aktarımı).
- (#17) Yeni kalem: "Koy önerileri ve fotoğraflar" (onay öncesi private,
  onay sonrası herkese açık, hesap ilişkisi, ödül kaydı).
- (#18) Cihaz tanımlayıcısı: yalnız sıklık sınırı için işlendiği, kimlik
  verilerinden AYRI tutulduğu ve kimlikle ilişkilendirilmediği yazıldı
  (kod tarafında device_id talep kaydından ayrıldı — migration
  claim_rate_limit_decouple, 2026-07-07).
- (#20) Hesap bilgilerine şifre özeti, oturum bilgileri ve görünen adın
  e-postadan türetilebildiği eklendi.
- (#21) RevenueCat'e user ID iletildiği eklendi.
- (#22) Saklama Süreleri veri türü bazında tabloya çevrildi (süre
  boşlukları [DANIŞMAN] etiketli).
- (#23) "hata (çökme) kayıtları işlenebilir" cümlesi KALDIRILDI — kod
  teyidi: uygulamada hiçbir crash/analytics SDK'sı yok (Sentry,
  Crashlytics, Firebase vb. taranıp doğrulandı, 2026-07-07).
- (#24) Çocuk bölümü pazara uygunlaştırıldı (13 yaş kaldırıldı;
  veli/vasi izni ifadesi).
- (#15/#19) Yurt dışı aktarım ve konum bölümlerinin hukuki sebep
  cümleleri DEĞİŞTİRİLMEDİ; altlarına HTML yorumu olarak danışman
  sorusu gömüldü.

### kvkk-aydinlatma.html
- (#16, #17) Tabloya iki yeni satır: "Kullanıcı içeriği" ve "İşletme ve
  değişiklik talepleri" (hukuki sebep teyidi [DANIŞMAN]).
- (#18) İşlem güvenliği satırı: hata kayıtları çıkarıldı; cihaz
  tanımlayıcısının ayrı tutulduğu/kimlikle ilişkilendirilmediği eklendi;
  şifre özeti + oturum bilgileri eklendi (#20).
- (#21) Aktarım bölümüne RevenueCat user ID cümlesi.
- (#22) Saklama bölümü tabloya çevrildi ([DANIŞMAN] süre boşlukları).
- (#25) Başvuru bölümüne yöntem listesi + posta adresi yer tutucusu.
- (#15/#19) HTML yorumları (konum satırı altı + aktarım bölümü altı).

### kosullar.html
- (#11) 5 yeni madde işlendi (7-11): Kullanıcı İçeriği ve Lisans;
  İçerik Sorumluluğu ve Üçüncü Kişi Hakları; İçeriğin İncelenmesi ve
  Moderasyon (uygulama içi "İçeriği bildir" mekanizmasına atıf);
  Katkı Ödülleri (ilk onaylanan öneri, takdir hakkı, devredilemez,
  nakit karşılığı yok, Apple sponsor değildir); İşletme Sahipliği ve
  Değişiklik Talepleri. Eski 7-10 → 12-15 olarak yeniden numaralandı.
- (#12) Abonelik bölümüne cayma/dijital içerik istisnası TASLAK
  paragrafı ([DANIŞMAN] yer tutuculu).
- (Gelir modeli değişikliği, 2026-07-08) Yaz Sezonu Paketi satıştan
  kaldırıldı; §5 haftalık + AYLIK abonelik olarak güncellendi, sezon
  maddesi çıkarıldı ("Koy Pusulası" → "Sahil Pusulası" adı da düzeltildi).
  gizlilik.html satın alma kalemi de "haftalık veya aylık abonelik"
  olarak güncellendi. Paket gelecek yıl kampanya olarak dönerse madde
  geri eklenecek.

## Danışmana Sorulacaklar

1. **[Saklama süreleri]** Gizlilik §6 ve KVKK §5 tablolarındaki tüm
   süre boşlukları: işletme talepleri, koy önerileri/fotoğraflar,
   anonim kalabalık raporları, satın alma kayıtları için öneri.
2. **[Yayımlanan öneri içeriği]** Hesap silindiğinde yayımlanmış koy
   önerisi/fotoğraf rehber içeriği olarak kalabilir mi, yoksa
   silinmeli mi? (Taslakta "kalabilir + talep üzerine kaldırılır"
   yazıldı — teyit.)
3. **[Girişsiz akış rızası / m.9]** Kalabalık raporu ve işletme talebi
   girişsiz kullanılabiliyor; kayıt sırasındaki açık rıza bu akışları
   kapsamıyor. Yurt dışı aktarım için m.9 mekanizması: açık rıza mı,
   standart sözleşme mi? Konum işlemenin hukuki sebebi ne olmalı?
   (Metinlerdeki HTML yorumlarında işaretli.)
4. **[Talep formu hukuki sebebi]** KVKK tablosuna "talebinize bağlı
   işlem — m.5/2-c" yazıldı; doğru nitelendirme bu mu, m.5/2-f mi?
5. **[Tebligat adresi]** KVKK §7 yazılı başvuru için posta adresi.
6. **[Cayma istisnası ifadesi]** Koşullar §5'teki taslak paragrafın
   Mesafeli Sözleşmeler Yönetmeliği m.15/1-ğ'ye uygun kesin ifadesi.
7. **[VERBİS]** Veri sorumlusu (gerçek kişi) için VERBİS kayıt
   yükümlülüğü doğuyor mu? (Çalışan sayısı/bilanço eşikleri ve istisna
   kapsamı değerlendirilecek.)
8. **[Saklama ve imha politikası]** Ayrı bir saklama-imha politikası
   belgesi gerekli mi; tablo yeterli mi?
9. **[Vergi / mali müşavir]** Uygulama içi satış gelirleri (Apple
   komisyonu sonrası) için vergisel yükümlülükler ve fatura düzeni —
   mali müşavire yönlendirilecek; hukuki metinleri etkileyen bir sonuç
   çıkarsa (ör. satıcı unvanı/adresi) Koşullar'a işlenecek.
10. **[Çökme kayıtları — bilgi]** Kod teyidi yapıldı: uygulama hiçbir
    çökme/analitik verisi TOPLAMIYOR. Danışman paketindeki metinlerden
    "çökme kayıtları" ifadeleri bu branch'te çıkarıldı; danışmanın
    başka belgede kullanması gerekmiyor.
