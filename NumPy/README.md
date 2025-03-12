# 📊 NumPy: Sıfırdan Zirveye

NumPy (**Numerical Python**), büyük ölçekli sayısal hesaplamalar ve veri işlemleri için kullanılan en popüler Python kütüphanesidir. **Çok boyutlu diziler (ndarray), hızlı vektör işlemleri ve matematiksel fonksiyonlar** sağlar.

---

## 🚀 1. NumPy Kurulumu

Eğer NumPy yüklü değilse, aşağıdaki komutla yükleyebilirsin:

```bash
pip install numpy
```

Kütüphaneyi içe aktaralım:

```python
import numpy as np
```

---

## 📌 2. NumPy Dizileri (ndarray) Oluşturma

NumPy dizileri (array), Python listelerine benzer ancak **daha hızlı ve verimli** çalışır.

### 📌 2.1 Listeyi NumPy Dizisine Çevirme

```python
import numpy as np

liste = [1, 2, 3, 4, 5]
numpy_dizi = np.array(liste)
print(numpy_dizi)
```

### 📌 2.2 NumPy ile Dizi Oluşturma

```python
np.zeros((3,3))  # 3x3 sıfır matrisi
np.ones((2,2))   # 2x2 birler matrisi
np.full((2,2), 7) # 2x2 7 ile doldurulmuş matris
np.eye(4)        # 4x4 birim matrisi
```

### 📌 2.3 Rastgele Sayılarla Dizi Oluşturma

```python
np.random.rand(3,3)   # 3x3 rastgele sayı matrisi (0-1 arası)
np.random.randint(1,10, (3,3))  # 1-10 arasında rastgele tam sayılarla 3x3 matris
np.random.randn(4,4)  # Normal dağılımlı rastgele sayılar
```

---

## 🔢 3. NumPy Dizi Özellikleri

```python
arr = np.array([[1, 2, 3], [4, 5, 6]])
print("Şekil:", arr.shape)   # (2,3) --> 2 satır, 3 sütun
print("Boyut:", arr.ndim)   # 2 --> 2D bir dizi
print("Eleman Sayısı:", arr.size)   # 6 eleman var
print("Veri Tipi:", arr.dtype)  # int32 veya int64
```

---

## ✂️ 4. NumPy Dizi Dilimleme ve Seçme

```python
arr = np.array([10, 20, 30, 40, 50])
print(arr[1:4])  # 20, 30, 40
print(arr[:3])   # 10, 20, 30
print(arr[-2:])  # 40, 50
```

**2D Dizilerde Seçim:**
```python
mat = np.array([[10, 20, 30], [40, 50, 60], [70, 80, 90]])
print(mat[1, 2])   # 60 (satır 1, sütun 2)
print(mat[:, 1])   # Tüm satırların 2. sütunu
print(mat[0:2, 1:3])  # Üst 2 satır ve son 2 sütun
```

---

## 🧮 5. NumPy Matematiksel İşlemler

```python
arr = np.array([1, 2, 3, 4])
print(arr + 5)  # [6 7 8 9]
print(arr * 2)  # [2 4 6 8]
print(np.exp(arr))  # Üstel fonksiyon
print(np.sqrt(arr))  # Karekök
```

---

## 🔄 6. NumPy Dizi Şekil Değiştirme ve Birleştirme

### 📌 6.1 Yeniden Şekillendirme (Reshape)
```python
arr = np.arange(1, 10)
arr = arr.reshape(3, 3)
print(arr)
```

### 📌 6.2 Dizi Birleştirme
```python
A = np.array([[1, 2], [3, 4]])
B = np.array([[5, 6]])
print(np.vstack((A, B)))  # Dikey birleştirme
print(np.hstack((A, B.T)))  # Yatay birleştirme
```

---

## 🎯 7. NumPy Uygulamaları

### 📌 7.1 Ortalama, Standart Sapma, Min-Max
```python
arr = np.array([10, 20, 30, 40, 50])
print("Ortalama:", np.mean(arr))
print("Standart Sapma:", np.std(arr))
print("Min:", np.min(arr))
print("Max:", np.max(arr))
```

### 📌 7.2 Benzersiz Değerleri Bulma
```python
arr = np.array([1, 2, 2, 3, 4, 4, 5])
print(np.unique(arr))  # [1 2 3 4 5]
```

---

## 🔥 8. NumPy ile Gerçek Dünya Projeleri

✔ **Veri Analizi:** NumPy, Pandas ile birlikte büyük veri kümeleri üzerinde hesaplamalar yapmak için kullanılır.  
✔ **Görselleştirme:** Matplotlib ile grafik çizimleri için veri oluşturma ve manipüle etme işlemlerinde kullanılır.  
✔ **Makine Öğrenmesi:** Büyük veri setleri ile hızlı hesaplamalar yapmak için temel bir kütüphane olarak kullanılır.  

---

## 🎓 Sonuç
Bu rehberde **NumPy kütüphanesini sıfırdan zirveye** kadar öğrendik. Daha fazla bilgi için [NumPy Resmi Dökümantasyonu](https://numpy.org/doc/) adresini ziyaret edebilirsin! 🚀
