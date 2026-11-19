# Başlarken — Teknocan Vakası ile PM Skills Uygulama Günü

Bugün Turkcell Dijital Servisler'de, şirket içi yapay zekâ platformu
**Teknocan**'ın ürün ekibindesiniz. Dean Peters'ın Product Manager Skills
skill'lerini 8 bölüm boyunca sırayla kullanacaksınız. Her bölüm gerçek bir ürün
yöneticisi durumudur. Dün konuştuğumuz model, context, RAG, MCP, agent ve harness
kavramları vakaların içinde karşınıza çıkacak.

> **Vaka kurgusaldır.** Turkcell'in ürün adları kullanılıyor ama tüm rakamlar,
> kişiler ve olaylar eğitim için uydurulmuştur. Gerçek ve gizli şirket bilgilerini
> bu çalışmaya yapıştırmayın.

## 1. Ön koşullar

- VS Code kurulu olmalı.
- **Claude Code Saka** eklentisi kurulu olmalı.
  
## 2. Klasörü açın

1. Bu klasörü bilgisayarınızda bir yere çıkarın (ör. Belgeler).
2. VS Code'da **File > Open Folder** ile klasörü açın.
3. "Bu klasördeki dosyaların yazarlarına güveniyor musunuz?" sorusuna
   **Evet / Trust** deyin. Claude Code da benzer bir soru sorarsa onaylayın.
   Onaylamazsanız vaka bağlamı ve skill'ler yüklenmez.

## 3. Skill'leri kontrol edin

Skill'ler `.claude/skills/` klasöründe durur. Bu klasör noktayla başladığı için
bazı bilgisayarlarda gizli görünür.

Eğitmeniniz skill'leri klasöre koymadıysa:

1. [github.com/deanpeters/Product-Manager-Skills](https://github.com/deanpeters/Product-Manager-Skills)
   sayfasında **Code > Download ZIP** ile repoyu indirin.
2. ZIP'in içindeki `skills` klasörünün **içindekileri** bu klasördeki
   `.claude/skills/` içine kopyalayın.
3. Doğru yerleştiyse şu dosya var olmalı:
   `.claude/skills/problem-framing-canvas/SKILL.md`

Claude-saka terminal komutu ile Claude Code CLI'ı açın ve şunu yazın:

```text
Bu klasörde hangi skill'ler yüklü? Sadece isimlerini listele.
```

Listede `problem-framing-canvas`, `incoming-request-advisor`, `prd-development` ve
`lifecycle-play-advisor` görünüyorsa hazırsınız. Görünmüyorsa eğitmene haber
verin.

## 4. Bir bölüm nasıl çalışılır

1. Claude Code CLI'da `/clear` yazarak temiz bir sohbet başlatın.
2. `vaka/` klasöründen bölümün iki dosyasını yan yana açın:
    - `bolum-1.md`: durum ve vaka malzemesi. Önce bunu okuyun (5 dk).
    - `bolum-1-adimlar.md`: kullanacağınız promptlar ve tartışma soruları.
3. Adımlar dosyasındaki ilk promptu kopyalayıp Claude Code'a yapıştırın.
4. Skill size sorular sorar. Her turda tek soru ve numaralı seçenekler gelir.
   Numarayla veya kendi cümlenizle cevap verin.
5. Adım bitince Claude çıktıyı `ciktilar/` klasörüne kaydeder. Sonra bir sonraki
   adımın promptuna geçin. Aynı bölümün adımları arasında `/clear` yapmayın.
6. Bölüm sonundaki tartışma sorularına 5 dakika ayırın.

## 5. İpuçları

- **İzin soruları normaldir.** Claude dosya kaydetmeden veya web'de arama
  yapmadan önce izin isteyebilir. `ciktilar/` klasörüne yazma ve Bölüm 3'teki web
  aramaları için onay verin.
- **Çok soru mu soruyor?** "En iyi tahminle devam et, varsayımlarını işaretle"
  yazın.
- **İngilizceye mi kaydı?** "Türkçe devam et" yazın.
- **Çıktıyı sorgulayın.** Her adımdan sonra kendinize sorun: Claude neyi kaçırdı,
  neyi uydurdu, neye itiraz etmeliyim?

## Bölümler

| Bölüm | Durum | Skill'ler |
| --- | --- | --- |
| 1 | Bir fikrim var, gerçek mi bilmiyorum: Kampanya Asistanı'nı kimse kullanmıyor | problem-framing-canvas → discovery-interview-prep → pol-probe-advisor |
| 2 | Masama bir talep düştü: "Teknocan'ı BiP'te müşterilere açalım" | incoming-request-advisor → stakeholder-mapping → prioritization-advisor |
| 3 | Pazarı hızlı anlamam lazım: Teknocan kurumsal müşterilere satılmalı mı? | market-landscape-scan → competitive-research-snapshot → swot-analysis |
| 4 | Sürekli kıyaslanıyoruz ve kaybediyoruz: Teknocan ve genel amaçlı asistan | positioning-workshop → roadmap-planning |
| 5 | Artık yazıya dökme zamanı: İşlem yapan agent'lar için onay katmanı | prd-development → epic-breakdown-advisor → user-story |
| 6 | Ürünümüz yaşlanıyor: Eski iç yardım botu Sorbi | lifecycle-play-advisor → eol-readiness-advisor → eol-process |
| 7 | Bir üst seviyeye çıkıyorum | director-readiness-advisor veya vp-cpo-readiness-advisor |
| 8 | Yeniyim / emin değilim: BiP, fizy, Dergilik ve Teknocan'dan altı iş | pm-skills-navigator |

---

Skill'ler: Dean Peters, [Product-Manager-Skills](https://github.com/deanpeters/Product-Manager-Skills),
CC BY-NC-SA 4.0 lisanslı. Vaka içeriği: Sharpware, kurgusal.
