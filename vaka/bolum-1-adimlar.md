# Bölüm 1 Adımları — "Bir fikrim var, gerçek mi bilmiyorum"

**Skill'ler:** problem-framing-canvas → discovery-interview-prep → pol-probe-advisor
**Süre:** ~75 dk
**Çıktı:** yeniden tanımlanmış problem + görüşme planı + 6 haftalık doğrulama deneyi

> Vaka malzemesi: `vaka/bolum-1.md`. Önce o dosyayı okuyun, sonra aşağıdaki
> promptları sırayla Claude Code'a yapıştırın.

## Adım 1 — problem-framing-canvas (~25 dk)

```text
@vaka/bolum-1.md dosyasındaki vaka malzemesini oku. problem-framing-canvas
skill'ini kullan. Bu problemi çerçevele: Teknocan Kampanya ve Tarife
Asistanı'nın çağrı merkezindeki haftalık kullanımı altı ayda %38'den %11'e
düştü. Yönetim üç çözüme çoktan çapalanmış durumda: oyunlaştırma ve KPI,
daha büyük bir modele geçmek ve daha fazla doküman yüklemek. Bu çözümleri
sorgula. Bitince çıktıyı ciktilar/ klasörüne kaydet.
```

Beklenen çıktı: Look Inward / Look Outward / Reframe bölümleri, yeniden yazılmış
problem cümlesi ve bir "Nasıl yapabiliriz?" (HMW) sorusu.

## Adım 2 — discovery-interview-prep (~25 dk)

```text
discovery-interview-prep skill'ini kullan. Bir önceki adımda çıkan problem
cümlesi ve HMW sorusu ciktilar/bolum-1-adim-1-problem-framing-canvas.md
dosyasında. Asistanı bırakan ve hâlâ kullanan çağrı merkezi temsilcileriyle
görüşme ve gözlem planı hazırla. Kısıtlar: 2 hafta, vardiya planına bağlı
görüşmeler, en fazla 12 temsilci gözlemi. Bitince çıktıyı ciktilar/
klasörüne kaydet.
```

Beklenen çıktı: görüşme hedefi, segment seçimi, yöntem, soru kılavuzu ve
"neyi öğrenirsek fikrimizi değiştiririz" listesi.

## Adım 3 — pol-probe-advisor (~20 dk)

```text
pol-probe-advisor skill'ini kullan. Doğrulamak istediğim en riskli hipotez:
"[ADIM 1-2'DEN ÇIKAN EN RİSKLİ HİPOTEZİNİZİ YAZIN]". Kaynaklarım: 6 hafta,
1 tasarımcı, 2 geliştirici, 150.000 TL, Teknocan sorgu loglarına erişim.
Bana uygun Proof of Life probe'unu seç. Bitince çıktıyı ciktilar/ klasörüne
kaydet.
```

Beklenen çıktı: hipoteze ve riske uygun bir probe türü, başarı ölçütü ve
"öldürme" kriteri.

## Tartışma (5 dk)

- Claude üç hazır çözümden birini savundu mu, yoksa problemi çözümden
  ayırabildi mi?
- Dün konuştuğumuz kavramlardan hangisi bu problemin merkezinde: model mi,
  context mi, RAG mı, harness mı?
- Veride kaçırdığınız bir kırılım var mı?
- Probe 6 hafta sonunda size hangi kararı verdirecek?
