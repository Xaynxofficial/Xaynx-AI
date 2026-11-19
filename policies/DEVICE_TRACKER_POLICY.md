> Resmî Canlı Sayfa: https://xaynxai.com/device-tracker-policy

Yürürlük Tarihi: 16 Kasım 2026 • Versiyon 1.0

# Cihaz takip merkezi politikası

İşbu Cihaz Takip Merkezi Güvenlik, Gizlilik ve Kullanım Politikası ("Politika"), Xaynx AI Teknoloji ("Şirket", "Xaynx AI", "biz" veya "hizmet") bünyesinde sunulan **Cihaz Takip Merkezi**(Device Tracker) servisinin çalışma esaslarını, coğrafi konum verilerinin işlenme standartlarını, donanımsal güvenlik tedbirlerini ve yasal kullanıcı sorumluluklarını açıklamaktadır.

**Sıfır-Bilgi (Zero-Knowledge) & Uçtan Uca Şifreleme (E2EE) Mimarisi:** Cihaz Takip Merkezi'nde konum koordinatlarınız ve donanım verileriniz cihazınızdan çıkmadan önce doğrudan tarayıcınızda 256-bit AES-GCM ile şifrelenir. Xaynx AI kendi güvenli sunucu altyapımızda ve izole veritabanlarımızda koordinatlarınız asla düz metin (plaintext) olarak tutulmaz; yalnızca şifreli bloklar (ciphertext) saklanır. Şifre çözme anahtarı sunucularımıza hiçbir zaman iletilmez; yalnızca sizin cihazınızda ve paylaşım linkinizin URL hash (#) parçasında izole kalır.

---

## 1. Gizlilik Politikası: Konum ve Cihaz Verilerinin İşlenmesi

Hizmetimiz, cihazınızın fiziksel konumunu harita üzerinde görselleştirmek ve kayıp/çalıntı durumlarında anlık kontrol sağlamak amacıyla aşağıdaki donanımsal verileri işler:

- **Coğrafi Koordinatlar:** WGS-84 formatındaki enlem, boylam, deniz seviyesinden rakım, anlık yön açısı (heading), hareket hızı (speed) ve hassasiyet yarıçapı (accuracy) bilgisi.
- **Cihaz ve Donanım Telemetrisi:** İşletim sistemi platformu (macOS, Windows, iOS, Android, Linux), tarayıcı motoru, CPU çekirdek sayısı, ekran çözünürlüğü ve Battery Status API üzerinden batarya yüzdesi ile şarj durumu.
- **Ağ ve Bağlantı Durumu:** Çevrimiçi/çevrimdışı (online/offline) bağlantı durumu, ağ gidiş-dönüş gecikme süresi (RTT) ve donanımın aktif ağ tipi (WiFi, hücresel veya ethernet).

Bu verilerin hiçbiri reklam ağlarıyla, veri brokerleriyle, analitik şirketleriyle veya Xaynx AI'ın kendi uzak sunucularıyla paylaşılmaz. Tüm koordinat hesaplamaları ve mesafe formülleri (Haversine) istemci tarafında (Client-Side) tamamlanır.

---

## 2. Konum Takip Politikası: GPS ve Gerçek Zamanlı Takip

Uygulamamızda **kesinlikle simülasyon, sahte (mock) veya varsayılan demo koordinatlar kullanılmaz**. Konum takibi kullanıcı güvenliğini ve doğruluğu en üst düzeye çıkarmak amacıyla çok kademeli gerçek donanım protokolleriyle yürütülür:

- **1. Aşama - Yüksek Hassasiyetli Donanım GPS:** Cihazın yerleşik GNSS/GPS yongasına veya işletim sistemi CoreLocation servisine doğrudan sorgu atılır (enableHighAccuracy: true). Uydu kilitlenmesi sağlandığında 3-15 metre arasında kusursuz konum elde edilir.
- **2. Aşama - Wi-Fi Triangulation ve Hibrit Mod:** Dizüstü bilgisayarlarda veya kapalı alanlarda uydu bağlantısı kurulamadığında sistem donma yaşamaksızın çevre Wi-Fi erişim noktaları ve baz istasyonu üçgenlemesiyle konumu doğrular.
- **3. Aşama - Doğrulanmış Fiziksel Ağ (IP) Konumu:** İşletim sistemi düzeyinde yetki gecikmesi veya GPS kısıtı oluştuğunda, kullanıcının talebiyle fiziksel modem IP adresi üzerinden gerçek şehir/bölge koordinatı temin edilir.

---

## 3. Kullanım Şartları: Kurallar ve Kullanıcı Sorumlulukları

Cihaz Takip Merkezi'ni başlatan veya paylaşım linki oluşturan her kullanıcı aşağıdaki yasal koşullara uymayı gayrikabili rücu kabul ve taahhüt eder:

- **Yalnızca Mülkiyet veya Yazılı Yetki:** Araç yalnızca kullanıcının bizzat sahip olduğu donanımlarda veya sahibinden açık yazılı ve hukuken geçerli takip yetkisi alınmış cihazlarda kullanılabilir.
- **Gizli İzleme ve Casusluk Kesinlikle Yasaktır (Stalking Yasağı):** Herhangi bir üçüncü şahsın haber ve rızası olmaksızın gizlice izlenmesi, izleme linkinin gizlice yüklenmesi veya takip edilmesi 5237 sayılı TCK m. 136 (Kişisel Verileri Hukuka Aykırı Olarak Ele Geçirme) ve TCK m. 123 (Kişilerin Huzur ve Sükununu Bozma) ile uluslararası mevzuata göre suçtur.
- **Acil Durum Özelliklerinin Kötüye Kullanımı:** Yüksek desibelli sesli siren (Acoustic Siren) ve ekran kilit modu yalnızca cihazın fiziki kaybı durumunda bulunması için tasarlanmıştır. Bu araçlar başkalarını taciz etmek veya cihaz kullanımını yetkisiz sabote etmek için kullanılamaz.

---

## 4. Veri Saklama ve Silme Politikası: Konum Geçmişi ve İmha

Konum geçmişi (Breadcrumb Trail) ve önbelleklenen koordinatlar üzerinde uygulanan veri tutma standartları şunlardır:

- **Maksimum 200 Noktalı FIFO Belleği:** Yerel cihaz geçmişinde en fazla son 200 konum noktası saklanır. 201. nokta eklendiğinde en eski konum otomatik olarak bellekten kalıcı şekilde imha edilir.
- **İzole LocalStorage Depolaması:** Konum geçmişi yalnızca 'xaynx_device_tracker_breadcrumbs' anahtarıyla tarayıcınızın kendi yerel alanında tutulur. Başka hiçbir web sitesi, eklenti veya sunucu bu veriye erişemez.
- **Tek Tıkla Anında Kalıcı İmha:** Kullanıcı arayüzdeki 'İzleri Temizle' butonuna bastığı saniye tüm coğrafi geçmiş, önbellek kayıtları ve donanım logları geri getirilemez biçimde silinir.

---

## 5. İzin ve Rıza Politikası: Donanım Yetkileri ve Tarayıcı Hakları

Cihaz Takip Merkezi donanım sensörlerine erişirken şu izin ve rıza mekanizmalarını işletir:

- **Zorunlu Kullanıcı Kimlik Doğrulaması (Authentication Gate):** Cihaz Takip Merkezi yalnızca doğrulanmış Xaynx AI hesabı ile oturum açmış kullanıcılar tarafından çalıştırılabilir. Oturum açmamış ziyaretçiler harita arayüzüne, donanım telemetrisine veya GPS sensörlerine erişemez; sistem tüm hassas bileşenleri DOM düzeyinde tamamen engelleyerek güvenli oturum açma sayfasına yönlendirir.
- **Ön Koşullu Onboarding ve Açık Rıza Onayı:** Kullanıcı ilk girişte güvenlik kurallarını ve işbu politikayı inceleyip onay kutusunu bizzat işaretleyerek onaylamadan önce tarayıcıda hiçbir konum izni istenmez, arka planda hiçbir veri aktarımı veya sensör sorgusu başlatılmaz.
- **Açık ve Bilinçli Konum İzni (Geolocation):** Kullanıcı tarayıcının yerel 'Konum Paylaşımına İzin Verilsin mi?' diyalog kutusunda 'İzin Ver' seçeneğini tıklamadıkça hiçbir koordinat sorgusu tetiklenmez.
- **Kullanıcı Tetiklemeli Ses İzni (Web Audio API):** Tarayıcı güvenlik kuralları uyarınca akustik alarm (siren) kullanıcının doğrudan 'Ses Çal' butonuna tıklaması olmaksızın otomatik veya gizlice çalamaz.
- **Rızanın Her An İptal Edilebilmesi:** Kullanıcı tarayıcının adres çubuğundaki kilit (veya ayarlar) simgesine tıklayarak konum iznini dilediği an iptal edebilir. İptal anında takip anında sonlanır.

---

## 6. Güvenlik Politikası: Yetkisiz Erişime Karşı Kriptografik Koruma

Cihaz bilgileri ve paylaşımlı takip mekanizmaları askeri seviyede kriptografik standartlarla korunmaktadır:

- **256-Bit Kriptografik Rastgelelik (Web Crypto API):** Cihaz takip kodları ve paylaşım belirteçleri standart sözde-rastgele fonksiyonlar yerine crypto.getRandomValues donanım entropisiyle 256-bit karmaşıklıkta üretilir.
- **Hash-Fragment İzolasyonu (RFC 3986):** Paylaşım linkinde yer alan anahtarlar URL'nin '#' parçasında saklanır. İnternet standartları gereği bu bölüm HTTP isteklerinde sunuculara veya erişim günlüklerine asla gönderilmez.
- **Tek Yönlü SHA-256 PIN Özeti:** Kayıp Modu kilit ekranı için belirlediğiniz PIN şifresi düz metin olarak asla tutulmaz; yalnızca tek yönlü kriptografik SHA-256 özeti bellekte doğrulanır.
- **Uzaktan Kayıp Modu ve Acil İletişim Notu:** Cihaz sahibi acil durumlarda ekranı anında kilitleyerek bulan kişiye yönelik güvenli bir kurtarma mesajı ve opsiyonel irtibat telefon numarası gösterebilir. Cihaz sahibi dilerse panelden tek tıkla veya cihaz başında PIN doğrulaması ile kilidi güvenle kaldırabilir.
- **Coğrafi Çit (Geofence) Güvenlik Çemberi:** Kullanıcılar cihaz etrafında 100m ile 1000m arasında sanal bir güvenlik alanı tanımlayabilir. Cihaz bu sınırın dışına çıktığında istemci tarafında anlık Haversine analizi yapılarak acil durum uyarısı oluşturulur.
- **Arka Plan Canlılığı ve Donanım Koruması (Keep-Alive):** İşletim sistemlerinin sekme uyutması nedeniyle GPS takibinin durmasını önlemek amacıyla yerel Screen WakeLock API ve ultra-düşük frekanslı ses tamponu kullanılır; harici casus yazılım veya arka plan sürücüsü asla yüklenmez.

---

## 7. Çocukların Gizliliği Politikası (COPPA & GDPR-K Uyumu)

Çocukların dijital mahremiyeti ve fiziki güvenliği en hassas olduğumuz alanlardan biridir:

- **Zorunlu Ebeveyn / Kanuni Vasi Denetimi:** 18 yaşından küçük bireylere ait cihazların takip edilmesi yalnızca kanuni veli veya vasinin açık izni, doğrudan gözetimi ve çocuğun güvenliği amacıyla yapılabilir.
- **Sıfır Profilleme ve Ticari Hedefleme Yasağı:** Çocuklara ait hiçbir konum geçmişi veya cihaz bilgisi reklam hedeflemesi, ticari profilleme ya da veri madenciliği amacıyla işlenemez ve üçüncü taraflara satılamaz.
- **Yetkisiz Çocuk Takibinin Cezai Sorumluluğu:** Yasal velisi veya vasisi olunmayan çocukların cihazlarına herhangi bir takip mekanizması kurulması hem ulusal hem de uluslararası ceza yasalarına göre ağır suç teşkil eder.

---

## 8. Hesap ve Veri Silme Politikası: Kalıcı Dijital İmha

Kullanıcılar cihaz takip verilerini istedikleri her an kendi kontrolleriyle sıfırlama hakkına sahiptir:

- **Panel Üzerinden Anlık Sıfırlama:** Cihaz paneli içerisindeki 'İzleri Temizle' butonuna tıklanmasıyla birlikte mevcut tüm ekmek kırıntıları ve konum geçmişi derhal sıfırlanır.
- **Kriptografik Kimliklerin Yok Edilmesi:** Tarayıcı çerezlerini ve yerel depolamayı (Site Verilerini Temizle) sildiğiniz anda cihazınıza atanan rastgele XY- kimliği kalıcı olarak yok olur ve yeniden oluşturulamaz.
- **Sunucu Tarafında Sıfır Artık (Zero Server Footprint):** Xaynx AI sunucularında cihazınıza veya koordinatlarınıza ait hiçbir kayıt tutulmadığı için yerel belleğinizi temizlemeniz ardınızda mutlak sıfır dijital ayak izi bırakır.

---

## Bize Ulaşın

Cihaz Takip Merkezi güvenlik standartları, donanım uyumluluğu veya bu politika ile ilgili her türlü soru ve teknik bildirimleriniz için Güvenlik ve Uyumluluk Ekibimizle iletişime geçebilirsiniz:

[contact@xaynx.com](mailto:contact@xaynx.com)

Xaynx AI Teknoloji A.Ş. • Cihaz Güvenliği & Kriptografi Birimi
