# Bölüm 2 Adımları — "Masama bir talep / emir düştü"

**Skill'ler:** incoming-request-advisor → stakeholder-mapping → prioritization-advisor
**Süre:** ~60 dk
**Çıktı:** talep analizi + cevap taslağı + paydaş haritası + önceliklendirme çerçevesi ve sıralama

> Vaka malzemesi: `vaka/bolum-2.md`. Önce o dosyayı okuyun, sonra aşağıdaki
> promptları sırayla Claude Code'a yapıştırın.

## Adım 1 — incoming-request-advisor (~20 dk)

```text
@vaka/bolum-2.md dosyasını oku. incoming-request-advisor skill'ini kullan.
GMY'm cuma akşamı bana WhatsApp'tan dosyadaki mesajı attı. Ben Teknocan'ın
Kıdemli Ürün Yöneticisiyim, o benim yöneticimin yöneticisi (upstream).
"Bilinen gerçekler" bölümünü de dikkate al. Cevap vermeden önce analiz et,
sonra cevap taslağı öner. Bitince çıktıyı ciktilar/ klasörüne kaydet.
```

Beklenen çıktı: "Incoming Request Breakdown" (literal talep, alttaki iş, alt
metin, kısıtlar, riskler) ve 4 yol: cevap taslağı, toplantı gündemi, discovery
çerçevesi veya karşı öneri. "1" (cevap taslağı) seçin.

## Adım 2 — stakeholder-mapping (~15 dk)

```text
stakeholder-mapping skill'ini kullan. "Teknocan'ı BiP'te müşterilere açma"
talebi için @vaka/bolum-2.md dosyasındaki paydaş listesini iki grid üzerinde
konumlandır ve her biri için iletişim stratejisi öner. Bitince çıktıyı
ciktilar/ klasörüne kaydet.
```

## Adım 3 — prioritization-advisor (~25 dk)

```text
prioritization-advisor skill'ini kullan. Q1 2027 için @vaka/bolum-2.md
dosyasındaki Teknocan backlog'undaki 7 kalem arasında önceliklendirme yapmam
gerekiyor. Ekip kapasitesi 12 hafta, 1 squad. Paydaşlarım farklı şeyler
istiyor ve verinin bir kısmı zayıf. Teknocan OKR'larını dikkate al. Önce bana
uygun çerçeveyi seç, sonra o çerçeveyle sırala. Bitince çıktıyı ciktilar/
klasörüne kaydet.
```

## Tartışma (5 dk)

- Nihan'ın asıl işi (job-to-be-done) neydi: bir özellik mi, YK'da anlatılacak
  bir hikaye mi?
- Cevap taslağınız "evet", "hayır" mı, yoksa "evet, ama şöyle" mi?
- İç kullanım için kurulmuş bir RAG sistemini müşteriye açmanın riskleri neler?
- Seçilen çerçeve (RICE, ICE, değer/efor…) zayıf veriyle nasıl başa çıktı?
