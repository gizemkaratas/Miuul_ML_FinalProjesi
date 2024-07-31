# Makine Öğrenmesi ile Futbol Maçlarında Oyuncuların Sarı Kart Görme Olasılığının Tahmin Edilmesi

Bu proje, futbol maçlarında oyuncuların sarı kart görme olasılığını etkileyen faktörleri analiz etmeyi ve bu bilgiler ışığında gelecekteki maçlar için sarı kart tahminleme modeli oluşturmayı hedeflemektedir.

## Proje Hakkında

İlk aşamada, oyuncuların yaşı, pozisyonu, oynadığı takım, teknik direktörü, sahada kaldığı süre, maçın oynandığı stadyum, seyirci sayısı, maçın önemi ve hakem gibi değişkenleri dikkate alarak sarı kart görme olasılıklarını değerlendireceğiz. Bu analiz kapsamında, sarı kart görme eğilimlerini anlamak için keşifsel veri analizi ve görselleştirme tekniklerini kullanacağız. Elde edilen bulgular doğrultusunda, makine öğrenimi algoritmalarıyla gelecekteki maçlarda hangi oyuncuların sarı kart göreceğini tahmin eden bir model geliştireceğiz. Bu model, futbol kulüpleri ve teknik direktörler için oyuncu performansını optimize etmek, maç stratejilerini geliştirmek ve disiplin sorunlarını önceden tahmin ederek gerekli önlemleri almak konusunda önemli bir araç olarak kullanılabilir.

## Gereksinimler

Bu projeyi çalıştırmak için aşağıdaki kütüphanelerin yüklü olması gerekmektedir:

- pandas
- numpy
- matplotlib
- seaborn
# Futbol Maç Sonucu Tahminlemesi

Bu projede, futbol maçlarında oyuncuların sarı kart görme olasılığını etkileyen faktörler analiz edilerek gelecekteki maçlar için sarı kart tahminleme modeli oluşturulmuştur. 

## Projenin Hedefi

Bu projenin amacı, futbol maçlarında oyuncuların sarı kart görme olasılığını tahmin etmektir. Bu tahminler, futbol kulüpleri ve teknik direktörler için oyuncu performansını optimize etmek, maç stratejilerini geliştirmek ve disiplin sorunlarını önceden tahmin ederek gerekli önlemleri almak konusunda önemli bir araç olarak kullanılabilir. Proje, futbol analitiği alanında yenilikçi bir yaklaşım sunarak veri odaklı karar alma süreçlerini desteklemeyi amaçlamaktadır.

## İçindekiler

- [Gerekli Kütüphanelerin Yüklenmesi](#gerekli-kütüphanelerin-yüklenmesi)
- [Veri Setlerinin Yüklenmesi ve Düzenlenmesi](#veri-setlerinin-yüklenmesi-ve-düzenlenmesi)
- [Veri Birleştirme ve Temizleme](#veri-birleştirme-ve-temizleme)
- [Veri Analizi ve Görselleştirme](#veri-analizi-ve-görselleştirme)
- [Model Oluşturma](#model-oluşturma)
- [Katkıda Bulunma](#katkıda-bulunma)
- [Lisans](#lisans)

## Gerekli Kütüphanelerin Yüklenmesi

Projede kullanılacak kütüphaneler aşağıda belirtilmiştir. Bu kütüphaneleri yüklemek için aşağıdaki kodları kullanabilirsiniz:

```python
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns
import warnings
import matplotlib
from sklearn.exceptions import ConvergenceWarning

pd.set_option("display.max_columns", None)
pd.set_option("display.float_format", lambda x: "%.3f" % x)

warnings.simplefilter(action='ignore', category=FutureWarning)
warnings.simplefilter("ignore", category=ConvergenceWarning)

Bu kütüphaneleri yüklemek için aşağıdaki komutu kullanabilirsiniz:

```bash
pip install pandas numpy matplotlib seaborn

## Kullanım
# Futbol Maç Sonucu Tahminlemesi

Bu projede, futbol maçlarında oyuncuların sarı kart görme olasılığını etkileyen faktörler analiz edilerek gelecekteki maçlar için sarı kart tahminleme modeli oluşturulmuştur. 

## Projenin Hedefi

Bu projenin amacı, futbol maçlarında oyuncuların sarı kart görme olasılığını tahmin etmektir. Bu tahminler, futbol kulüpleri ve teknik direktörler için oyuncu performansını optimize etmek, maç stratejilerini geliştirmek ve disiplin sorunlarını önceden tahmin ederek gerekli önlemleri almak konusunda önemli bir araç olarak kullanılabilir. Proje, futbol analitiği alanında yenilikçi bir yaklaşım sunarak veri odaklı karar alma süreçlerini desteklemeyi amaçlamaktadır.

## İçindekiler

- [Gerekli Kütüphanelerin Yüklenmesi](#gerekli-kütüphanelerin-yüklenmesi)
- [Veri Setlerinin Yüklenmesi ve Düzenlenmesi](#veri-setlerinin-yüklenmesi-ve-düzenlenmesi)
- [Veri Birleştirme ve Temizleme](#veri-birleştirme-ve-temizleme)
- [Veri Analizi ve Görselleştirme](#veri-analizi-ve-görselleştirme)
- [Model Oluşturma](#model-oluşturma)
- [Katkıda Bulunma](#katkıda-bulunma)
- [Lisans](#lisans)

## Gerekli Kütüphanelerin Yüklenmesi

Projede kullanılacak kütüphaneler aşağıda belirtilmiştir. Bu kütüphaneleri yüklemek için aşağıdaki kodları kullanabilirsiniz:

```python
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns
import warnings
import matplotlib
from sklearn.exceptions import ConvergenceWarning

pd.set_option("display.max_columns", None)
pd.set_option("display.float_format", lambda x: "%.3f" % x)

warnings.simplefilter(action='ignore', category=FutureWarning)
warnings.simplefilter("ignore", category=ConvergenceWarning)

