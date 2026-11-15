# ClimateData – İklim Verisi Analizi

Meteoroloji Genel Müdürlüğü'nün ham istasyon verilerinden, Doğu Karadeniz'deki 4 il (Trabzon, Giresun, Rize, Artvin) için temiz ve analiz edilebilir günlük iklim veri seti üreten çalışma. Bu repoda örnek olarak **10 cm toprak sıcaklığı** verisi gösterilmiştir.

![Python](https://img.shields.io/badge/Python-3776AB?logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?logo=pandas&logoColor=white)
![Google Colab](https://img.shields.io/badge/Google%20Colab-F9AB00?logo=googlecolab&logoColor=white)
![Power BI](https://img.shields.io/badge/Power%20BI-F2C811?logo=powerbi&logoColor=black)

## Veri

| | |
| --- | --- |
| Kaynak | Meteoroloji Genel Müdürlüğü (MGM) |
| Dönem | 1980 – 2025 |
| Kapsam | 4 il, 128 meteoroloji istasyonu |
| Ham veri | 161.080 istasyon kaydı |
| Çıktı | 67.208 satırlık il bazlı günlük veri seti |

Ham veri MGM'ye ait olduğu için repoda paylaşılmamaktadır.

## Yapılanlar

1. **Veri temizleme ve düzenleme:** İstasyon numaraları illerle eşleştirildi, tarih sütunu oluşturuldu.
2. **İl bazlı günlük veri seti:** Aynı ildeki istasyonların değerleri **medyan** yöntemiyle birleştirildi. Medyan, tek bir istasyondaki hatalı ölçümün il değerini bozmasını engeller.
3. **Mevsimsel ayrıştırma:** Her kayıt astronomik mevsim tarihlerine göre etiketlendi.
4. **Trend analizi:** Her il ve mevsim için yıllık ve 10 yıllık sıcaklık değişimi (°C) hesaplandı.
5. **Aykırı yıl tespiti:** Uzun dönem ortalamasından ±1 standart sapmadan fazla ayrışan yıllar işaretlendi, grafik ve tablo olarak raporlandı.
6. **KPI özeti:** İl ve mevsim bazında aykırı yıl sayısı ile ilk ve son aykırı yıl çıkarıldı.
7. **Power BI:** DAX fonksiyonlarıyla aykırı yıl ve değerler panoda gösterildi.

## Dosyalar

| Dosya | İçerik |
| --- | --- |
| [`Medyan_10cm_ort.ipynb`](Medyan_10cm_ort.ipynb) | Temizleme, medyan birleştirme, trend ve aykırı yıl analizi |

## Çalıştırma

Not defteri Google Colab için yazılmıştır. Ham CSV dosyasını Google Drive'a yükleyip not defterindeki dosya yolunu güncelledikten sonra hücreleri sırayla çalıştırmak yeterlidir.

Gerekli kütüphaneler: `pandas`, `numpy`, `matplotlib`

## Ekran Görüntüleri

<img width="658" height="618" alt="Trend analizi tablosu" src="https://github.com/user-attachments/assets/be4b38af-b255-4a31-abbf-2940a000111a" />
<img width="286" height="241" alt="Power BI aykırı yıl göstergesi" src="https://github.com/user-attachments/assets/49f46d30-965b-4639-bfbc-6a39834e6d5e" />
<img width="961" height="442" alt="Aykırı yıl grafiği" src="https://github.com/user-attachments/assets/d20671d8-7697-4330-8ff8-45b06d4d82fd" />
<img width="934" height="451" alt="Yıllık ortalama grafiği" src="https://github.com/user-attachments/assets/cca7db87-f340-4d6f-84d1-a5cdd1a7e490" />

## İletişim

Azra Dinler · [GitHub](https://github.com/azradnlr06)
