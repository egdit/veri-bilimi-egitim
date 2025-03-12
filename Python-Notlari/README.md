# 🐍 Veri Bilimi için Python Notları

Bu bölüm, veri bilimi projelerinde sık kullanılan Python fonksiyonları ve metodlarını içermektedir.

## 🚀 1. List Comprehension (Liste Anlama)
Python'da hızlı ve okunabilir listeler oluşturmak için kullanılır.

```python
sayilar = [x for x in range(10) if x % 2 == 0]
print(sayilar)  # Çıktı: [0, 2, 4, 6, 8]
```

## 🔹 2. Lambda Fonksiyonları (Anonim Fonksiyonlar)
Tek satırlık fonksiyonlar yazmak için kullanılır.

```python
kare_al = lambda x: x ** 2
print(kare_al(5))  # Çıktı: 25
```

## 💊 3. Map, Filter ve Reduce Fonksiyonları
Bu fonksiyonlar, diziler ve listeler üzerinde işlem yaparken kullanılır.

```python
sayilar = [1, 2, 3, 4, 5]

# Her sayıyı karesiyle değiştirme
kareler = list(map(lambda x: x**2, sayilar))
print(kareler)  # Çıktı: [1, 4, 9, 16, 25]

# Çift sayıları filtreleme
ciftler = list(filter(lambda x: x % 2 == 0, sayilar))
print(ciftler)  # Çıktı: [2, 4]
```

## 📚 4. JSON ve CSV Dosyalarını Okuma
Veri analizi yaparken sık kullanılan dosya formatlarıdır.

```python
import pandas as pd

# CSV dosyası okuma
df = pd.read_csv("veri.csv")

# JSON dosyası okuma
import json
with open("veri.json") as f:
    data = json.load(f)
