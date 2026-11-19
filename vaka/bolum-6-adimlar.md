# Bölüm 6 Adımları — "Ürünümüz yaşlanıyor"

**Skill'ler:** lifecycle-play-advisor → eol-readiness-advisor → eol-process
**Süre:** ~40 dk
**Çıktı:** yaşam döngüsü teşhisi + emekliye ayırma için git/gitme kararı + uçtan uca kapatma planı

> Vaka malzemesi: `vaka/bolum-6.md`. Önce o dosyayı okuyun, sonra aşağıdaki
> promptları sırayla Claude Code'a yapıştırın.

## Adım 1 — lifecycle-play-advisor (~10 dk)

```text
@vaka/bolum-6.md dosyasını oku. lifecycle-play-advisor skill'ini kullan.
Eski iç yardım botumuz Sorbi hakkında ne yapacağımıza karar vermeme yardım et.
Solmakta olduğunu düşündüren sinyaller dosyada. Extend, replace veya retire
seçeneklerinden hangisi uygun? Bitince çıktıyı ciktilar/ klasörüne kaydet.
```

## Adım 2 — eol-readiness-advisor (~10 dk)

```text
eol-readiness-advisor skill'ini kullan. Sorbi'yi emekliye ayırmak için git/gitme
değerlendirmesi yap ve gereken eforu doğru boyutlandır. Özellikle şifre
sıfırlama gibi Teknocan'ın henüz yapamadığı işlemlere, saha çalışanlarına ve
bayi personeline dikkat et. Bitince çıktıyı ciktilar/ klasörüne kaydet.
```

## Adım 3 — eol-process (~20 dk)

```text
eol-process skill'ini kullan. Sorbi için uçtan uca kapatma planı oluştur:
karar, paydaş hizalama, plan, hazırlık, duyuru ve kapanış. Paydaşlar: Nihan,
Hakan (BT Hizmetleri, Sorbi'nin kurucusu), Cem (Finans), Ece (Bilgi Yönetimi),
Burak (Platform), Tolga (Bilgi Güvenliği), Zeynep (Hukuk), İK, bayi kanalı.
Çalışanlara gidecek ilk duyuru metnini de yaz. Bitince çıktıyı ciktilar/
klasörüne kaydet.
```

## Tartışma (5 dk)

- Kapatma bir maliyet konusu mu, yoksa Teknocan'ın yeni kullanıcı kazanma
  fırsatı mı?
- Paydaşlara hangi sırayla gidiyorsunuz? Hakan'a ne zaman?
- Sorbi'yi kapatmak için Bölüm 5'teki onay katmanını beklemek gerekiyor mu?
- Duyuru metni sahadaki bir teknisyenin anlayacağı dilde mi?
