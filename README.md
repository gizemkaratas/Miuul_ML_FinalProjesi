# Makine Öğrenmesi ile Futbol Maç Sonucu Tahminlemesi

Bu projede, futbol maçlarında oyuncuların sarı kart görme olasılığını etkileyen faktörler analiz edilerek gelecekteki maçlar için sarı kart tahminleme modeli oluşturulmuştur. 

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
- [Katkıda Bulunma](#katkıda-bulunma)
- [Lisans](#lisans)

## Proje Hakkında

Bu projede, futbol oyuncularının maç performansları ve disiplin cezaları (örneğin, sarı kart, kırmızı kart) gibi veriler kullanılarak oyuncuların kart görme eğilimleri tahmin edilmektedir. Proje, hiyerarşik kümeleme ve sınıflandırma algoritmaları ile bu verileri analiz etmektedir.

## Kullanılan Kütüphaneler

Bu proje aşağıdaki Python kütüphanelerini kullanmaktadır:

- pandas
- numpy
- scikit-learn
- seaborn
- matplotlib

## Veri Seti

Proje, futbol oyuncularının performans verilerini içeren bir veri seti kullanmaktadır. Veri seti aşağıdaki özellikleri içermektedir:

- goals: Gol sayısı
- assists: Asist sayısı
- red_cards: Kırmızı kart sayısı
- games_played: Oynanan maç sayısı
- minutes_played: Oynanan dakika sayısı

## Model Eğitimi ve Değerlendirme

Proje, çeşitli makine öğrenmesi algoritmaları ile oyuncuların kart görme eğilimlerini tahmin etmektedir. Kullanılan modeller ve değerlendirme metrikleri şunlardır:

- RandomForestClassifier
- accuracy_score
- precision_score
- recall_score
- f1_score
- confusion_matrix

## Sonuçlar

Proje, oyuncuların kart görme eğilimlerini tahmin etmek için kullanılan modellerin performansını değerlendirmektedir. Performans metrikleri arasında doğruluk (accuracy), kesinlik (precision), geri çağırma (recall) ve F1 skoru bulunmaktadır.

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



