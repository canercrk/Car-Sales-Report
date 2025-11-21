# 3 Yıllık Bölgesel Satış Büyüme Analizi

## Arka Plan ve Genel Bakış

Bu analiz projesi, şirketin son üç yıllık (2020-2022) satış performansını incelemektedir. 2020 ve 2021 yıllarındaki 6,9 Milyon $ seviyelerinde ki durağan cironun ardından, 2022 yılında %146 olan ani ve açıklanmamış bir büyümeyle 17,0 Milyon $ seviyesine ulaşılmıştır.

**İş Hedefi:** 2022'deki bu olağanüstü büyümenin kök nedenlerini teşhis etmek; başarının ana itici güçlerini (bölge, temsilci, ürün) izole etmek; düşük performanslı alanları belirlemek ve sonraki dönemler için sürdürülebilir, ölçeklenebilir bir büyüme stratejisi oluşturmak üzere eyleme geçirilebilir, veriye dayalı tavsiyeler sunmaktır.

## Veri Yapısı

Analiz, 3 yıllık (2020-2022) dönemi kapsayan satış raporu üzerinden yürütülmüştür ve veri modeli, çok boyutlu analize izin veren bir "Yıldız Şeması" (Star Schema) yapısını yansıtmaktadır:

**Ana Tablo (Fact Table):** FactSales (Toplam Satış $, İşlem Sayısı gibi metrikleri içerir).

**Boyut Tabloları (Dimension Tables):**
- **dTime:** Yıl (2020, 2021, 2022) ve Ay bazında kırılımlar.
- **dRegion:** 5 ana satış bölgesi (West, NorthWest, SouthWest, East, MidWest).
- **dSalesReps:** 5 satış temsilcisi (CANBERK, MURAT, MİRAÇ, SUNA, GÜLAY).
- **dProduct:** 7 ürün kategorisi (CAR1, CAR2, ..., CAR7).

Bu yapı, FactSales tablosundaki her işlemin; bir zaman, bölge, temsilci ve ürünle ilişkilendirilerek performansın detaylı bir şekilde dilimlenmesine (slicing) olanak tanımıştır.
<img width="1082" height="482" alt="Image" src="https://github.com/user-attachments/assets/6288d00f-1352-4e84-8175-66cfbc0c516b" />

## Yönetici Özeti

**Büyüme Odaklıdır, Yaygın Değildir:** 2022'deki %146'lık ciro artışı, şirketin tamamına yayılan organik bir başarı değildir. Büyüme, spesifik olarak 2022'nin 4. Çeyreği'nde (Kasım: 4,1M$, Aralık: 4,2M$) yaşanan ani bir patlamadan kaynaklanmaktadır.

**"Kazanan" Ürünler Domine Etmektedir:** Toplam 3 yıllık cironun (30,7M$) %50'si sadece iki adet üründen gelmektedir: CAR1 (7,7M$) ve CAR5 (7,7M$).

**Performans Temsilcilerde Yoğunlaşmıştır:** Toplam cironun %53'ü sadece iki satış temsilcisi tarafından üretilmiştir: CANBERK (9,6M$) ve MURAT (6,6M$).

**Yüksek Bağımlılık Riski ve Durağanlık:** Bu durum, cironun %31'inin tek bir kişiye (CANBERK) ve %50'sinin iki ürüne bağlı olması nedeniyle yüksek bir operasyonel risk yaratmaktadır. Eş zamanlı olarak, East ve MidWest bölgeleri 2022'deki bu patlamadan hiç faydalanamamış ve GÜLAY (3,9M $) gibi temsilciler liderlerin çok altında kalmıştır.
![Image](https://github.com/user-attachments/assets/153055dd-a9cb-4f5b-9d0b-5951c607e22b)

![Image](https://github.com/user-attachments/assets/be785cd5-2b3e-4869-a31d-6ff31da175fa)

## Derinlemesine Bakış

Tüm detay raporları çapraz analiz edildiğinde, şirketin net bir "başarı formülü" ve "başarısızlık nedeni" ortaya çıkmıştır:

**Başarının Formülü:** Yüksek ciro, yüksek performanslı temsilcilerin (CANBERK, MURAT), yüksek performanslı bölgelerde (West, NorthWest), yüksek performanslı ürünleri (CAR1, CAR5) satmasıyla elde edilmiştir. CANBERK'in 9,6M $ olan cirosunun arkasındaki itici güç, West bölgesinde CAR1 (0,64M$) ve CAR5 (0,65M$) ürünlerine odaklanmasıdır.

**Düşük Performansın Teşhisi:** Düşük performanslı temsilcilerin (örn: GÜLAY) raporları incelendiğinde, sorunun "odaksızlık" olduğu görülmüştür. GÜLAY'ın portföyü, başarılı temsilcilerin aksine, hiçbir ürün veya bölgede uzmanlaşmamış; tüm kategorilere düşük hacimlerde dağılmıştır. Bu temsilciler, şirketin "kazanan formülünü" uygulamamaktadır.

**Kaçırılan Fırsat:** East ve MidWest bölgelerinin 2020-2021 seviyelerinde kalması, bu bölgelerde "başarı formülünün" ya bilinmediğini ya da uygulanmadığını göstermektedir.

## Tavsiyeler

Analiz sonuçlarına dayanarak, büyümenin sürdürülebilir kılınması ve riskin azaltılması amacıyla aşağıdaki 3 somut eylem önerilmektedir:

**Riski Azaltın ve Başarıyı Kurumsallaştırma:**

CANBERK'in %31'lik ciro bağımlılığı acil bir risktir. CANBERK'in West bölgesinde CAR1/CAR5 için kullandığı satış stratejisi, müşterileri ve metodolojisi derhal belgelenmeli ve diğer üst düzey temsilcilere (MURAT, MİRAÇ) aktarılarak bilgi kurumsallaştırılmalı ve risk dağıtılmalıdır.

**Düşük Performansı İyileştirin ve Başarıyı Kopyalayama:**

GÜLAY ve SUNA için, dağınık portföy yönetimi yerine, kanıtlanmış "başarı formülüne" odaklanan bir "Performans İyileştirme Planı" hazırlanmalıdır ve bu temsilcilere spesifik olarak CAR1/CAR5 ürünlerini West/NorthWest bölgelerinde satma hedefleri verilmelidir.

**Stratejik Nedeni Araştırma:**

"Neden sadece CAR1 ve CAR5? Neden özellikle West Bölgesi?" sorularının cevabı için stratejik bir saha ve müşteri araştırması yapılmalıdır ve bu iki ürün birbiriyle ilişkili mi (bundle)? Bu bölgede yeni bir müşteri segmenti mi keşfedildi? Bu soruların cevabı, bu başarının tesadüfi olup olmadığını veya ölçeklenebilir bir büyüme stratejisinin temelini oluşturup oluşturmadığını belirleyecektir.
