# NeuroLab Power Analysis

Primer nöron kültürü deneylerinde gereken hayvan (gebe dişi) sayısını hesaplayan, tek sayfalık bir güç analizi aracı. Hayvan deneyleri etik kurulu başvurularında denek sayısını gerekçelendirmek için hazırlanmıştır.

## Kullanım

`index.html` dosyasını bir tarayıcıda açmanız yeterli; kurulum gerekmez. Tüm sorular aynı sayfadadır. Her sayısal soruda hazır değerlerden birini seçebilir ya da "Elle gir" ile kendi değerinizi girebilirsiniz; izin verilen aralık sorunun altında yazar. Sonuç her değişiklikte güncellenir.

## Neler hesaplanır

- **Tasarımlar:** iki bağımsız grup, iki eşleştirilmiş grup (aynı hayvanın hücreleri iki gruba ekilir) ve çok gruplu tekrarlı ölçüm / blok tasarımı.
- **Etki büyüklüğü:** doğrudan (d, dz veya f) ya da ortalama ve standart sapmadan. Standart sapma nörit veya hücre düzeyinde ölçülmüşse, ICC ve hayvan başına ölçüm sayısıyla hayvan ortalaması düzeyine çevrilir.
- **Sonuç:** toplam gebe dişi, gerçekleşen güç, yaklaşık embriyo sayısı, 3 hayvanla elde edilen güç, duyarlılık tablosu ve aynı hesabı G*Power'da tekrarlamak için ayarlar.

Analiz birimi hayvandır: aynı hayvandan gelen kuyucuk ve hücreler ortalaması alınarak tek gözlem sayılır.

## Yöntem

Hesaplar G*Power 3.1 ile aynı yöntemi kullanır. t testlerinde güç, merkezi olmayan t dağılımından sayısal integralle; tekrarlı ölçüm ANOVA'da merkezi olmayan F dağılımından ("Repeated measures, within factors" formülü) hesaplanır. Sonuçlar SciPy tabanlı bir Python uygulamasıyla karşılaştırılarak doğrulanmıştır.

## Kaynaklar

- Faul F, Erdfelder E, Lang AG, Buchner A. G*Power 3. *Behav Res Methods* 2007; 39:175–191.
- Lazic SE, Clarke-Williams CJ, Munafò MR. What exactly is 'N' in cell culture and animal experiments? *PLoS Biol* 2018; 16:e2005282.
- Abidian MR, Corey JM, Kipke DR, Martin DC. Conducting-polymer nanotubes improve electrical properties, mechanical adhesion, neural attachment, and neurite outgrowth of neural electrodes. *Small* 2010; 6:421–429. (Açılıştaki örnek değerler)
