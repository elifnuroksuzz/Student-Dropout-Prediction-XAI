# Yükseköğretimde Öğrenci Terkinin Tahmini: Karşılaştırmalı ML ve XAI Yaklaşımı

Bu depo, Portekiz'deki bir yükseköğretim kurumundan elde edilen verilerle öğrenci terkini (dropout) tahmin etmeye yönelik geliştirilen akademik çalışmanın kaynak kodlarını içermektedir[cite: 6]. [cite_start]Çalışma, makine öğrenmesi modellerini **Açıklanabilir Yapay Zeka (XAI)** teknikleriyle birleştirerek şeffaf bir karar destek mekanizması sunar.

## 🚀 Öne Çıkan Özellikler
* [cite_start]**Veri Sızıntısı (Data Leakage) Önleme:** SMOTE algoritması, `imblearn.pipeline` yapısı kullanılarak her çapraz doğrulama katlantısında ayrı ayrı uygulanmıştır.
* [cite_start]**Gelişmiş Özellik Mühendisliği:** Akademik gelişim trendlerini yansıtan 10 yeni öznitelik türetilmiştir (Örn: `Overall Success Rate`, `Grade Change`).
* [cite_start]**Kapsamlı Model Karşılaştırması:** LightGBM, XGBoost, Random Forest dahil 13 farklı algoritma 6 farklı deney senaryosunda test edilmiştir.
* [cite_start]**XAI Entegrasyonu:** Model kararları SHAP (SHapley Additive exPlanations) kullanılarak global, sınıf bazlı ve bireysel düzeyde açıklanmıştır.

## 📊 Önemli Bulgular
* [cite_start]**En Başarılı Model:** LightGBM (%76,61 Doğruluk, 0,7148 F1-Makro).
* [cite_start]**Belirleyici Faktörler:** SHAP analizine göre türetilen akademik başarı oranları ve harç ödeme durumu terk riskinde en kritik rollerdir.
* [cite_start]**İstatistiksel Doğrulama:** Modeller arası farklar Friedman ve Wilcoxon testleri ile doğrulanmıştır ($p<0,001$).

## 📂 Dosya Yapısı
* `Student_Dropout_Analysis_XAI.ipynb`: Veri ön işleme, modelleme ve SHAP analizlerini içeren ana notebook.
* `requirements.txt`: Çalışmanın tekrarlanabilirliği için gerekli kütüphane versiyonları (scikit-learn, lightgbm, shap, vb.).

## 🛠️ Kurulum ve Çalıştırma
1. Bu depoyu klonlayın:
   ```bash
   git clone https://github.com/elifnuroksuz/Student-Dropout-Prediction.git
   ```
2. Gerekli kütüphaneleri yükleyin:
   ```bash
   pip install -r requirements.txt
   ```
3. Veri setini [UCI Machine Learning Repository](https://archive.ics.uci.edu/dataset/697/predict+students+dropout+and+academic+success) üzerinden indirin ve notebook içindeki veri yolunu güncelleyin.
