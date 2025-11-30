# https://github.com/kkadir8/FET312_DeepPark_Proje.git
DeepPark

Model Uygulama ve Test Süreci (Abdulkadir Gedik)

Bu çalışmada, otopark doluluk tespiti probleminin temel başarımını (baseline) belirlemek amacıyla standart katmanlara sahip sade ve temel bir CNN modeli oluşturulmuş ve test edilmiştir. Uygulanan adımlar şöyledir:

Veri Ön İşleme: Veri seti ImageFolder yapısı ile yüklenmiş, tüm görüntüler 64x64 piksel boyutuna getirilmiş ve veri seti rastgele olarak %80 Eğitim (7199 görsel), %20 Test (1800 görsel) verisi şeklinde ayrılmıştır.

Model Mimarisi: Modelde temel öznitelik çıkarımı için iki adet konvolüsyon katmanı (Conv2d), doğrusal olmayan ilişkileri öğrenmek için standart ReLU aktivasyon fonksiyonu ve boyut azaltma için Max Pooling (2x2) katmanları kullanılmıştır.

Eğitim Konfigürasyonu: Model, Adam optimizasyon algoritması (lr=0.001) ve sınıflandırma problemleri için uygun olan CrossEntropyLoss kayıp fonksiyonu ile derlenmiştir.

Test: Model 3 epoch (dönem) boyunca eğitilmiş, eğitim kaybı 0.0895 seviyesinden 0.0037 seviyesine kadar düşmüş ve modelin daha önce hiç görmediği test seti üzerinde %99.94 nihai doğruluk oranı elde edilmiştir.
