> Resmî Canlı Sayfa: https://xaynxai.com/google-privacy-policy

Google Veri GüvenliğiApplication: xaynx(Xaynx AI Teknoloji A.Ş.)

# Google API ve Workspace Kullanıcı Verileri Gizlilik Politikası

Effective Date: November 16, 2026•Last Updated: November 16, 2026•Doc ID: XAYNX-GOOGLE-PRIV-2026/V2•Google Sınırlı Kullanım (Limited Use) Standartlarına Tam Uyum
Google API Hizmetleri Kullanıcı Verisi Politikası (Sınırlı Kullanım Beyanı)"Xaynx AI's (application name: **xaynx**) use and transfer of information received from Google APIs to any other app will adhere to the [Google API Services User Data Policy](https://developers.google.com/terms/api-services-user-data-policy), including the Limited Use requirements. Xaynx AI does NOT use data obtained from Google Workspace APIs to develop, improve, or train generalized or foundation AI/ML models."

## 1. Kapsam ve Uygulama Kimliği

Bu politika; Xaynx AI Teknoloji A.Ş. tarafından geliştirilen "xaynx" (veya "Xaynx AI") uygulamasının, Google OAuth 2.0 kimlik doğrulama protokolü ve Google Workspace API'leri (özellikle Gmail API) vasıtasıyla eriştiği kullanıcı verilerinin nasıl toplandığını, kullanıldığını, korunduğunu, saklandığını ve imha edildiğini düzenler.

Uygulamamız, Google verilerine yalnızca kullanıcının açık rızası ve onay düğmesine basması ile erişir. Yetkilendirme isteğe bağlıdır ve kullanıcı dilediği an bu erişimi kesebilir.

## 2. Talep Edilen Google OAuth İzinleri ve İşleme Amaçları

Xaynx AI, Yalnızca Asgari Veri İlkesi (Data Minimization) çerçevesinde aşağıdaki izinleri talep eder:

| OAuth Scope | Erişilen Veri | Kullanım Amacı |
| --- | --- | --- |
| https://www.googleapis.com/auth/gmail.readonly | E-posta başlıkları, konu, gönderici ve mesaj içeriği | Kullanıcının talep ettiği gelen kutusu iletilerini listelemek, aramak ve kullanıcının isteği üzerine e-posta özetleri sunmak. |
| https://www.googleapis.com/auth/gmail.send | Kullanıcı tarafından hazırlanan e-posta taslağı | Yalnızca kullanıcının 'Gönder' butonuna açık onayı ile hazırlanan e-postayı kullanıcının kendi hesabı üzerinden göndermek. |
| https://www.googleapis.com/auth/gmail.compose | E-posta taslakları | Kullanıcı için taslak e-postalar oluşturmak ve düzenlenebilir taslaklar kaydetmek. |
| https://www.googleapis.com/auth/gmail.modify | E-posta etiketleri ve okundu durumu | Kullanıcı isteğiyle e-postaları okundu işaretlemek veya etiket düzenlemesi yapmak. |
| https://www.googleapis.com/auth/calendar.events | Takvim etkinlikleri, toplantı saatleri ve davetliler | Kullanıcının talimatıyla takvime yeni toplantı, hatırlatıcı ve etkinlik eklemek veya güncellemek. |
| https://www.googleapis.com/auth/calendar.readonly | Yaklaşan takvim etkinlikleri ve takvim listesi | Kullanıcının günlük programını ve yaklaşan randevularını arayüzde görüntülemek ve çakışmaları analiz etmek. |
| https://www.googleapis.com/auth/drive.readonly | Seçilen Drive dokümanları, PDF ve metin dosyaları | Kullanıcının seçtiği dokümanları okumak, içerik özetlemek ve yapay zeka ile doküman analizi yapmak. |
| https://www.googleapis.com/auth/drive.file | Xaynx AI ile oluşturulan veya paylaşılan dosyalar | Kullanıcının Xaynx AI üzerinden oluşturduğu rapor, doküman ve dosyaları kendi Google Drive'ına kaydetmek. |
| userinfo.email, userinfo.profile & openid | E-posta adresi, isim, profil fotoğrafı ve benzersiz kullanıcı ID'si | Kullanıcı kimliğini doğrulamak, güvenli oturum açmak ve arayüzde doğru kullanıcı profilini görüntülemek. |

## 3. Veri Depolama, Saklama ve Güvenlik Esasları

**Sıfır Kalıcı Sunucu Depolaması:** Xaynx AI, kullanıcıların Gmail e-posta gövdelerini, eklerini veya kişisel yazışmalarını harici merkezi veritabanı sunucularında kalıcı olarak saklamaz. E-postalar doğrudan Google API'leri üzerinden güvenli şifreli kanallarla (TLS 1.3) anlık olarak çekilir, kullanıcının yerel tarayıcı oturum belleğinde (in-memory) geçici olarak işlenir ve oturum kapandığında bellekten tamamen silinir.

**Yetkilendirme Anahtarları:** Google OAuth erişim belirteçleri (tokens), kullanıcının kendi cihazındaki yerel tarayıcı depolamasında tutulur; çoklu cihaz senkronizasyonu aktif edildiğinde ise yalnızca kullanıcının kendi hesabına bağlı izole bulut oturum kaydında şifreli olarak saklanır. Kullanıcı çıkış yaptığında veya bağlantıyı kestiğinde anahtarlar anında silinir.

4. Yapay Zeka Modeli Eğitimi Kesin YasağıGoogle Workspace ve Gmail API'lerinden elde edilen veriler; hiçbir koşulda genel amaçlı, kamuya açık veya kişiselleştirilmemiş temel yapay zeka, makine öğrenimi veya büyük dil modellerini (LLM) eğitmek, ince ayar (fine-tuning) yapmak ya da geliştirmek amacıyla KULLANILMAZ ve üçüncü taraflara aktarılmaz.

## 5. Üçüncü Taraflarla Paylaşım ve Satış Yasağı

- **Reklam ve Pazarlama Yasağı:** Google kullanıcı verileri hiçbir reklam ağına, reklam hedefleme motoruna veya pazarlama platformuna aktarılmaz.
- **Veri Satışı Yasağı:** Google kullanıcı verileri hiçbir kişi, kurum veya veri simsarına satılamaz, kiralanamaz veya takas edilemez.
- **İnsan Tarafından İnceleme Sınırlaması:** Şirket çalışanlarımız kullanıcıların e-posta içeriklerini okuyamaz veya inceleyemez. Yalnızca kullanıcının açık teknik destek talebi veya yasal zorunluluk halleri istisnadır.

## 6. Erişim İptali ve Veri İmhası (Revocation & Deletion)

Kullanıcılar, Xaynx AI'a verdikleri Google erişim yetkisini iki kolay yöntemle anında sonlandırabilirler:

**Yöntem 1: Uygulama İçi Bağlantı Kesme**Ayarlar > Bağlantılar sekmesine gidin ve Gmail kartındaki 'Bağlantıyı Kes' düğmesine tıklayın. Bu işlem yerel tüm token'ları ve oturum verilerini derhal siler.

**Yöntem 2: Google Hesap Güvenliği**Doğrudan [Google İzinler Sayfası](https://myaccount.google.com/permissions) üzerinden \"xaynx\" uygulamasının erişimini tek tıkla iptal edebilirsiniz.

## 7. İletişim ve Resmi Başvurular

Google API veri taahhütlerimiz, gizlilik sorularınız veya veri silme talepleriniz için resmi iletişim kanallarımız:

Xaynx AI Teknoloji A.Ş.

Email: [contact@xaynx.com](mailto:contact@xaynx.com)

General Privacy Policy: [https://xaynxai.com/privacy](/privacy)
