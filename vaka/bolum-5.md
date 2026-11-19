# Bölüm 5 — "Artık yazıya dökme zamanı"

## Durum

Karar verildi: Bir sonraki çeyrekte Agent Oluşturucu'ya **İşlem Yapan Agent'lar için Onay
ve Yetki Katmanı** geliyor. Bugün agent'lar MCP bağlantıları üzerinden iç
sistemlerdeki veriyi sadece okuyabiliyor. Ekipler, agent'ların işlem de
yapabilmesini istiyor: BT talebi açmak, Jira kaydı oluşturmak, Müşteri 360'a not
eklemek, fizy'de şarkı bilgisini düzeltmek gibi. Bilgi güvenliği, insan onayı ve
yetki kontrolü olmadan buna izin vermiyor. Mühendislik ekibi 2 hafta sonra
planlamaya başlıyor ve PRD istiyor.

## Vaka malzemesi

### Discovery notları (10 ekip görüşmesi + bilgi güvenliği çalıştayı, özet)

1. 10 ekibin 8'i agent'ın işlemi "hazırlamasını", son onayı bir insanın vermesini
   istiyor. Tam otomatik işlem isteyen 2 ekip var (fizy ve BT destek), ikisi de
   düşük riskli, çok tekrarlı işler için.
2. fizy ekibi haftada yaklaşık 3.000 şarkı bilgisi düzeltmesi yapıyor; her birini
   tek tek onaylamak "agent'ı anlamsız kılar" diyor. Toplu onay istiyor.
3. Ekipler onay isteğini Teknocan'a girmeden, alıştıkları yerde (e-posta veya
   kurumsal mesajlaşma) görmek istiyor.
4. Kullanıcılar agent'ın "kimin adına" işlem yaptığını bilmiyor. Bir ekip, agent'ın
   kendi yetkilerinden fazlasını yapabildiğini fark etmiş.
5. Bilgi güvenliği çalıştayında bir test yapıldı: Bilgi bankasındaki bir dokümana
   gizlenmiş bir talimat, agent'ı ilgisiz bir Jira kaydı açmaya yönlendirdi
   (prompt injection).
6. Denetim ekibi, müşteri verisine dokunan her işlem için "hangi kişi, hangi
   agent, hangi veri, ne zaman" kaydı istiyor.
7. Agent sahipleri, onaylanan ve reddedilen işlemlerin oranını görmek istiyor;
   bunu agent'ı iyileştirmek için kullanacaklar.
8. Onay bekleyen işlem saatlerce beklerse işin anlamı kalmıyor (ör. müşteri
   görüşmesi bitmiş oluyor).

### Teknik gerçekler

- MCP bağlantıları bugün bağlantı başına tek bir servis hesabıyla çalışıyor. Bu
  hesapların yetkisi, agent'ı kullanan kişinin yetkisinden geniş.
- Kurumsal kimlik yönetimi (SSO) var; kişi bazlı yetki bilgisi her iç sistemden
  alınabiliyor ama bazı sistemlerde gecikmeli.
- Teknocan'da sadece sohbet kayıtları tutuluyor; MCP üzerinden yapılan
  çağrıların ayrı bir denetim kaydı yok.
- Bağlantıların işlem yapabilen (yazma) uçları: Jira, BT talep sistemi, Müşteri
  360 (not ekleme), fizy İçerik Yönetim Sistemi. Dergilik arşivi sadece okuma.
- KVKK: Müşteri verisine yapılan her işlem kişi bazında kayıt altına alınmalı ve
  yetkisiz erişim engellenmeli (Zeynep).

### Bağlı olduğu OKR'lar

- Üretimde çalışan agent sayısını 15'ten 100'e çıkarmak.
- Destekleyici metrik: İşlem yapan agent'larda kabul edilen öneri oranı %80 ve
  üzeri; güvenlik ihlali sıfır.

### Kapsam dışı (Selim'in notu)

Müşteriye açık agent'lar (BiP), yeni model entegrasyonu, agent pazaryeri.
