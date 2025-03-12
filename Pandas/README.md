# 📊 Pandas: Sıfırdan Zirveye

**Pandas**, veri analizi ve veri manipülasyonu için kullanılan en popüler Python kütüphanelerinden biridir. **Veri setlerini kolayca okuyabilir, işleyebilir ve analiz edebilirsin.** Pandas, özellikle **DataFrame** ve **Series** yapılarıyla öne çıkar.

---

## 🚀 1. Pandas Kurulumu

Eğer Pandas yüklü değilse, aşağıdaki komutla yükleyebilirsin:

```bash
pip install pandas
```

Kütüphaneyi içe aktaralım:

```python
import pandas as pd
```

---

## 📌 2. Pandas Veri Yapıları: Series ve DataFrame

### **2.1 Series (Tek Boyutlu Veri Yapısı)**

Series, tek boyutlu bir veri yapısıdır. Liste veya sözlükten kolayca oluşturulabilir.

```python
import pandas as pd

data = [10, 20, 30, 40]
seri = pd.Series(data)
print(seri)
```

Series nesnesine indeks vererek daha okunabilir hale getirebiliriz:

```python
seri = pd.Series([100, 200, 300], index=['a', 'b', 'c'])
print(seri)
```

---

### **2.2 DataFrame (İki Boyutlu Veri Yapısı)**

DataFrame, **satır ve sütunlardan oluşan** bir veri yapısıdır. Genellikle CSV veya Excel dosyalarındaki veriler bu yapıdadır.

```python
data = {
    'İsim': ['Ali', 'Veli', 'Ayşe'],
    'Yaş': [25, 30, 22],
    'Maaş': [5000, 7000, 4500]
}

df = pd.DataFrame(data)
print(df)
```

---

## 📂 3. Pandas ile Veri Okuma ve Yazma

### 📌 3.1 CSV Dosyası Okuma
```python
df = pd.read_csv("veri.csv")
print(df.head())  # İlk 5 satırı gösterir
```

### 📌 3.2 Excel Dosyası Okuma
```python
df = pd.read_excel("veri.xlsx")
print(df.head())
```

### 📌 3.3 CSV Dosyasına Yazma
```python
df.to_csv("yeni_veri.csv", index=False)
```

---

## 🔍 4. DataFrame Üzerinde İşlemler

### 📌 4.1 Veri Çerçevesinin Genel Bilgilerini Görme
```python
print(df.info())  # Veri türlerini ve eksik verileri gösterir
print(df.describe())  # Sayısal sütunların istatistiklerini gösterir
```

### 📌 4.2 Sütun Seçme
```python
print(df['İsim'])  # Sadece İsim sütununu getirir
print(df[['İsim', 'Yaş']])  # Birden fazla sütunu seçmek
```

### 📌 4.3 Satır Seçme
```python
print(df.loc[0])  # İlk satırı getirir
print(df.iloc[1:3])  # 1. ve 2. indeksli satırları getirir
```

### 📌 4.4 Filtreleme
```python
print(df[df['Yaş'] > 25])  # Yaşı 25'ten büyük olanları getirir
```

---

## 🔄 5. Veri Manipülasyonu

### 📌 5.1 Eksik Verileri Bulma
```python
print(df.isnull().sum())  # Eksik verilerin toplamını gösterir
```

### 📌 5.2 Eksik Verileri Doldurma
```python
df.fillna(df.mean(), inplace=True)  # Eksik değerleri sütunun ortalaması ile doldur
```

### 📌 5.3 Sütun Ekleme ve Silme
```python
df['Yeni_Sütun'] = df['Yaş'] * 2  # Yeni sütun ekleme

df.drop('Yeni_Sütun', axis=1, inplace=True)  # Sütunu silme
```

---

## 📊 6. Veri Görselleştirme ile Kullanımı

Pandas, **Matplotlib ve Seaborn** ile veri görselleştirme işlemlerini kolaylaştırır.

```python
import matplotlib.pyplot as plt

df['Yaş'].hist()
plt.show()
```

---

## 🎯 7. Pandas ile Gerçek Dünya Projeleri

✔ **Veri Analizi:** Büyük veri setleri üzerinde hızlı analizler yapabilirsin.  
✔ **Makine Öğrenmesi:** Veri setlerini temizleyerek model eğitimi için uygun hale getirebilirsin.  
✔ **Finans ve İş Zekası:** Şirket gelir-gider analizleri yapabilirsin.  

---

## 🎓 Sonuç
Bu rehberde **Pandas kütüphanesini sıfırdan zirveye** kadar öğrendik. Daha fazla bilgi için [Pandas Resmi Dökümantasyonu](https://pandas.pydata.org/docs/) adresini ziyaret edebilirsin! 🚀
