[English version below ↓ / İngilizce sürüm aşağıda](#privacy--safety-by-design--fingo)

# Fingo — Privacy & Safety by Design

**Son güncelleme:** Temmuz 2026

Fingo, **mekâna bağlı anonim bir ilan panosudur** — Fingo'nun temel amacı bir flört veya eşleşme platformu olmak değildir. Kaybettiğin bir eşyayı, kaçırdığın bir evcil hayvanı ya da tanışamadığın birini, o anı yaşadığın mekâna bağlı bir ilanla arayabilirsin. Bu sayfa, uygulamanın temel tasarım kararlarının **neden** böyle olduğunu, sade bir dille açıklıyor. Ayrıntılı, hukuki dille yazılmış tam metin için [Gizlilik Politikası](README.md)'na bakabilirsiniz.

Bu ilkeler; Türkiye'de 6698 sayılı KVKK, Avrupa Birliği'nde GDPR ve Amerika Birleşik Devletleri'nde CCPA/CPRA'nın ortak temel prensipleriyle (veri minimizasyonu, amaç sınırlaması, varsayılan olarak gizlilik — "privacy by default") uyumlu olacak şekilde tasarlanmıştır.

## Neden böyle tasarlandı?

Fingo geliştirilirken temel hedef yalnızca kullanıcı gizliliğini korumak değil, aynı zamanda uygulamayı kullanmayan kişilerin gizliliğini de korumaktı. Bu nedenle uygulama; veri minimizasyonu, varsayılan olarak gizlilik (privacy by default), amaç sınırlaması ve kötüye kullanımı önlemeye yönelik teknik kontroller esas alınarak tasarlanmıştır.

---

### 1) Neden herkes başta bir kuğu olarak görünüyor (anonimlik)?

Çünkü Fingo'da varsayılan durum **gizliliktir**, açıklık değil. Bir ilana yanıt verdiğinde, karşı taraf gerçek adını, yaşını, fotoğrafını göremez — sadece rastgele üretilmiş bir "kuğu kimliği" (ör. "Dişi Kuğu #0421") görür. Bu, veri koruma hukukundaki "varsayılan olarak gizlilik" (privacy by default) ilkesinin doğrudan uygulanmasıdır: kişisel verinizi paylaşmanız için bilinçli bir adım (karşılıklı bağlantı) atmanız gerekir, sistem bunu sizin adınıza otomatik yapmaz.

### 2) Neden fotoğraf paylaşımı karşılıklı bağlantı kurulmadan açılmıyor?

Çünkü fotoğraf, bir kişiyi doğrudan teşhis etmenin en güçlü yoludur. Fingo, iki taraf da birbirini onaylamadan (karşılıklı "bağlantı" kurulmadan) hiçbir fotoğrafı karşı tarafa göstermez — bu kural istemci tarafında bir arayüz kısıtlaması değil, **sunucu tarafında zorunlu kılınan** bir kuraldır (`conversations.status = 'accepted'` olmadan fotoğraf uç noktası isteği reddeder). Bağlantı kurulduktan sonra bile fotoğraflar yalnızca tek seferlik açılabiliyor ve açıldığı anda sunucudan kalıcı olarak siliniyor.

### 3) Neden ilanlar süreli ve kendiliğinden siliniyor?

Çünkü veri koruma hukukunun temel ilkelerinden biri **veri minimizasyonu ve saklama sınırlaması**dır — bir veri, amacı sona erdiğinde saklanmamalıdır. Fingo'da ilanlar varsayılan olarak 24 saat sonra süresi dolar ve otomatik bir arka plan görevi (sweep) tarafından temizlenir. Aradığını bulan bir kullanıcı ilanını istediği an manuel olarak da kaldırabilir; bağlantı kurulduktan 5 dakika sonra kullanıcıya bunu hatırlatan bir bildirim gönderilir.

### 4) Neden isim, telefon numarası veya sosyal medya hesabı paylaşımı yasak?

Çünkü bu bilgiler, anonimlik korumasını tamamen anlamsız kılan doğrudan kimlik teşhis verileridir. İlan gönderilirken metin, kimlik tespitine yardımcı olabilecek ifadeler ve iletişim bilgileri için otomatik filtrelerden geçirilir; bu tür içerik tespit edilirse ilan **hiçbir bypass seçeneği olmadan** gönderilemez — kullanıcının içeriği düzenlemesi zorunludur.

### 5) Neden tek taraflı erişim yok, karşılıklı onay ("bağlantı") şart?

Çünkü kimliği açığa çıkarma kararı, tek bir kullanıcının değil, **her iki tarafın da rızasına** bağlı olmalıdır. Bir kullanıcı "bu doğru kişi/durum" deyip onay verse bile, karşı taraf da aynı onayı vermeden hiçbir profil bilgisi veya fotoğraf açılmaz. Bu tasarım, kimlik bilgilerinin yalnızca her iki tarafın da bilinçli tercihiyle görünür hâle gelmesini sağlayan "privacy by design" yaklaşımının bir parçasıdır.

### 6) Neden aynı mekana ilan verme sıklığı sınırlanıyor?

Çünkü bir kullanıcının aynı mekana kısa aralıklarla tekrar tekrar ilan vermesi, o mekanı gerçek bir arayış dışında bir amaçla (ör. birini izleme/takip etme) kullandığının bir işareti olabilir. Bu yüzden aynı kullanıcı aynı mekana (150 metre yarıçap + mekan adı eşleşmesi ile tanımlanan) 24 saatte en fazla 2, 7 günde en fazla 4 ilan verebilir; aynı başlık+açıklama 30 gün içinde tekrar paylaşılamaz. Bu sınırlar sunucu tarafında zorunlu kılınır, kullanıcı arayüzünde atlanabilecek bir uyarı değildir.

### 7) Neden moderasyon ve şikayet mekanizması var?

Çünkü kullanıcı tarafından oluşturulan her platformda kötüye kullanım riski vardır ve bu riski azaltmak platformun sorumluluğundadır. Her ilan metni; hakaret ve kişisel bilgi sızıntısı yönünden otomatik olarak taranır. Ayrıca **hassas mekan türlerinde ilan vermeye baştan izin verilmez**: anaokulu, ilkokul, ortaokul, lise gibi eğitim kurumları, hastane/sağlık kuruluşları, karakol/adliye/valilik gibi kamu kurumları ve cami/kilise gibi ibadet yerlerinde "İlan ver" seçeneği hem uygulama arayüzünde hem de sunucu tarafında (ikinci bir savunma katmanı olarak) kapalıdır. **Üniversiteler bu kısıtlamanın dışındadır** — kampüsler gerçek sosyal buluşma alanları olduğu için, adında "okul" geçen bir kelime bulunsa bile (ör. "... Üniversitesi Mühendislik Fakültesi") üniversite/yüksekokul/fakülte/akademi olarak tanınan mekanlarda ilan vermeye izin verilir; bu bilinçli bir istisnadır, K-12 eğitim kurumlarındaki (küçük yaştaki öğrenciler) hassasiyet üniversite kampüslerine aynı ölçüde uygulanmaz. Kullanıcılar ayrıca bir ilanı gerekçeyle bildirebilir; 3 farklı kullanıcının bildirdiği bir ilan otomatik gizlenir ve sahibine 7 günlük ilan yasağı uygulanır. Saatlik/günlük bildirim kotaları, bildirim mekanizmasının kötüye kullanılmasını (spam şikayet) da engelliyor.

### 8) Fingo bir tanışma/flört uygulaması mı?

Fingo'nun temel amacı bir flört veya eşleşme platformu olmak değildir — **mekâna bağlı anonim bir ilan panosudur**. İnsan aramanın yanı sıra kaybolan evcil hayvan, kaybedilen eşya gibi günlük hayatta sık karşılaşılan durumlar için de aynı mekanizmayla kullanılır (ör. taksi durağında düşürülen bir cüzdan, parkta kaçan bir köpek). İlan verirken bir kategori (Kişi / Evcil Hayvan / Kayıp Eşya / Diğer) seçilir. Romantik/insan arama, uygulamanın sunduğu kullanım senaryolarından biridir — iki kullanıcı bu yolla gerçekten tanışabilir, ama bu uygulamanın merkezî amacı değil, ortaya çıkabilecek sonuçlardan sadece biridir.

### 9) Verileriniz üzerinde hangi haklara sahipsiniz?

Fingo; yürürlükteki veri koruma düzenlemelerinin (KVKK, GDPR, CCPA/CPRA gibi) öngördüğü kullanıcı haklarını, uygulanabildiği ölçüde desteklemeyi hedefler: verilerinize erişim talep etme, yanlış verinin düzeltilmesini isteme, işlemeye itiraz etme ve hesabınızı — dolayısıyla tüm kişisel verilerinizi — kalıcı olarak sildirme. Silme talebi uygulama içinden veya e-posta ile yapılabilir, 30 günlük bir bekleme süresinin ardından kalıcı olarak uygulanır. Ayrıntılar için [Gizlilik Politikası, Bölüm 5/7](README.md#5-haklarınız).

### 10) Kötüye kullanım (stalking, taciz) şüphesi olursa ne oluyor?

Fingo, bir kişinin rızası dışında izlenmesi, taciz edilmesi veya sistematik olarak takip edilmesi amacıyla kullanılmak üzere **tasarlanmamıştır** ve kullanım koşulları bunu açıkça yasaklar. Teknik sınırlamalar ve içerik politikaları (anonimlik, karşılıklı onay, aynı-mekan sınırları, kimlik-tespit-eden-içerik engeli, moderasyon) bu tür kötüye kullanımları önlemeyi amaçlar. Şüpheli bir kullanım fark edilirse hesap askıya alınabilir; gerektiğinde ve yalnızca yetkili bir yasal makamın (mahkeme, savcılık, kolluk kuvveti) geçerli bir talebi olması hâlinde ilgili veri paylaşılır — bu dışında verileriniz hiçbir üçüncü tarafla paylaşılmaz.

---

## Privacy by Design

Fingo'da gizlilik sonradan eklenmiş bir özellik değil, uygulamanın ilk tasarım kararlarından biridir. Kimliklerin gizlenmesi, karşılıklı eşleşme zorunluluğu, otomatik silinen ilanlar, içerik filtreleri ve sunucu tarafında uygulanan erişim kontrolleri bu yaklaşımın parçalarıdır.

---

**İletişim:** fingosupport@gmail.com

---
---

# Privacy & Safety by Design — Fingo

**Last updated:** July 2026

Fingo is a **location-bound, anonymous bulletin board** — its core purpose is not to be a dating or matchmaking platform. You can post about someone you saw, a pet you lost, or an item you dropped, tied to the real venue where it happened. This page explains, in plain language, **why** the app's core design decisions are what they are. For the full legal text, see the [Privacy Policy](README.md).

These principles are designed to align with the shared core ideas behind Turkey's KVKK, the EU's GDPR, and the US CCPA/CPRA — data minimization, purpose limitation, and privacy by default.

## Why was it designed this way?

While building Fingo, the goal was not only to protect the privacy of our users, but also the privacy of people who don't use the app at all. That's why the app is built around data minimization, privacy by default, purpose limitation, and technical controls aimed at preventing misuse.

---

### 1) Why does everyone start out as an anonymous swan?

Because privacy is Fingo's **default** state, not openness. When you respond to a post, the other person cannot see your real name, age, or photo — only a randomly generated "swan identity" (e.g. "Female Swan #0421"). This is a direct application of the "privacy by default" principle in data-protection law: sharing personal data requires a deliberate step (mutual connection) — the system never does it for you automatically.

### 2) Why is photo sharing locked until a mutual connection is made?

Because a photo is one of the strongest ways to directly identify someone. Fingo never reveals a photo to the other side until both parties have confirmed each other — this is enforced **server-side**, not just hidden in the UI (the photo endpoint rejects the request unless `conversations.status = 'accepted'`). Even after connecting, photos can only be opened once and are permanently deleted from the server the moment they're viewed.

### 3) Why do posts expire and delete themselves?

Because data minimization and storage limitation are core data-protection principles — data shouldn't be retained once its purpose has ended. Posts on Fingo expire after 24 hours by default and are cleared by an automated background sweep. A user who found what they were looking for can also remove their post manually at any time; a reminder notification is sent 5 minutes after a connection is made.

### 4) Why are names, phone numbers, and social media handles banned from posts?

Because these are direct identifying data points that would defeat the whole point of the anonymity protection. Post text is automatically run through filters for language that could help identify someone and for contact-info patterns; if detected, the post **cannot be submitted at all, with no bypass** — the user must edit the content first.

### 5) Why is mutual confirmation ("connection") required instead of one-sided access?

Because the decision to reveal identity should never rest with just one person — it requires **both** parties' consent. Even if one user says "yes, this is them," nothing is revealed until the other person gives the same confirmation. This design is part of a "privacy by design" approach, where identifying information only becomes visible through a deliberate choice made by both sides.

### 6) Why is posting about the same venue rate-limited?

Because repeatedly posting about the same venue in a short time span can be a sign the venue is being used for something other than a genuine search — such as watching or following someone. A user can post about the same venue (matched by a 150-meter radius plus venue name) at most twice in 24 hours and four times in 7 days; identical title+description text can't be reposted within 30 days. These limits are enforced server-side, not a dismissible UI warning.

### 7) Why is there moderation and a reporting system?

Because any user-generated-content platform carries a risk of misuse, and reducing that risk is the platform's responsibility. Every post's text is automatically scanned for insults and leaked personal information. In addition, **posting is blocked outright at certain sensitive venue types**: schools (kindergarten through high school), hospitals/healthcare facilities, government buildings (police stations, courthouses, government offices), and places of worship — the "Create post" option is disabled both in the app UI and, as a second line of defense, on the server. **Universities are explicitly exempt from this restriction** — campuses are genuine social gathering spaces, so a venue name containing a word like "school" (e.g. "... University School of Engineering") is still allowed to post at, as long as it's recognized as a university/college/faculty/academy; this is a deliberate exception, since the sensitivity around K-12 institutions (involving minors) doesn't apply the same way to university campuses. Users can also report a post with a reason; once 3 different users report the same post, it is auto-hidden and the owner receives a 7-day posting ban. Hourly/daily report quotas also prevent the reporting mechanism itself from being abused.

### 8) Is Fingo a dating app?

Fingo's core purpose is not to be a dating or matchmaking platform — it's a **location-bound, anonymous bulletin board**. Alongside looking for a person, the same mechanism is used every day for lost pets and lost items (a wallet dropped at a taxi stand, a dog that escaped in a park). When creating a post, you choose a category (Person / Pet / Lost Item / Other). Finding a person is one of the possible use cases — two people can genuinely meet through it — but it isn't the app's central purpose, just one of the outcomes that can happen.

### 9) What rights do you have over your data?

Fingo aims to support the user rights set out by applicable data protection regulations (such as KVKK, GDPR, and CCPA/CPRA), to the extent they apply: requesting access to your data, requesting correction of inaccurate data, objecting to processing, and permanently deleting your account — and with it, all your personal data. Deletion can be requested in-app or by email, and takes effect after a 30-day grace period. See [Privacy Policy, Section 7](README.md#7-your-rights-gdpr--kvkk) for details.

### 10) What happens if misuse (stalking, harassment) is suspected?

Fingo is **not designed** to be used for monitoring, harassing, or systematically tracking someone without their consent, and this is explicitly prohibited by our terms. Technical limitations and content policies (anonymity, mutual consent, same-venue limits, the identifying-content block, moderation) are aimed at preventing this kind of misuse. If suspicious use is detected, the account may be suspended; data is shared with a third party only when a competent legal authority (a court, prosecutor, or law enforcement agency) makes a valid request — otherwise, your data is never shared with anyone outside our infrastructure providers.

---

## Privacy by Design

Privacy on Fingo isn't a feature bolted on afterward — it's one of the app's earliest design decisions. Hidden identities, mandatory mutual matching, self-expiring posts, content filters, and server-side access controls are all part of that approach.

---

**Contact:** fingosupport@gmail.com
