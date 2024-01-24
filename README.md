#EN
The code is organized into three separate cells. The first cell handles accessing folders, applying necessary initial steps, and generating a 1D vector. The middle cell contains the chosen algorithms and their results. The final cell is specifically dedicated to drawing the decision tree.

As the first step, I defined two functions, "resize_image" and "min_max_normalization," to reduce the dimensions of the available data to the desired size (28x28) and convert them into a 1D vector while normalizing them. I labeled the data based on their groups and transferred them to an array, shuffling the data and labels using the "shuffle" function.

For the 5-fold cross-validation algorithm, I used the "Kfold" function from the Sklearn library and assigned it to a variable since I will use this algorithm multiple times. For the KNN algorithm, I implemented a loop to use both the Euclidean and Manhattan distance metrics for each k value (3-5-7). Within this loop, I defined variables for training and testing data using the Kfold variable, and then added training, testing, and performance metrics to a table.

For the decision tree, I utilized the "DecisionTreeClassifier" function from the Sklearn library and created a loop to calculate entropy and GINI values separately. In this loop, using the Kfold variable, I generated lists for training and testing. I also calculated training, testing times, and performance metrics within the same loop.

I did not create a similar loop for Naive Bayes and SVM but instead used a list to record training, testing, and performance metric data. I created these using the "GaussianNB" and "SVC" functions. I printed the data in the list to the screen in a suitable format.

For the confusion matrix, I manually entered the functions for all classification models separately at the end because the terminal output with the confusion matrix images would be quite extensive within the code. I ran these separately and saved the resulting images.

For the decision tree, I created a separate Jupyter code cell to manually test and find ideal dimensions. Then, using the "DecisionTreeClassifier" function and Pyplot, I visualized the trained models based on the entropy value.


#TR
İlk hücre, klasörlere erişim sağlayıp gerekli ilk adım işlemlerini uygulayarak 1D vektör üreten kodları içermektedir. Ortadaki hücre, istenilen algoritmaları ve sonuçlarını içermektedir. Son hücre ise karar ağacını çizdirmek için özellikle ayrılmıştır.

İlk adım olarak elimdeki verileri istenilen boyuta indirgeyip (28x28) 1D vektöre çeviren ve normalize etmemi sağlayacak iki adet fonksiyon tanımladım: resize_image ve min_max_normalization. Verileri kendi gruplarına göre etiketleyip bir diziye aktardım ve "shuffle" fonksiyonuyla veri ve etiketleri karıştırdım.

5-Fold cross-validation algoritması için "Sklearn" kütüphanesindeki 'Kfold' fonksiyonunu kullanarak bu algoritmayı birden fazla kez kullanacağım için bir değişkene atadım (kf). KNN algoritması için uzaklık metriği olarak öklid ve manhattan formüllerini kullanacak ve bunu her k değeri (3-5-7) için yapacak bir döngü tanımladım.

Bu döngü içinde eğitim ve test verilerini tanımladığım değişken üzerinden (kf) oluşturdum, ardından eğitim, test ve performans metriklerini bir tabloya ekledim. Decision tree için "Sklearn" kütüphanesindeki "DecisionTreeClassifier" fonksiyonunu kullanarak Entropi ve GINI değerleri için ayrı ayrı hesaplayacak bir döngü oluşturdum.

Bu döngü içinde yine tanımladığım Kfold fonksiyonu değişkeni olan kf üzerinden test ve eğitim listelerimi oluşturdum. Bu listelerin eğitim, test sürelerini ve performans metriklerini aynı döngü içinde hesapladım.

Naive Bayes ve SVM için benzer eğitim, test ve performans metriği hesaplayan bir döngü tanımladım ve bunları bir listeye kaydettim. Bunları "GaussianNB" ve "SVC" fonksiyonlarıyla oluşturdum. Elimdeki liste içinde bulunan verileri ekrana uygun şekilde bastırdım.

Karmaşıklık matrisi için tüm sınıflandırma modellerinin fonksiyonları ayrı ayrı en son manuel olarak girdim, çünkü kod içerisindeki terminalde oldukça uzun bir karmaşıklık matrisi resmi olacaktı. Bunları ayrı ayrı çalıştırıp çıkan resimleri kaydettim.

Decision tree için Jupyter'de ayrı bir kod hücresi oluşturdum, çünkü boyutlarını manuel olarak ideal şekilde denemek istedim. Ardından "DecisionTreeClassifier" fonksiyonu yardımıyla entropi değeri üzerinden "Pyplot" kullanarak eğittiğim modeller üzerinden çizdirdim.
