# Bölüm 5 Adımları — "Artık yazıya dökme zamanı"

**Skill'ler:** prd-development → epic-breakdown-advisor → user-story
**Süre:** ~80 dk
**Çıktı:** PRD + parçalanmış epic + Gherkin kabul kriterli user story'ler

> Vaka malzemesi: `vaka/bolum-5.md`. Önce o dosyayı okuyun, sonra aşağıdaki
> promptları sırayla Claude Code'a yapıştırın.

## Adım 1 — prd-development (~40 dk)

```text
@vaka/bolum-5.md dosyasını oku. prd-development skill'ini kullan. Teknocan
Agent Oluşturucu için "İşlem Yapan Agent'lar için Onay ve Yetki Katmanı"
özelliğinin PRD'sini oluştur. Discovery notları, teknik gerçekler, bağlı
olduğu OKR'lar ve kapsam dışı maddeler dosyada. Varsayımları ve açık soruları
ayrıca işaretle. Bitince PRD'yi ciktilar/ klasörüne kaydet.
```

## Adım 2 — epic-breakdown-advisor (~25 dk)

PRD'den bir epic seçin. Önerilen: **"Agent bir işlem yapmadan önce kullanıcıdan
onay alır"**.

```text
epic-breakdown-advisor skill'ini kullan. PRD
ciktilar/bolum-5-adim-1-prd-development.md dosyasında. Şu epic tahmin
edilemeyecek kadar büyük: "Agent bir işlem yapmadan önce kullanıcıdan onay
alır." Farklı sistemlerin farklı riskleri var, bazı ekipler toplu onay istiyor,
işlem kullanıcının kendi yetkisiyle yapılmalı ve her işlem denetim kaydına
düşmeli. Humanizing Work split pattern'leriyle parçala ve ilk sprintte teslim
edilebilecek en ince dilimi öner. Bitince çıktıyı ciktilar/ klasörüne kaydet.
```

## Adım 3 — user-story (~15 dk)

```text
user-story skill'ini kullan. Bir önceki adımda çıkan ilk 3 dilim için Mike Cohn
formatında user story ve Gherkin (Given/When/Then) kabul kriterleri yaz.
Kullanıcının yetkisinin yetmediği, onayın zaman aşımına uğradığı ve agent'ın
şüpheli bir talimatla tetiklendiği senaryoları da kapsa. Bitince çıktıyı
ciktilar/ klasörüne kaydet.
```

## Tartışma (5 dk)

- PRD'nin başarı metrikleri OKR'a gerçekten bağlanıyor mu?
- Claude PRD'de discovery notlarında olmayan bir şey uydurdu mu?
- Dün konuştuğumuz MCP ve agent kavramları burada hangi yeni riskleri doğurdu?
- İlk dilim gerçekten 2 haftada yapılır mı? Kabul kriterleri test edilebilir mi?
