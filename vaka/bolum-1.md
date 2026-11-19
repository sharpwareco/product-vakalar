# Bölüm 1 — "Bir fikrim var, gerçek mi bilmiyorum"

## Durum

Teknocan'ın müşteri hizmetleri için kurduğu **Kampanya ve Tarife Asistanı** altı
ay önce 6.200 çağrı merkezi temsilcisine açıldı. Asistan, kampanya ve tarife
doküman havuzunu RAG ile kullanarak temsilcilerin sorularını cevaplıyor. Hedef,
görüşme süresini kısaltmak ve müşteriye yanlış bilgi verilmesini azaltmaktı.

Kullanım hızla düştü. Pazartesi yönetim toplantısında üç farklı "çözüm" masaya
kondu:

- Ayşe (Müşteri Hizmetleri): "Kullanımı temsilci KPI'larına bağlayalım, bir de
  liderlik tablosu koyalım. Oyunlaştırma işe yarar."
- Teknocan ekibinden bir mühendis: "Daha büyük, yeni nesil bir modele geçelim.
  Cevaplar iyileşir, kullanım artar."
- Ece (Bilgi Yönetimi): "Daha fazla doküman yükleyelim, kapsama artsın."

Selim, Deniz'den 2 hafta içinde "gerçek problemin ne olduğunu" göstermesini istedi.

## Vaka malzemesi

### Temel metrikler

| Metrik | Lansman ayı | 6. ay |
| --- | --- | --- |
| Haftalık aktif temsilci oranı | %38 | %11 |
| Cevaplara "yararlı" (başparmak yukarı) oranı | %61 | %52 |
| Ortalama görüşme süresi (AHT) | 312 sn (lansman öncesi) | 318 sn |
| Aylık "yanlış bilgi verildi" şikayeti | 1.940 (lansman öncesi) | 2.010 |
| Ortalama cevap süresi | 8 sn | 9 sn |

### Ekip içi doğruluk testi (200 gerçek temsilci sorusu)

| Soru tipi | Doğru cevap oranı |
| --- | --- |
| Genel prosedür (iade, nakil, hat dondurma) | %84 |
| Kurumsal sözleşme maddeleri | %81 |
| Güncel kampanya ve fiyat | %43 |
| Tüm sorular | %61 |

Yanlış cevapların %70'inde asistan, süresi geçmiş bir kampanya dokümanını kaynak
almış.

### Bilgi bankası durumu (Ece'nin ekibinden)

- Kampanya ve tarife havuzunda 14.800 doküman var.
- Son 90 günde güncellenen doküman oranı: %22.
- Aynı kampanyanın birden fazla versiyonunun bulunduğu doküman oranı: %35.
- Dokümanları pazarlama ekipleri yüklüyor. Eski versiyonu kaldırmak kimsenin
  görev tanımında yok.

### Kullanım kırılımları (analist notu)

| Kırılım | Haftalık aktif oranı |
| --- | --- |
| Kurumsal hat destek ekibi | %41 |
| Bireysel faturalı hat ekibi | %7 |
| İlk 6 ayındaki temsilciler | %29 |
| 2 yıldan kıdemli temsilciler | %4 |

Temsilciler Müşteri 360 (CRM) ekranında çalışıyor. Teknocan ayrı bir tarayıcı
sekmesinde açılıyor; görüşme sırasında geçiş 3 tık ve bazen yeniden oturum açma
gerektiriyor. Asistan cevabının hangi dokümana dayandığını göstermiyor.

### Temsilci ve takım lideri sesleri

1. "Asistan geçen ayın kampanyasını söyledi, müşteriye yanlış fiyat verdim,
   şikayet geldi. O günden beri açmıyorum." — Bireysel faturalı temsilci
2. "Görüşme sırasında ikinci bir pencere açıp soru yazacak vaktim yok. Takım
   liderine soruyorum." — Temsilci
3. "Kurumsal hatlarda sözleşme maddelerini saniyede buluyor, çok iyi." — Kurumsal
   destek temsilcisi
4. "Cevabın nereden geldiğini göstermiyor. Doğru mu, emin olamıyorum." — Temsilci
5. "Kampanya PDF'lerini masaüstüne indiriyoruz, daha hızlı." — Takım lideri
6. "Yeniler kullanıyor, kıdemliler hiç açmıyor." — Takım lideri

### Paydaş görüşleri

- Ayşe (Müşteri Hizmetleri): "Temsilciler yeniliğe direnç gösteriyor. Hedef
  koymazsak kullanmazlar."
- Burak (Platform): "Model tarafında sorun görmüyoruz. Gecikme makul."
- Ece (Bilgi Yönetimi): "Bilgi bankası bizim, ama içeriği pazarlama yüklüyor.
  Ekibim 3 kişi."
- Selin (Pazarlama): "Kampanya her hafta değişiyor. Dokümanları zamanında
  yüklüyoruz."
- Cem (Finans): "Yeni nesil modele geçmek sorgu maliyetini yaklaşık 3 katına
  çıkarır."

### Kısıtlar

Deney için 6 hafta, 1 tasarımcı, 2 geliştirici, 150.000 TL bütçe. Teknocan sorgu
loglarına erişim var. Temsilcilerle görüşme vardiya planına bağlı; en fazla 12
temsilci gözlemi (yanında oturarak) yapılabilir.
