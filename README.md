# IBM HR Analytics: Employee Attrition Prediction & Performance Analysis

![Python](https://img.shields.io/badge/python-3.8%2B-blue)
![License](https://img.shields.io/badge/license-MIT-green)

Bu proje, IBM HR Analytics veri setini kullanarak çalışan devamsızlık tahmini ve performans faktörlerinin analizini içerir. Makine öğrenmesi modelleriyle %87 doğruluk elde edilmiştir.

## 📋 İçerikler
- [Teknolojiler](#teknolojiler)
- [Veri Seti](#veri-seti)
- [Analiz Süreci](#analiz-süreci)
- [Önemli Bulgular](#önemli-bulgular)
- [Model Performansı](#model-performansı)

## 🛠️ Teknolojiler
- **Python 3.8+**
- **Kütüphaneler**: 
  - Pandas, NumPy (Veri İşleme)
  - Matplotlib, Seaborn (Görselleştirme)
  - Scikit-learn (Random Forest, Gradient Boosting, Logistic Regression)
  - Imbalanced-learn (SMOTE)
- **Veri Kaynağı**: [Kaggle IBM HR Dataset](https://www.kaggle.com/datasets/pavansubhasht/ibm-hr-analytics-attrition-dataset)

## 📊 Veri Seti
- **1470 gözlem**, **35 özellik**
- **Hedef Değişken**: `Attrition` (Ayrılma Durumu)
- **Temel Özellikler**:
  - `Age`, `Department`, `JobRole`
  - `MonthlyIncome`, `YearsAtCompany`
- **Eksik Veri Yok**

## 🔍 Analiz Süreci
1. **Veri Ön İşleme**
   - Gereksiz sütunların çıkarılması
   - Kategorik değişken kodlaması (One-Hot Encoding)
   - Veri normalizasyonu (`StandardScaler`)

2. **Keşifsel Veri Analizi**
   ![Departmana Göre Ayrılma Oranları]
   - Satış departmanında ayrılma oranı: **20.6%**
   - Yaş gruplarına göre dağılım analizi

3. **Model Geliştirme**
   - SMOTE ile veri dengelenmesi
   - GridSearchCV ile hiperparametre optimizasyonu
   - Çapraz doğrulama (5-fold)

## 📌 Önemli Bulgular
- **En Etkili Faktörler**:
  1. Aylık Gelir (`MonthlyIncome`)
  2. Yaş (`Age`)
  3. Toplam Çalışma Süresi (`TotalWorkingYears`)
  
- **Çarpıcı İstatistikler**:
  - 18-25 yaş grubunda ayrılma oranı: **30.4%**
  - İş Tatmini Düşük çalışanlarda ayrılma: **3.2x daha fazla**

## 🏆 Model Performansı
| Model               | Doğruluk | ROC-AUC | Hassasiyet (Ayrılanlar) |
|---------------------|----------|---------|-------------------------|
| Random Forest       | 87.2%    | 0.93    | 72.1%                   |
| Gradient Boosting   | 85.6%    | 0.91    | 68.9%                   |
| Logistic Regression | 82.3%    | 0.88    | 63.4%                   |

