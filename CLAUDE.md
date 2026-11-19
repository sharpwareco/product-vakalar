# Turkcell Dijital Servisler — PM Skills Uygulama Günü

Bu klasör "GenAI for Product Managers" eğitiminin uygulama çalışması içindir.
Kullanıcı bir ürün yöneticisidir ve Dean Peters'ın Product Manager Skills
skill'lerini Turkcell'in dijital ürünleri üzerine kurulmuş kurgusal bir vakada
deniyor.

## Önemli: Bu vaka kurgusaldır

Vakada Turkcell'in gerçek ürün adları (Teknocan, BiP, fizy, Dergilik) kullanılır.
Ancak vakadaki **tüm rakamlar, kişiler, olaylar, iç detaylar ve kararlar eğitim
için uydurulmuştur**. Gerçek Turkcell verisi, stratejisi veya planı değildir.
Vaka bilgisini gerçek bilgiymiş gibi sunma; gerekiyorsa "vakaya göre" de.

## Çalışma kuralları

- Yanıtlarını her zaman **Türkçe** ver. Skill dosyaları İngilizce olsa da çıktılar,
  sorular ve seçenekler Türkçe olmalı. Yaygın İngilizce terimleri (PRD, epic,
  user story, SWOT, OKR, RAG, MCP, agent, token, prompt) çevirmeden kullanabilirsin.
- Kullanıcı bir skill'in adını verdiğinde o skill'i yükle ve talimatlarını izle.
- Vaka malzemesi `vaka/bolum-<N>.md` dosyalarındadır. `vaka/bolum-<N>-adimlar.md`
  dosyaları katılımcının kopyaladığı promptları içerir; bu dosyaları okuma ve
  referans alma. Sadece kullanıcının yazdığı adımı çalıştır, bir sonraki adıma
  kendiliğinden geçme.
- Vakada olmayan rakam, kişi veya olayı uydurma. Bir varsayım yapman gerekirse
  bunu açıkça **"Varsayım:"** diye işaretle.
- Bölüm 3 dışında web araması yapma; vaka malzemesi yeterlidir. Bölüm 3'te
  kamuya açık kaynak kullan ve her iddia için kaynak bağlantısı ver. Teknocan
  hakkında kamuya açık bilgi bulamazsan vaka bilgisini kullan ve bunu belirt.
- Skill bir soru sorduğunda tek soru sor ve numaralı seçenekler sun. Kullanıcı
  "en iyi tahminle devam et" derse varsayımlarını işaretleyerek devam et.
- Bir adımın nihai çıktısını `ciktilar/` klasörüne Markdown olarak kaydet.
  Dosya adı: `bolum-<N>-adim-<M>-<skill-adi>.md`
  (örnek: `ciktilar/bolum-1-adim-1-problem-framing-canvas.md`).
- Kod yazma, program kurma veya `ciktilar/` dışındaki dosyaları değiştirme.

## Vaka bağlamı

**Şirket:** Turkcell, Dijital Servisler ve Çözümler birimi.

**Odak ürün: Teknocan** — Turkcell'in şirket içi yapay zekâ platformu (harness).

- Şirket içi bilgi bankalarını **RAG** ile kullanır: Confluence ve SharePoint
  alanları, kampanya ve tarife doküman havuzu, politika ve prosedür dokümanları
  (toplam yaklaşık 120.000 doküman).
- İç uygulamalara **MCP** üzerinden bağlanır: Jira, Müşteri 360 (CRM, şu an salt
  okuma), BT talep sistemi, fizy İçerik Yönetim Sistemi, Dergilik arşivi. İK
  portalı bağlantısı geliştiriliyor.
- **Agent Oluşturucu** (beta): ekipler kendi agent'larını kurabiliyor. Üretimde
  15 agent var, 40 ekip bekleme listesinde.
- **Model katmanı:** birden fazla büyük dil modeli; görev tipine göre model seçimi.
- 2025'te iç kullanıma açıldı. Erişimi olan çalışan: 18.000. Haftalık aktif
  kullanıcı: 4.300.
- Sorgu başına ortalama token maliyeti yaklaşık 0,40 TL.
- Her yeni bilgi bankası veya MCP bağlantısı için bilgi güvenliği onayı ortalama
  6 hafta sürüyor.

**Diğer dijital ürünler (vakada geçen)**

- **BiP:** mesajlaşma uygulaması; kanallar ve kurumsal hesaplar için bot altyapısı var.
- **fizy:** müzik ve video platformu; içerik ekibi Teknocan agent'ı kullanıyor.
- **Dergilik:** dijital dergi ve gazete platformu; editoryal ekip Teknocan'ı arşiv
  araması için kullanıyor.
- **Sorbi:** 2018'den beri çalışan, kural tabanlı eski iç yardım botu (BT ve İK
  soruları). Kurgusaldır.

**Ekip ve paydaşlar (hepsi kurgusal)**

| Kişi | Rol |
| --- | --- |
| Deniz Aksoy | Kıdemli Ürün Yöneticisi, Teknocan (kullanıcı bu rolde) |
| Selim Karaca | Yapay Zekâ Platformları Direktörü (Deniz'in yöneticisi) |
| Nihan Ertürk | Dijital Servisler ve Çözümler GMY (Selim'in üstü, Yönetim Kurulu'na sunum yapar) |
| Ayşe Koç | Müşteri Hizmetleri Direktörü (çağrı merkezi, 6.200 temsilci) |
| Ece Tan | Bilgi Yönetimi Müdürü (bilgi bankalarının sahibi) |
| Burak Şen | Platform Mühendisliği Lideri (MCP bağlantıları, altyapı) |
| Tolga Uysal | Bilgi Güvenliği Müdürü |
| Zeynep Arslan | Hukuk, Regülasyon ve KVKK |
| Kaan Polat | BiP Ürün Direktörü |
| Melis Doğan | fizy İçerik Operasyonları Müdürü |
| Can Yurt | Dergilik Editoryal Müdürü |
| Selin Demir | Pazarlama Direktörü |
| Cem Tunç | Finans İş Ortağı |

**Ekip kapasitesi:** Teknocan ürün ekibi 1 squad (6 geliştirici, 1 tasarımcı,
1 analist), 2 haftalık sprint, çeyrek = 12 hafta. Platform mühendisliği ortak kaynak.

**Teknocan OKR'ları (2027 H1):**

1. Haftalık aktif kullanıcıyı 4.300'den 10.000'e çıkarmak.
2. Üretimde çalışan agent sayısını 15'ten 100'e çıkarmak.
3. Müşteri hizmetlerinde "yanlış bilgi verildi" şikayetlerini %30 azaltmak.
4. Sorgu başına token maliyetini %25 düşürmek.
