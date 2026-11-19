# Bölüm 2 — "Masama bir talep / emir düştü"

## Durum

Cuma 18:40. Deniz'in ekibi çeyreğin ortasında, Bölüm 1'de ortaya çıkan problem
üzerinde çalışıyor. Dijital Servisler ve Çözümler GMY'si Nihan Ertürk'ten bir
WhatsApp mesajı geliyor. Deniz cevap yazmadan önce mesajı analiz etmek istiyor.

## Vaka malzemesi

### Mesaj (Nihan Ertürk, GMY → Deniz Aksoy)

> Deniz selam, Selim'le de konuştum. Rakip operatör geçen hafta kendi
> mesajlaşma uygulamasında yapay zekâ asistanı açtı; müşteriler fatura ve tarife
> sorularını oradan soruyor. Basında da çok konuşuldu. YK'da "BiP'imiz var,
> Teknocan'ımız var, bizde neden yok?" diye soruldu. Teknocan'ı BiP'e bağlayıp
> müşterilere açabilir miyiz? Ay sonundaki YK'da en azından demo görelim.
> Pazarlama "BiP'te yapay zekâ" kampanyasını hazır tutsun. Ne dersin?

### Bilinen gerçekler

- Teknocan'ın bilgi bankaları iç kullanım için kuruldu. Dokümanların bir kısmı
  gizli veya iç bilgi içeriyor (bayi prim tabloları, iç süreçler). Müşteriye açık
  bir asistan için içeriği ayrıştırmak gerekiyor; Ece'nin tahmini 3–4 ay.
- Bölüm 1'deki testte güncel kampanya ve fiyat sorularında doğruluk %43.
  Müşteriye yanlış fiyat söylemek tüketici şikayeti ve regülasyon riski demek.
- Müşterinin kendi fatura bilgisine erişmek için kimlik doğrulama ve KVKK
  kapsamında açık rıza gerekiyor. Müşteri 360 MCP bağlantısı şu an sadece
  temsilci yetkisiyle ve salt okuma çalışıyor.
- BiP'in kurumsal hesaplar için bot altyapısı var. Turkcell'in BiP'teki resmi
  hesabında bugün kural tabanlı basit bir menü botu çalışıyor (Kaan).
- Maliyet: Sorgu başına 0,40 TL ile günde 300.000 müşteri sorusu, aylık yaklaşık
  3,6 milyon TL token maliyeti demek (Cem).
- Prompt injection ve kötüye kullanım testleri müşteriye açık bir asistan için
  henüz yapılmadı (Tolga).
- YK sunumuna 12 iş günü var. Sprint 2 hafta.

### Paydaş listesi

| Paydaş | Bu konudaki tutumu |
| --- | --- |
| Nihan Ertürk (GMY) | YK'ya cevap göstermek istiyor, hız bekliyor |
| Selim Karaca (Direktör) | Nihan'a "bakarız" demiş; çeyrek hedefi Bölüm 1'deki sorun |
| Kaan Polat (BiP Ürün Direktörü) | Kanalın sahibi; kötü deneyimden BiP'in zarar görmesinden çekiniyor |
| Selin Demir (Pazarlama) | Kampanya için hevesli |
| Ayşe Koç (Müşteri Hizmetleri) | Çağrı yükünü azaltacaksa destekler |
| Ece Tan (Bilgi Yönetimi) | Ekibi küçük, içerik ayrıştırma yükünden korkuyor |
| Burak Şen (Platform) | Ölçeklenme ve MCP yetkileri konusunda temkinli |
| Tolga Uysal (Bilgi Güvenliği) | Müşteriye açık yapay zekâ için veto hakkı var |
| Zeynep Arslan (Hukuk/KVKK) | Müşteri verisi ve açık rıza konusunda veto hakkı var |
| Cem Tunç (Finans) | Token maliyetinin karşılığını görmek ister |
| Müşteriler | Henüz kimse sormadı |

### Teknocan backlog'u — Q1 2027 adayları

| Kalem | Kimin talebi | Tahmini etki | Efor | Veri güveni |
| --- | --- | --- | --- | --- |
| Kampanya bilgi bankası temizliği + cevapta kaynak gösterme | Teknocan ekibi | Kampanya sorularında doğruluk %43 → %80; temsilci kullanımı artar | 6 hafta | Orta |
| Teknocan'ı Müşteri 360 ekranına yan panel olarak gömme | Müşteri hizmetleri | Görüşme sırasında kullanım; AHT düşüşü | 8 hafta | Orta |
| BiP'te müşteriye açık yapay zekâ asistanı | Nihan | Rakip paritesi; çağrı azalması belirsiz | 12+ hafta + içerik ayrıştırma | Düşük |
| Agent Oluşturucu'yu genel kullanıma açma | 40 ekip | Üretimdeki agent sayısı | 10 hafta | Orta |
| İK portalı MCP bağlantısı | İK | Ayda 2.000 İK sorusu Teknocan'a geçer | 3 hafta | Yüksek |
| Model yönlendirme ile maliyet optimizasyonu | Finans | Sorgu maliyetinde –%30 | 4 hafta | Yüksek |
| Kullanım panosu ve oyunlaştırma | Ayşe | Kullanım artışı iddiası | 3 hafta | Düşük |

Kapasite: 1 squad, Q1 = 12 hafta.
