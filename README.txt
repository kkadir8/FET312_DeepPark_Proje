# https://github.com/kkadir8/FET312_DeepPark_Proje.git
DeepPark

Model Uygulama ve Test Süreci (Abdulkadir Gedik)

Bu çal›ﬂmada, otopark doluluk tespiti probleminin temel baﬂar›m›n› (baseline) belirlemek amac›yla standart katmanlara sahip sade ve temel bir CNN modeli oluﬂturulmuﬂ ve test edilmiﬂtir. Uygulanan ad›mlar ﬂöyledir:

Veri Ön ‹ﬂleme: Veri seti ImageFolder yap›s› ile yüklenmiﬂ, tüm görüntüler 64x64 piksel boyutuna getirilmiﬂ ve veri seti rastgele olarak %80 E€itim (7199 görsel), %20 Test (1800 görsel) verisi ﬂeklinde ayr›lm›ﬂt›r.

Model Mimarisi: Modelde temel öznitelik ç›kar›m› için iki adet konvolüsyon katman› (Conv2d), do€rusal olmayan iliﬂkileri ö€renmek için standart ReLU aktivasyon fonksiyonu ve boyut azaltma için Max Pooling (2x2) katmanlar› kullan›lm›ﬂt›r.

E€itim Konfigürasyonu: Model, Adam optimizasyon algoritmas› (lr=0.001) ve s›n›fland›rma problemleri için uygun olan CrossEntropyLoss kay›p fonksiyonu ile derlenmiﬂtir.

Test: Model 3 epoch (dönem) boyunca e€itilmiﬂ, e€itim kayb› 0.0895 seviyesinden 0.0037 seviyesine kadar düﬂmüﬂ ve modelin daha önce hiç görmedi€i test seti üzerinde %99.94 nihai do€ruluk oran› elde edilmiﬂtir.