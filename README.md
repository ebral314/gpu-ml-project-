# GPU Destekli Makine Öğrenmesi Projesi

Bu projede, **GPU** ve **CPU** kullanarak veri üretimi, kümeleme (KMeans), sınıflandırma (Random Forest) ve görselleştirme işlemleri gerçekleştirilmiştir.  
Küçük veri setleri için `iris.csv`, büyük veri testleri için ise `synthetic_data.csv` kullanılmıştır.

---

## 🚀 Kullanılan Kütüphaneler

- `cupy`, `cuml` (GPU işlemleri için)
- `pandas`, `polars`
- `scikit-learn`
- `matplotlib`, `seaborn`

---

## 🧠 Proje Aşamaları

### 1. Sahte Veri Üretimi (`veri_olustur.py`)
- `CuPy` kullanılarak 500.000 satır ve 10 sütunluk rastgele veri üretildi.
- `pandas` ile `synthetic_data.csv` olarak `data/` klasörüne kaydedildi.

### 2. Modelleme ve Kümeleme (`main.py`)
- `iris.csv` kullanılarak:
  - `RandomForestClassifier` ile sınıflandırma yapıldı
  - `KMeans` ile 3 kümeye ayrıldı
- Sonuçlar `clustered_data.csv` dosyasına yazıldı
- Veriler matplotlib ile görselleştirildi

### 3. Alternatifler
- GPU destekli `cuML` test edildi ancak yerel CUDA desteği olmadığı için CPU ile devam edildi.
- `.csv` dosyaları proje içindedir.

---



