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

1. **Veri Üretimi:** CuPy kullanılarak 10 sütun ve 1.000.000 satırdan oluşan 10 MB'lık sahte veri üretildi.
2. **Veri Kaydı:** Üretilen veri `.csv` formatında `data/` klasörüne kaydedildi.
3. **Kümeleme:** cuML içindeki `KMeans` algoritması ile 3 küme oluşturuldu.
4. **Görselleştirme:** Sonuçlar matplotlib ile görselleştirildi.
5. **Notebook:** Tüm işlemler `gpu_kmeans.ipynb` dosyasında adım adım açıklandı.

## 📁 Klasör Yapısı

