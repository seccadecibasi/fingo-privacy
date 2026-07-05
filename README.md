# Fingo Gizlilik Politikası

**Son güncelleme:** Temmuz 2026

Fingo ("uygulama") olarak kullanıcılarımızın gizliliğine önem veriyoruz. Bu politika, uygulamamızı kullanırken hangi verileri topladığımızı, nasıl kullandığımızı ve nasıl koruduğumuzu açıklar.

---

## 1. Topladığımız Veriler

### Hesap Bilgileri
- E-posta adresi (kayıt ve giriş için)
- İsim, yaş, cinsiyet, mahalle (profil için, isteğe bağlı)
- Profil fotoğrafı ve galeri fotoğrafları (isteğe bağlı)

### Konum Bilgisi
- Uygulama açıkken yakındaki ilanları göstermek için anlık konum kullanılır.
- Konumunuz sunucularımızda saklanmaz; yalnızca ilan oluştururken seçtiğiniz mekan koordinatı kaydedilir.

### İlan ve Mesaj Verileri
- Oluşturduğunuz ilanlar (mekan adı, başlık, açıklama)
- Diğer kullanıcılarla yaptığınız mesajlaşmalar

### Cihaz Bilgisi
- Push bildirimi göndermek için Firebase Cloud Messaging (FCM) token'ı

---

## 2. Verileri Nasıl Kullanıyoruz

- Yakınındaki ilanları haritada göstermek
- Kullanıcılar arasında eşleşme ve mesajlaşma sağlamak
- İlan süresi dolduğunda bildirim göndermek
- Uygulama güvenliğini ve içerik moderasyonunu sağlamak

### Eşleşme ve Mesajlaşma Kuralları

- Bir kullanıcı sizi eşleşmeden çıkardığında, kullanıcı güvenliği gereği o kullanıcının ilanlarına tekrar mesaj gönderemezsiniz. Bu kural geçmiş konuşma kayıtları üzerinden otomatik uygulanır.

### İçerik Kuralları ve Moderasyon

- **Fotoğraf kısıtlaması:** Kullanıcılar yalnızca kendilerine ait profil ve galeri fotoğrafı yükleyebilir. Başka kişilere (ör. ilanda aradığınız kişi) veya mekanlara ait fotoğraf yüklemek yasaktır; uygulama bu tür yüklemelere teknik olarak izin vermez.
- **Sohbet içi tek seferlik fotoğraf:** Karşılıklı eşleşme gerçekleştikten sonra, sohbet ekranından kamera veya galeriden tek seferlik görüntülenmek üzere fotoğraf gönderilebilir. Gönderilen fotoğraf, alıcı tarafından açılıp görüntülendiği anda erişime kapatılır ve kısa süre içinde sunucularımızdan kalıcı olarak silinir; bir daha kimse tarafından görüntülenemez. Fotoğrafın kameradan mı galeriden mi gönderildiği, görüntülenirken karşı tarafa gösterilir. Ekran görüntüsü alınması teknik olarak engellenmez; ancak bir kullanıcı ekran görüntüsü aldığında karşı taraf bilgilendirilir. **İstisna:** bir fotoğraf karşı taraf tarafından bildirilirse, o fotoğraf kanıt olarak moderasyon amacıyla saklanır ve otomatik silme uygulanmaz.
- **İlan sınırları:** Bir kullanıcı bir günde en fazla 3 ilan açabilir ve aynı anda en fazla 10 aktif ilana sahip olabilir. Bu sınırlar spam ve kötüye kullanımı önlemek için sunucu tarafında uygulanır.
- **Şikayet mekanizması:** Her kullanıcı, uygunsuz bulduğu bir ilanı gerekçe seçerek bildirebilir. Farklı kullanıcılardan gelen bildirimler eşiği aştığında ilan otomatik olarak gizlenir ve sahibine geçici ilan verme kısıtlaması uygulanır. Bildirimler kötüye kullanıma karşı saatlik ve günlük kotalarla sınırlandırılmıştır.
- İlan başlığı ve açıklamaları; hakaret, kişisel bilgi paylaşımı ve benzeri ihlallere karşı otomatik olarak denetlenir.

---

## 3. Verilerinizi Kimlerle Paylaşıyoruz

Kişisel verilerinizi üçüncü taraflara satmıyoruz. Yalnızca hizmet altyapısı için aşağıdaki servisler kullanılmaktadır:

| Servis | Amaç |
|--------|------|
| **Supabase** | Veritabanı ve dosya depolama |
| **Firebase** | Kimlik doğrulama ve push bildirimleri |
| **Render** | Backend API sunucusu |
| **Cloudflare R2** | Fotoğraf depolama |

**Yasal makamlarla paylaşım:** Kişisel verileriniz, yukarıdaki altyapı sağlayıcıları dışında hiçbir kişi veya kurumla paylaşılmaz — yalnızca mahkeme, savcılık veya kolluk kuvvetleri gibi yetkili bir yasal makamın geçerli bir talebi olması hâlinde, talep edilen ölçüde paylaşılır.

---

## 4. Verilerinizi Nasıl Saklıyoruz

- Tüm veriler şifreli bağlantı (HTTPS) üzerinden iletilir.
- Fotoğraflar güvenli bulut depolamada saklanır.
- Mesajlar yalnızca ilgili kullanıcılar tarafından görülebilir.

---

## 5. Haklarınız

Dilediğinizde:
- Hesabınızı ve tüm verilerinizi silebilirsiniz. İki yoldan biriyle:
  - **Uygulama içinden:** Profil → Ayarlar → Hesap Ayarları → Hesabı Kalıcı Sil
  - **Uygulamayı açmadan:** fingosupport@gmail.com adresine e-posta hesabınızla
    birlikte "Hesabımı silmek istiyorum" yazarak talep edebilirsiniz
  - Her iki yoldan da silme talebi 30 günlük bir bekleme süresine alınır; bu
    süre içinde tekrar giriş yaparsanız talep otomatik iptal olur. Süre
    sonunda hesabınız, ilanlarınız, fotoğraflarınız ve mesajlarınız kalıcı
    olarak silinir. Silme sonrasında, yasal bir veri talebine cevap
    verebilmek için yalnızca kişisel veri içermeyen minimal bir kayıt
    (hesabın ne zaman var olup ne zaman silindiği) tutulur.
- Verilerinize erişim veya düzeltme talep edebilirsiniz
- Konum iznini istediğiniz zaman cihaz ayarlarından iptal edebilirsiniz

---

## 6. Çocukların Gizliliği

Fingo 18 yaş altı kullanıcılara yönelik değildir. 18 yaş altı kullanıcıların verilerini bilerek toplamıyoruz.

---

## 7. Değişiklikler

Bu politikayı zaman zaman güncelleyebiliriz. Önemli değişikliklerde kullanıcılar bildirim yoluyla bilgilendirilir.

---

## 8. İletişim

Gizlilik ile ilgili sorularınız için:

**E-posta:** fingosupport@gmail.com

---

*Bu gizlilik politikası Türkiye'de geçerli olan 6698 sayılı Kişisel Verilerin Korunması Kanunu (KVKK) kapsamında hazırlanmıştır.*
