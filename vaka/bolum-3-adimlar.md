# Bölüm 3 Adımları — "Pazarı hızlı anlamam lazım"

**Skill'ler:** market-landscape-scan → competitive-research-snapshot → swot-analysis
**Süre:** tam ~90 dk, hızlı mod ~45 dk (Adım 1'i atlayın)
**Çıktı:** kaynaklı pazar haritası + rakip karşılaştırma matrisi + bir oyuncunun SWOT'u

> Vaka malzemesi: `vaka/bolum-3.md`. Önce o dosyayı okuyun, sonra aşağıdaki
> promptları sırayla Claude Code'a yapıştırın.
>
> Bu bölümde skill'ler web aramasıyla kamuya açık kaynak toplar ve kaynak
> gösterir. Claude web araması için izin isterse onaylayın.

## Adım 1 — market-landscape-scan (~30 dk, hızlı modda atlayın)

```text
@vaka/bolum-3.md dosyasını oku. market-landscape-scan skill'ini kullan.
Türkiye'de kurumsal yapay zekâ asistanı ve agent platformları pazarını tara.
Segmentleri (sektör ve şirket büyüklüğüne göre), oyuncuları, ikameleri
(şirketin kendi kurduğu çözümler gibi) ve boş alanları haritala. Bu taramanın
destekleyeceği karar: "Turkcell, Teknocan'ı kurumsal müşterilerine ürün olarak
sunmalı mı, hangi segmente?" Her iddia için kaynak göster. Bitince çıktıyı
ciktilar/ klasörüne kaydet.
```

## Adım 2 — competitive-research-snapshot (~30 dk)

```text
competitive-research-snapshot skill'ini kullan. Türkiye'de kurumsal müşterilere
sunulan yapay zekâ asistanı ve agent platformlarını karşılaştır: en az bir
küresel platform, bir model sağlayıcının kurumsal planı, bir yerli oyuncu ve
bir operatör teklifi olsun. Kriterler: veri nerede tutuluyor, iç sistemlere
bağlantı (MCP veya benzeri), agent oluşturma, fiyatlandırma modeli, kurulum
hizmeti, hedef sektör. Karşılaştırma matrisi ve "bunun Teknocan kararı için
anlamı" bölümü olsun. Kaynak göster. Bitince çıktıyı ciktilar/ klasörüne kaydet.
```

## Adım 3 — swot-analysis (~25 dk)

SWOT tek bir gerçek şirket için yapılır. Adım 2'deki oyunculardan birini seçin.

```text
swot-analysis skill'ini kullan. [ŞİRKET ADI] için Türkiye kurumsal yapay zekâ
asistanı ve agent platformu pazarı odaklı, kamuya açık kaynaklara dayalı bir
SWOT hazırla. Sonunda stratejik çaprazlamaları (SO, ST, WO, WT) ver ve
"Teknocan için anlamı" diye kısa bir bölüm ekle. Bitince çıktıyı ciktilar/
klasörüne kaydet.
```

## Tartışma (5 dk)

- Claude'un kaynaklarından birini açıp kontrol edin. İddia kaynağın söylediğiyle
  örtüşüyor mu?
- Turkcell'in bu pazarda gerçekten farklılaştığı nokta ne olabilir: model mi,
  veri yerelleştirme mi, kurulum hizmeti mi, mevcut müşteri ilişkisi mi?
- Nihan'ın sorusuna şimdi tek cümlelik cevabınız ne?
