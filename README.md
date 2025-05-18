# Marmara Fayı Deprem Verisi Analizi (2000–2025)

Bu proje, Python ile Veri Analizi dersi kapsamında gerçekleştirilmiştir. Veri kümesi, Marmara Bölgesi’ne ait 2000–2025 yılları arasındaki deprem ve fay hattı verilerini içermektedir. Proje kapsamında `pandas` kullanılarak veri temizleme, özetleme, eksik değer analizi, frekans dağılımları ve temel analizler yapılmıştır.

## 📂 Kullanılan Veri Seti

- Dosya adı: `marmara_faults_earthquakes_2000_2025.csv`
- Gözlem sayısı: 21.605 satır
- Sütun sayısı: 23

## 🔧 Kullanılan Kütüphaneler

- Python 3.12.7
- Pandas 2.2.2
- Numpy
- Matplotlib
- YData Profiling (isteğe bağlı)

## 🔍 Uygulanan Adımlar

1. Veri seti `pandas` ile okundu ve bir DataFrame'e dönüştürüldü.
2. Verinin özet bilgisi (`.info()`) ve ilk/son 5 satırı listelendi.
3. Kütüphane ve Python sürüm bilgileri alındı.
4. Sütun isimleri, sütun sayısı, satır sayısı bulundu.
5. Nümerik ve kategorik sütunlar ayrıştırıldı.
6. Eksik veriler analiz edildi ve dolduruldu veya çıkarıldı.
7. Tekrarlı kayıtlar tespit edildi.
8. Frekans dağılımları analiz edildi.
9. Tüm işlemler sonrasında temiz bir DataFrame elde edildi.

## 📈 Örnek Kod

```python
import pandas as pd

df = pd.read_csv("marmara_faults_earthquakes_2000_2025.csv")
print(df.info())

# Eksik veri sayısı
print(df.isnull().sum())

# Nümerik sütunlar
print(df.select_dtypes(include=['number']).columns)
