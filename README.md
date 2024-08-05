# Makine Öğrenmesi ile Futbol Maç Sonucu Tahminlemesi

Bu projede, futbol maçlarında oyuncuların sarı kart görme olasılığını etkileyen faktörler analiz edilerek gelecekteki maçlar için sarı kart tahminleme modeli oluşturulmuştur.

**Proje, 03.08.2024 tarihinde gerçekleşen Süper Kupa Final Maçı olan GS-BJK maçında alınacak sonuçların önceden tahmininde kullanılmıştır.**

## Projenin Hedefi

Bu projenin amacı, futbol maçlarında oyuncuların sarı kart görme olasılığını tahmin etmektir. Bu tahminler, futbol kulüpleri ve teknik direktörler için oyuncu performansını optimize etmek, maç stratejilerini geliştirmek ve disiplin sorunlarını önceden tahmin ederek gerekli önlemleri almak konusunda önemli bir araç olarak kullanılabilir. Proje, futbol analitiği alanında yenilikçi bir yaklaşım sunarak veri odaklı karar alma süreçlerini desteklemeyi amaçlamaktadır.

## İçindekiler
# Read me
- [Proje Hakkında](#proje-hakkında)
- [Kullanılan Kütüphaneler](#kullanılan-kütüphaneler)
- [Veri Seti](#veri-seti)
- [Model Eğitimi ve Değerlendirme](#model-eğitimi-ve-değerlendirme)
- [Sonuçlar](#sonuçlar)
- [Nasıl Çalıştırılır](#nasıl-çalıştırılır)
- [Yazar](#yazar)

## Proje İçindekiler
- [Gerekli Kütüphanelerin Yüklenmesi](#gerekli-kütüphanelerin-yüklenmesi)
- [Veri Setlerinin Yüklenmesi ve Düzenlenmesi](#veri-setlerinin-yüklenmesi-ve-düzenlenmesi)
- [Veri Birleştirme ve Temizleme](#veri-birleştirme-ve-temizleme)
- [Veri Analizi ve Görselleştirme](#veri-analizi-ve-görselleştirme)
- [Model Oluşturma](#model-oluşturma)
- [Sonuç ve Değerlendirme](#sonuç-ve-değerlendirme)
- [Örnek Tahmin](#örnek-tahmin)
- [Katkıda Bulunma](#katkıda-bulunma)
- [Lisans](#lisans)

## Proje Hakkında

Bu projede, futbol oyuncularının maç performansları ve disiplin cezaları (örneğin, sarı kart, kırmızı kart) gibi veriler kullanılarak oyuncuların kart görme eğilimleri tahmin edilmektedir. Proje, hiyerarşik kümeleme ve sınıflandırma algoritmaları ile bu verileri analiz etmektedir.

## Kullanılan Kütüphaneler

Bu proje aşağıdaki Python kütüphanelerini kullanmaktadır:

- pandas (pd): Veri manipülasyonu ve analizi için.
- numpy (np): Bilimsel hesaplamalar ve matris işlemleri için.
- scikit-learn: Model eğitimi ve değerlendirmesi için
- xgboost (XGBClassifier): XGBoost sınıflandırıcı.
- imbalanced-learn (SMOTE): Sınıf dengesizliğini gidermek için SMOTE algoritması.
- sklearn.preprocessing (LabelEncoder): Kategorik verileri sayısal değerlere dönüştürmek için.
- matplotlib.pyplot (plt): Grafikler oluşturmak için.
- seaborn (sns): Veri görselleştirme için.
- time: Zaman hesaplamaları için.
- warnings: Uyarı yönetimi için.
- sklearn.exceptions (ConvergenceWarning): Modelin konverjans uyarıları için.

## Veri Seti

9 ayrı veri seti kullanılarak oluşturulan csv dosyası birçok yeni özellik bulundurmaktadır. Proje, futbol oyuncularının performans verilerini içeren bir veri seti kullanmaktadır. Veri seti aşağıdaki özellikleri içermektedir:

- player_id: Oyuncunun benzersiz kimlik numarası.
- attendance: Maçta oyuncunun seyirci sayısı.
- referee: Maçın hakemi (metin olarak ifade edilen bir kategori).
- position: Oyuncunun maçtaki pozisyonu (metin olarak ifade edilen bir kategori).
- starting: Oyuncunun maça başlangıçta dahil olup olmadığı (0 veya 1 gibi bir değer).
- team_captain: Oyuncunun takım kaptanı olup olmadığı (0 veya 1 gibi bir değer).
- yellow_cards: Oyuncunun aldığı sarı kart sayısı.
- minutes_played: Oyuncunun maçta oynadığı süre (dakika olarak).
- hosting: Maçın ev sahibi takımda olup olmadığı (0 veya 1 gibi bir değer).
- age: Oyuncunun yaşı.
- last_20: Oyuncunun son 20 maçtaki performansı (belirli bir ölçüm).
- first_20: Oyuncunun ilk 20 maçtaki performansı (belirli bir ölçüm).
- attendance_rate: Oyuncunun maçlarda bulunma oranı.
- referee_card_avg: Hakemlerin kart ortalaması (oyuncunun kart durumuna etkisi).
- importance: Oyuncunun maçtaki önemi (genellikle bir ölçüm veya skor).
- experience: Oyuncunun deneyim seviyesi (yıl olarak ifade edilen bir ölçüm).
- minutes_in_last_4_matches: Son 4 maçta oyuncunun oynadığı toplam süre (dakika olarak).
- total_cards_in_game: Maçtaki toplam kart sayısı (sarısı ve kırmızısı dahil).
- player_card_av: Oyuncunun ortalama kart sayısı (sarısı ve kırmızısı dahil).

## Model Eğitimi ve Değerlendirme

Proje, çeşitli makine öğrenmesi algoritmaları ile oyuncuların kart görme eğilimlerini tahmin etmektedir. Kullanılan modeller ve değerlendirme metrikleri şunlardır:

- DecisionTreeClassifier
- RandomForestClassifier.
- KNeighborsClassifier
- StandardScaler
- RandomForestClassifier
- accuracy_score
- precision_score
- recall_score
- f1_score
- confusion_matrix
- 
## Sonuçlar

Proje, oyuncuların kart görme eğilimlerini tahmin etmek için kullanılan modellerin performansını değerlendirmektedir. Performans metrikleri arasında doğruluk (accuracy), kesinlik (precision), geri çağırma (recall) ve F1 skoru bulunmaktadır.


| Model | Eğitim Doğruluğu | Test Doğruluğu | F1 Skoru | Recall | Precision |
|----------|----------|----------|----------|----------|----------|
| KNN | 0.8998 | 0.8554 | 0.8546 | 0.8554 | 0.8578 |
| Random Forest | 0.9999 | 0.8733 | 0.8717 | 0.8733 | 0.8722 |
| Decision Tree | 1.0000 | 0.7902 | 0.7910 | 0.7902 | 0.7920 |
| Gradient Boosting | 0.9113 | 0.8681 | 0.8677 | 0.8681 | 0.8677 |
| XGBoost | 0.9997 | 0.8985 | 0.8717 | 0.9012 | 0.9013 |

## GS-BJK Süper Kupa Finali (03.08.2024) Maçı için Sarı Kart Tahminlemesi




## Nasıl Çalıştırılır

Projenin çalıştırılması için aşağıdaki adımları izleyebilirsiniz:

1. Gerekli kütüphaneleri yükleyin:
    ```bash
    pip install pandas numpy scikit-learn seaborn matplotlib
    ```

2. Proje dosyasını çalıştırın:
    ```python
    jupyter notebook asist_BitirmeProjesi_miuul.ipynb
    ```

3. Jupyter Notebook'u açın ve hücreleri sırasıyla çalıştırın.

## Yazar

Gizem, Şahin, Çağlar,Leyla ve Elçin tarafından hazırlanmıştır.

Bu proje, Miuul'deki bitirme projesi kapsamında geliştirilmiştir. 



