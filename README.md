# E-Commerce Shipping Analysis (SQL + Power BI)

Bu projede, e-ticaret süreçlerinde sipariş bazlı kargo performansı analiz edilmiştir.  
Teslimatların zamanında gerçekleşme oranı ve gecikmelere neden olan faktörler incelenmiştir.  
Analiz sonuçları Power BI dashboard’ları ile görselleştirilmiştir.

---

## Proje Amacı

Bu çalışmanın amacı; farklı gönderim yöntemleri, depo blokları ve ürün özelliklerine göre teslimat performansını analiz etmek ve gecikmelere neden olan temel faktörleri tespit etmektir.

---

## Cevaplanan İş Soruları
- Teslimatların ne kadarı zamanında gerçekleşiyor?  
- Gecikmeler hangi gönderim tiplerinde daha yoğun?  
- Hangi depo blokları daha fazla yük altında?  
- Ürün önemi teslimat performansını nasıl etkiliyor?  
- Gecikmelere en çok hangi operasyonel faktörler neden oluyor?

---

## Analiz Süreci
1. E-ticaret kargo verisi incelenmiş ve doğrulanmıştır.  
2. Sipariş bazlı teslimat performans metrikleri hesaplanmıştır.  
3. Gönderim tipi, depo bloğu ve ürün önemi gibi kırılımlar analiz edilmiştir.  
4. Bulgular iki farklı Power BI dashboard ile görselleştirilmiştir.

---

## Power BI Dashboard'ları

### 1️) E-Commerce Shipping Performance Overview (E-Ticaret Kargo Performans Genel Görünümü)
Bu dashboard, genel teslimat performansını üst seviyede analiz etmeyi sağlar.  

**Temel Bulgular:**
- Toplam 10.999 siparişin %59,7’si zamanında, %40,3’ü gecikmeli teslim edilmiştir  
- Gönderim yöntemleri (Flight, Ship, Road) arasında zamanında teslim oranı büyük ölçüde benzerdir  
- Depo blokları arasında performans farkı sınırlıdır, operasyonel süreçler genel olarak dengelidir  
- Yüksek öneme sahip ürünlerde zamanında teslim oranı daha yüksektir (önceliklendirme etkisi)

**Dashboard İçeriği:**
- Total orders (Toplam sipariş), on-time orders (zamanında teslim), and late orders (KPI cards) (gecikmeli teslim (KPI kartları))  
- On-time delivery rate by shipment mode (Gönderim tipine göre zamanında teslim oranı)  
- On-time delivery rate by warehouse block (Depo bloğuna göre zamanında teslim oranı)  
- On-time delivery rate by product importance (Ürün önemine göre zamanında teslim oranı)

---

### 2️) Shipping Breakdown Overview – Late Delivery Drivers (Kargo Dağılımı ve Gecikme Analizi (Detaylı İnceleme))
Bu dashboard, gecikmelere neden olan faktörleri detaylı şekilde analiz eder.

**Temel Bulgular:**
- En yüksek sipariş hacmi Ship gönderim tipindedir (yoğunluk → gecikme riski)  
- F depo bloğu en fazla siparişi işlemektedir (kritik operasyon noktası)  
- Gecikmeler, düşük ve orta öneme sahip ürünlerde daha sık görülmektedir  
- Belirli gönderim kombinasyonları (ürün önemi + gönderim tipi + ağırlık grubu) gecikmelerin büyük kısmını oluşturmaktadır

**Dashboard İçeriği:**
- Gönderim tipine göre sipariş dağılımı  
- Depo bloğuna göre sipariş dağılımı  
- Ürün önemine göre sipariş dağılımı  
- Gecikmeye en çok neden olan gönderim profilleri  
- Etkileşimli filtreler (gönderim tipi, depo, ürün önemi)

---

## Veri Kaynağı
- Veri Seti: E-Commerce Shipping Dataset  
- Kaynak: Kaggle  
- Veri Tipi: Sipariş bazlı kargo ve teslimat performans verisi

---

## Proje Yapısı

<pre>
ecommerce-shipping-analysis-powerbi/
│
├── data/
│ └── Ecommerce Shipping Data.csv
│
├── powerbi/
│ ├── shipping_performance_overview.png
│ └── shipping_breakdown_late_delivery_drivers.png
│
├── sql/
│ └── ecommerce_shipping_analysis.sql
│
└── README.md
</pre> 

---

## Genel Değerlendirme

Genel teslimat performansı orta seviyede olsa da gecikmeler önemli bir oran oluşturmaktadır.  
Analiz sonuçları; sipariş yoğunluğu, depo yükü ve ürün önceliklendirmesinin teslimat performansı üzerinde belirleyici olduğunu göstermektedir.

Bu çalışma, operasyonel süreçlerin iyileştirilmesi ve teslimat performansının artırılması için veri odaklı içgörüler sunmaktadır.
