# 🎙️ Speech Emotion Recognition (Ses Verisinden Duygu Analizi)

Bu proje, ses sinyallerini işleyerek konuşmacının duygu durumunu tespit eden bir makine öğrenmesi sistemidir. **MFFC (Mel-frequency cepstral coefficients)** yöntemi ile özellik çıkarımı yapılmış ve **SVM, MLP, Random Forest** algoritmaları ile modeller eğitilmiştir.

En yüksek başarım, **%93,3 doğruluk oranı** ile **MLP (Multi-Layer Perceptron)** algoritması kullanılarak elde edilmiştir.

## 📋 İçindekiler
- [Proje Hakkında](#-proje-hakkında)
- [Veri Setleri](#-veri-setleri)
- [Yöntem ve Özellik Çıkarımı](#-yöntem-ve-özellik-çıkarımı)
- [Kullanılan Modeller](#-kullanılan-modeller)
- [Sonuçlar ve Performans](#-sonuçlar-ve-performans)
- [Kurulum ve Kullanım](#-kurulum-ve-kullanım)

## 💡 Proje Hakkında
Duygu analizi sistemleri; müşteri hizmetleri (çağrı merkezleri), öneri sistemleri ve kullanıcı deneyimini iyileştirme gibi alanlarda kritik öneme sahiptir. Bu çalışmanın amacı, ham ses verilerini işleyerek konuşmadaki duygusal tonu yüksek doğrulukla sınıflandırmaktır. 

Proje kapsamında ses dosyaları analiz edilmiş, sayısal sinyallere dönüştürülmüş ve çeşitli hiper parametre optimizasyonları ile modellerin performansı maksimize edilmiştir.

## 📊 Veri Setleri
Projede model eğitimi ve doğrulama için iki farklı ve popüler veri seti kullanılmıştır:

1.  **RAVDESS (The Ryerson Audio-Visual Database of Emotional Speech and Song):**
    * Model eğitimi için ana veri seti olarak kullanılmıştır.
    * Dil, aksan ve cümle uzunlukları analiz edilerek veri ön işlemeye tabi tutulmuştur.
2.  **TESS (Toronto Emotional Speech Set):**
    * Eğitilen modellerin başarısını dışsal bir veri seti ile doğrulamak (validation) amacıyla kullanılmıştır.

## ⚙️ Yöntem ve Özellik Çıkarımı
Ses dosyalarından bilgisayarın anlayabileceği anlamlı veriler elde etmek için **MFCC (Mel-frequency cepstral coefficients)** tekniği kullanılmıştır.

* **Süreç:** Ses Dosyası ➡️ Sinyal İşleme ➡️ MFCC Dönüşümü ➡️ Sayısal Matris ➡️ Model Girişi

## 🧠 Kullanılan Modeller
Bu çalışmada üç temel makine öğrenmesi algoritması karşılaştırmalı olarak analiz edilmiştir:

* **MLP (Multi-Layer Perceptron):** Yapay sinir ağları tabanlı sınıflandırma.
* **SVM (Support Vector Machine):** Destek vektör makineleri.
* **RF (Random Forest):** Rastgele orman algoritmaları.

*Her model için farklı hiper parametre varyasyonları denenmiş (Grid Search / Random Search) ve en iyi sonuçlar raporlanmıştır.*

## 🏆 Sonuçlar ve Performans
Eğitilen modeller; **Karmaşıklık Matrisi (Confusion Matrix)**, **Kesinlik (Precision)**, **Duyarlılık (Recall)** ve **F1-Skor** metriklerine göre değerlendirilmiştir.

| Model | En İyi Doğruluk Oranı (Accuracy) |
| :--- | :--- |
| **MLP (Multi-Layer Perceptron)** | **%93.3** 🌟 |
| SVM (Support Vector Machine) | *%XX.X* |
| Random Forest | *%XX.X* |

*> Not: TESS veri seti ile yapılan çapraz doğrulamalar, MLP modelinin genelleme yeteneğinin yüksek olduğunu göstermiştir.*

## 🚀 Kurulum ve Kullanım

Projeyi yerel ortamınızda çalıştırmak için:

1. Repoyu klonlayın:
   ```bash
   git clone [https://github.com/KULLANICI_ADIN/REPO_ISMI.git](https://github.com/KULLANICI_ADIN/REPO_ISMI.git)
