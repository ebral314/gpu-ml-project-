# gpu-ml-project-
proje
# GPU Destekli Makine Öğrenmesi Projesi

Bu projede, RAPIDS AI kütüphanesi (cuML) kullanılarak GPU üzerinde KMeans algoritması ile kümeleme işlemi gerçekleştirilmiştir. CuPy ile 10 MB'lık rastgele veri üretilmiş ve Polars ile hızlı veri işleme gerçekleştirilmiştir.

## 🚀 Kullanılan Kütüphaneler

- cuml
- cupy
- pandas
- polars
- matplotlib
- scikit-learn

## 🧠 Proje Adımları

1. **Veri Üretimi:** CuPy kullanılarak 10 sütun ve 500.000 satırdan oluşan 10 MB'lık sahte veri üretildi.
2. **Veri Kaydı:** Üretilen veri `.csv` formatında `data/` klasörüne kaydedildi.
3. **Kümeleme:** cuML içindeki `KMeans` algoritması ile 3 küme oluşturuldu.
4. **Görselleştirme:** Sonuçlar matplotlib ile görselleştirildi.
5. **Notebook:** Tüm işlemler `gpu_kmeans.ipynb` dosyasında adım adım açıklandı.

## 📁 Klasör Yapısı

README.md dosyası eklendi

import cupy as cp
import pandas as pd

rows = 500_000
cols = 10

# GPU'da rastgele veri üret
data_gpu = cp.random.rand(rows, cols)

# CPU'ya çevir
data_cpu = cp.asnumpy(data_gpu)

# DataFrame oluştur
df = pd.DataFrame(data_cpu, columns=[f"feature_{i}" for i in range(cols)])

# CSV olarak kaydet
df.to_csv("data/synthetic_data.csv", index=False)

print("Veri başarıyla oluşturuldu ve kaydedildi!")

import cupy as cp
import pandas as pd
import os

# Klasör var mı kontrol et, yoksa oluştur
os.makedirs("data", exist_ok=True)

# 1 milyon satır x 10 sütunluk rastgele veri (10 MB civarı)
rows = 500.000
cols = 10

data_gpu = cp.random.rand(rows, cols)
data_cpu = cp.asnumpy(data_gpu)

df = pd.DataFrame(data_cpu, columns=[f"feature_{i}" for i in range(cols)])
df.to_csv("data/synthetic_data.csv", index=False)

print("✅ synthetic_data.csv başarıyla oluşturuldu ve kaydedildi!")

README eklendi, GPU destekli veri oluşturma scripti taşındı.
