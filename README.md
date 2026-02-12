FLO CLTV Prediction with BG-NBD & Gamma-Gamma 👟📊

Bu proje, FLO'nun satış ve pazarlama stratejilerini belirlemek amacıyla müşterilerin gelecekteki potansiyel değerlerini BG-NBD ve Gamma-Gamma modelleri kullanarak tahmin etmeyi hedefler.

📌 İş Problemi (Business Problem)
FLO, orta ve uzun vadeli yol haritası belirleyebilmek için mevcut müşterilerinin şirkete sağlayacağı potansiyel değeri (Customer Lifetime Value) bilmek istemektedir. Bu sayede pazarlama bütçesini daha verimli kullanabilir ve sadık müşterilerine yönelik özel stratejiler geliştirebilir.

🗂 Veri Seti Hikayesi
Veri seti, 2020 - 2021 yıllarında FLO'dan hem online hem de offline (Omnichannel) alışveriş yapan müşterilerin geçmiş davranışlarından oluşmaktadır.

master_id: Eşsiz müşteri numarası

order_num_total: Toplam alışveriş sayısı (Online + Offline)

customer_value_total: Toplam harcama (Online + Offline)

first_order_date: İlk alışveriş tarihi

last_order_date: Son alışveriş tarihi

interested_in_categories_12: Son 12 ayda alışveriş yapılan kategoriler

🛠 Kullanılan Modeller ve Teknolojiler
1. BG-NBD (Beta Geometric / Negative Binomial Distribution)
Müşterilerin gelecekte yapacakları satın alma sayısını (Expected Number of Transactions) tahmin etmek için kullanılır. "Buy Till You Die" prensibiyle çalışır; müşterinin alışveriş yapma sıklığını ve olasılıksal olarak "churn" (terk etme) durumunu analiz eder.

2. Gamma-Gamma Submodel
Müşterilerin işlem başına bırakacakları ortalama kârı (Expected Average Profit) tahmin etmek için kullanılır. İşlem sayısı ve işlem değeri arasındaki ilişkiyi olasılıksal olarak modeller.

3. CLTV Hesaplama
BG-NBD ve Gamma-Gamma modellerinden gelen çıktılar birleştirilerek belirli bir zaman projeksiyonu (örn: 6 ay veya 1 yıl) için CLTV tahmini yapılır.

🚀 Proje Adımları
Veri Hazırlama: Aykırı değerlerin (outliers) baskılanması ve tarih değişkenlerinin tip dönüşümleri.

RFM Metriklerinin CLTV Yapısına Dönüştürülmesi: Recency, T (Tenure), Frequency ve Monetary değerlerinin haftalık cinsten hazırlanması.

BG-NBD Model Fit: 3 ve 6 aylık beklenen satış tahminlerinin oluşturulması.

Gamma-Gamma Model Fit: Beklenen ortalama değer tahmini.

Segmentasyon: CLTV skorlarına göre müşterilerin A, B, C ve D gruplarına ayrılması.

📊 Örnek Çıktı ve Segmentler
Proje sonunda müşteriler 6 aylık tahmin edilen CLTV değerlerine göre segmente edilmiştir:

A Segmenti: En yüksek değere sahip "Premium" müşteriler.

D Segmenti: En düşük değere sahip veya kaybedilme riski yüksek müşteriler.
