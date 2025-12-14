# DHearth-ML
# Makine Öğrenmesi Yöntemleri ile Kalp Hastalığı Tahmini

Bu proje, *Veri Bilimine Giriş* dersi kapsamında geliştirilmiş olup, klinik ve demografik veriler kullanılarak bireylerde *kalp hastalığı var/yok* durumunun makine öğrenmesi yöntemleriyle tahmin edilmesini amaçlamaktadır.

Projede iki farklı sınıflandırma modeli karşılaştırılmıştır:
- *Lojistik Regresyon*
- *Random Forest*

---

## Proje Özeti

Kalp hastalıkları dünya genelinde en yaygın ölüm nedenlerinden biridir. Erken teşhis, tedavi süreçlerinde kritik rol oynamaktadır. Bu proje kapsamında Kaggle üzerinde yer alan *Heart Disease* veri seti kullanılarak, temel veri bilimi adımları uygulanmış ve iki farklı makine öğrenmesi modeli ile tahmin performansları karşılaştırılmıştır.

---

## Kullanılan Veri Seti

- *Kaynak:* Kaggle – Heart Disease Dataset  
- *Gözlem Sayısı:* 303  
- *Özellik Sayısı:* 13 + 1 hedef değişken  
- *Hedef Değişken:* target
  - 0 → Kalp hastalığı yok  
  - 1 → Kalp hastalığı var  

### Öne Çıkan Özellikler
- age – Yaş  
- cp – Göğüs ağrısı tipi  
- thalach – Maksimum kalp atım hızı  
- oldpeak – ST depresyon değeri  
- ca – Major damar sayısı  

---

## Kullanılan Teknolojiler

- *Python 3*
- *Jupyter Notebook / Visual Studio / VS Code*
- *Kütüphaneler:*
  - pandas
  - numpy
  - matplotlib
  - seaborn
  - scikit-learn

---

## Uygulanan Yöntemler

### 🔹 Veri Ön İşleme
- Eksik veri kontrolü
- Özellik ölçekleme (StandardScaler)
- Eğitim / test ayrımı (%80 / %20, stratified)

### 🔹 Keşifsel Veri Analizi (EDA)
- Hedef değişken dağılımı
- Korelasyon ısı haritası
- Özelliklerin hedef ile ilişkilerinin incelenmesi

### 🔹 Modeller
1. *Lojistik Regresyon*
   - Doğrusal sınıflandırma modeli
   - Yorumlanabilirlik avantajı

2. *Random Forest*
   - Ağaç tabanlı topluluk (ensemble) yöntemi
   - Karmaşık ve doğrusal olmayan ilişkileri yakalama gücü

---

## Model Performansları

### 🔸 Lojistik Regresyon
- *Accuracy:* %80.98
- Pozitif sınıf (kalp hastalığı var) için yüksek recall değeri
- Temel ve karşılaştırma modeli olarak kullanılmıştır

### 🔸 Random Forest
- *Accuracy:* %100
- Test verisindeki tüm örnekler doğru sınıflandırılmıştır
- En başarılı model olarak öne çıkmıştır

| Model | Accuracy |
|------|----------|
| Lojistik Regresyon | %80.98 |
| Random Forest | *%100* |

> Not: Random Forest modelinin %100 doğruluk vermesi, veri setinin küçük ve temiz olmasından kaynaklanmaktadır. Daha büyük veri setlerinde genellenebilirlik ayrıca test edilmelidir.

---

## Özellik Önemleri (Feature Importance)

Random Forest modeli üzerinden yapılan analizde, aşağıdaki değişkenlerin kalp hastalığı tahmininde daha baskın olduğu görülmüştür:

- thalach
- oldpeak
- cp
- ca

Bu değişkenler klinik açıdan da anlamlı sonuçlar sunmaktadır.
