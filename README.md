Kodun tamamını 3 farklı hücreye ayrışmış şekilde içerir. İlk hücre klasörlere 
erişim sağlayıp gerekli ilk adım işlemlerini uygulayıp 1D vektör üretecek kodları içerir. Son hücre 
karar ağacını çizdirmek için özellikle ayrılmıştır. Ortadaki hücre ise istenilen algoritmaları ve 
sonuçlarını içerir.
İlk adım olarak elimdeki verileri istenilen boyuta indirgeyip (28x28) 1D vektöre çeviren ve normalize 
etmemi sağlayacak 2 adet fonksiyon tanımladım (resize_image ve min_max_normalization).
Verileri kendi gruplarına göre etiketleyip bir diziye aktardım ve “shuffle” fonksiyonuyla veri ve 
etiketleri karıştırdım.
5-Fold cross validation algoritması için “Sklearn kütüphanesindeki ‘Kfold’ “ fonksiyonunu kullanarak
bu algoritmayı birden fazla kez kullanacağım için bir değişkene atadım (kf).
KNN algoritması için uzaklık metriği olarak öklid ve manhattan formüllerini kullanacak ve bunu her k 
değeri (3-5-7) için yapacak bir döngü tanımladım.
Bu döngü içinde eğitim ve test verilerini tanımladığım değişken üzerinden (kf) oluşturdum ardından
eğitim, test ve performans metriklerini bir tabloya ekledim.
Decision tree için “Sklearn” kütüphanesindeki “DecisionTreeClassifier” fonksiyonunu kullanarak
Entropi ve GINI değeleri için ayrı ayrı hesaplayacak bir döngü oluşturdum. Bu döngü içinde yine 
tanımladığım Kfold fonksiyonu değişkeni olan kf üzerinden test ve eğitim listelerimi oluşturdum.Bu 
listelerin eğitim, test sürelerini ve performans metiriklerini aynı döngü içinde hesapladım.
Naive Bayes ve SVM için benzer eğitim test ve performans metriği hesaplayan bir döngü tanımadım 
bunu da bir listeye kaydettim. Bunları “GaussianNB ve SVC” fonkisyonlarıyla oluşturdum.Elimdeki
liste içinde bulunan verileri ekrana uygun şekilde bastırdım.
Karmaşıklık matrisi için tüm sınıflandırma modellerinin fonksiyonları ayrı ayrı en son manuel olarak 
girdim çünkü kod içerisindeki terminalde oldukça uzun bir karmaşıklık matrisi resmi olacaktı. Bunları 
ayrı ayrı çalıştırıp çıkan resimleri kaydettim.
Decision tree için jupyterde ayrı bir kod hücresi oluşturdum çünkü boyutlarını manuel olarak ideal 
şekilde denemek istedim ardından “DecisionTreeClassifier” fonksiyonu yardımıyla entropi değeri 
üzerinden “Pyplot” kullanarak eğittiğim modeller üzerinden çizdirdim
