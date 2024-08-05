# Asist Bitirme Projesi - Miuul

Bu proje, makine öğrenmesi kullanarak futbol (soccer) verilerini analiz etmeyi ve tahminlerde bulunmayı amaçlamaktadır. Proje, çeşitli makine öğrenmesi algoritmaları kullanılarak futbol oyuncularının kart görme eğilimlerini tahmin etmeyi hedeflemektedir.

## İçindekiler

- [Proje Hakkında](#proje-hakkında)
- [Kullanılan Kütüphaneler](#kullanılan-kütüphaneler)
- [Veri Seti](#veri-seti)
- [Model Eğitimi ve Değerlendirme](#model-eğitimi-ve-değerlendirme)
- [Sonuçlar](#sonuçlar)
- [Nasıl Çalıştırılır](#nasıl-çalıştırılır)
- [Yazar](#yazar)

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

Furkan

Bu proje, Miuul'deki bitirme projesi kapsamında geliştirilmiştir. 



