# Beyin Tümörü MR Görüntüleri ile Sınıflandırma

Bu repository, **manyetik rezonans (MR) görüntülerinden beyin tümörü sınıflandırması** amacıyla geliştirilmiş derin öğrenme tabanlı bir proje çalışmasını içermektedir.
Bu proje, bir derin öğrenme dersi kapsamında gerçekleştirilen akademik bir ders projesidir. 
Proje kapsamında model eğitimi, değerlendirme süreci, eğitilmiş model dosyası ve Gradio tabanlı basit bir arayüz yer almaktadır.

---

## 📌 Proje Hakkında

Beyin tümörleri, erken teşhis gerektiren ciddi sağlık problemleridir. MR görüntülerinin manuel olarak incelenmesi zaman alıcı ve yoruma açık olduğundan, otomatik sınıflandırma sistemleri büyük önem taşımaktadır.

Bu projede, derin öğrenme yöntemleri kullanılarak MR görüntüleri aşağıdaki dört sınıfa ayrılmaktadır:

- **Glioma**
- **Meningioma**
- **Pituitary (Hipofiz tümörü)**
- **No Tumor (Tümör yok)**

Farklı CNN mimarileri karşılaştırılmış ve en iyi performansı gösteren model nihai model olarak seçilmiştir.

---

## 🧠 Kullanılan Modeller

Çalışma kapsamında aşağıdaki modeller uygulanmış ve karşılaştırılmıştır:

- Temel CNN (sıfırdan eğitilen)
- ResNet50 (Transfer Learning)
- EfficientNet-B0 (Transfer Learning)
- MobileNetV2 (Transfer Learning)

Deneysel sonuçlara göre **temel CNN modeli**, test doğruluğu ve F1-skoru açısından en iyi performansı göstermiştir ve nihai model olarak seçilmiştir.

---

## 📊 Veri Seti

Bu projede kullanılan veri seti Kaggle üzerinden açık erişimlidir:

**Brain Tumor MRI Dataset**  
🔗 https://www.kaggle.com/datasets/masoudnickparvar/brain-tumor-mri-dataset

Veri seti dört sınıftan oluşmakta olup eğitim ve test alt kümelerine ayrılmıştır.

> **Not:**  
> Veri seti repository içerisinde yer almamaktadır.  
> Veri setini indirdikten sonra yerel dizininize ekleyip notebook içerisindeki yol ayarlarını güncellemeniz gerekmektedir.

---

## 📁 Klasör Yapısı

- **`notebooks/`**
  - `train.ipynb`  
    Veri ön işleme, model eğitimi, değerlendirme ve farklı mimarilerin karşılaştırılmasını içeren eğitim notebook’u.
  - `gradio.ipynb`  
    Eğitilmiş modeli kullanarak MR görüntüleri üzerinde tahmin yapılmasını sağlayan Gradio tabanlı arayüz.

- **`models/`**
  - `final_baseline_cnn_model.keras`  
    En iyi performansı gösteren ve nihai model olarak seçilen eğitilmiş CNN modeli.

- **`report/`**
  - `rapor.pdf`  
    Projenin detaylı raporu (problem tanımı, yöntem, deneyler ve sonuçlar).

---

## 📌 Notlar

- Bu proje **akademik ve eğitim amaçlıdır**.
- Elde edilen sonuçlar klinik tanı amacıyla kullanılmamalıdır.

---
