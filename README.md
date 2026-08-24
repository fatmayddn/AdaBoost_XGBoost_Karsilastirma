# Telco Customer Churn – AdaBoost ve XGBoost Karşılaştırması

Bu projede **Telco Customer Churn** veri seti kullanılarak müşterilerin hizmetten ayrılma (churn) durumlarının tahmin edilmesi amaçlanmıştır.

Çalışmada iki farklı boosting algoritması olan **AdaBoost** ve **XGBoost** modelleri uygulanmış ve performansları karşılaştırılmıştır.

## Projenin Amacı

Telekomünikasyon müşterilerinin mevcut özelliklerinden yararlanarak müşterinin hizmetten ayrılıp ayrılmayacağını tahmin etmek ve farklı boosting algoritmalarının bu problem üzerindeki performansını incelemektir.

Hedef değişken:

- `Churn = 0` → Churn Yok
- `Churn = 1` → Churn Var

## Projede Yapılan İşlemler

- Telco Customer Churn veri setinin yüklenmesi
- `customerID` değişkeninin modelleme dışında bırakılması
- Kategorik değişkenlerin sayısal forma dönüştürülmesi
- Verinin eğitim ve test setlerine ayrılması
- Churn sınıf dağılımının incelenmesi
- `tenure` değişkeninin churn durumuna göre görselleştirilmesi
- AdaBoost modelinin oluşturulması ve eğitilmesi
- Farklı `n_estimators` değerlerinin AdaBoost performansına etkisinin incelenmesi
- XGBoost modelinin oluşturulması ve eğitilmesi
- XGBoost özellik önemlerinin incelenmesi
- Eğitim ve test Log Loss değerlerinin karşılaştırılması
- Confusion Matrix analizi
- ROC Curve ve AUC-ROC karşılaştırması
- 5-Fold Cross Validation uygulanması
- Modellerin eğitim sürelerinin karşılaştırılması
- AdaBoost ve XGBoost modellerinin genel performans karşılaştırması

## Kullanılan Performans Metrikleri

Modeller aşağıdaki metrikler kullanılarak değerlendirilmiştir:

- Accuracy
- Precision
- Recall
- F1 Score
- AUC-ROC
- 5-Fold Cross Validation
- Eğitim Süresi

## 🤖 Kullanılan Modeller

### AdaBoost
Zayıf öğrenicilerin ardışık şekilde eğitilerek güçlü bir sınıflandırıcı oluşturmasını sağlayan boosting algoritmasıdır. Bu çalışmada temel öğrenici olarak `DecisionTreeClassifier(max_depth=1)` kullanılmıştır.

### XGBoost
Gradient Boosting yaklaşımını kullanan, regularizasyon ve çeşitli optimizasyon teknikleri içeren güçlü bir boosting algoritmasıdır.

## Kullanılan Teknolojiler

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- XGBoost
- Google Colab

## Model Karşılaştırması

AdaBoost ve XGBoost modelleri yalnızca Accuracy açısından değil; Precision, Recall, F1 Score, AUC-ROC, Cross Validation sonuçları ve eğitim süreleri açısından da karşılaştırılmıştır.

Bu sayede modellerin Telco Customer Churn problemi üzerindeki performanslarının farklı açılardan değerlendirilmesi amaçlanmıştır.
