## Biz kimiz ?
Merhaba biz Adnan Menderes Üniversitesi Bilgisayar Mühendisliği Bölümünden 2020 yılı itibariyle mezun olmuş üç arkadaşız. Adlarımız sırasıyla Okan Çifti, Uğurcan Kök ve Filiz Gözet. Üçümüz de bölüme girdiğimizden beri Doğal Dil İşleme üzerine çalışmaktayız. Bu yüzden Türkiye Açık Kaynak Platformu'nun Türkçe Doğal Dil İşleme konusunda farkındalık oluşturmak amacıyla düzenlediği bu yarışmaya katılarak biz de çalışmalara katkı sağlamak istedik.


## Ne yaptık ?
Yarışma için verilen metne bağlı sorulan soruların cevaplandırılması konusu üzerinde çalıştık. Fakat bunu yapmadan önce ilk olarak hem kendimizin kullanabileceği hem de başka çalışmalarda da kullanabilecek bir veri seti hazırlamakla işe başladık. Konu bütünlüğünü sağlayabilmek için soru-cevaplarımızı Osmanlı Tarihi üzerine oluşturduk ve bu bağlamda toplam “” kadar soru çıkarttık.

|               | Başlık/Title  |  Paragraf/Context    | Question-Answer / Soru-Cevap |
| ------------- |---------------|----------------------|------------------------------|
|     Train     |               |                      |                              |
|     Test      |               |                      |                              |

Bir sonraki aşamada bu elde ettiğimiz soru ve cevap ikililerini BERT ve ELECTRA algoritmalarına vererek modelimizi eğittik.
BERT kelimeleri tek tek değerlendirmek yerine, önündeki ve arkasındaki kelimeler ya da benzer ve eş anlamlı kelimeler ile birlikte değerlendirme yapmaktadır. Bu da bize karmaşık soruların çok daha iyi anlaşılıp, çözümlenme olanğı sağlamaktadır. Bu iki algoritmayı kullanarak ve parametrelerini değiştirerek modelimizi en iyi şekilde eğitmeyi hedefledik.


### BERT
| Model/Hyperparameters | epoch | max_seq_length | per_gpu_eval_batch_size | per_gpu_train_batch_size |
|-----------------------|-------|----------------|-------------------------|--------------------------|
|    BERT, Uncased#1    |       |                |                         |                          |
|    BERT, Uncased#2    |       |                |                         |                          |
|    BERT, Cased        |       |                |                         |                          |



### ELECTRA
| Hyperparameters | epoch | max_seq_length | per_gpu_eval_batch_size | per_gpu_train_batch_size |
|-----------------|-------|----------------|-------------------------|--------------------------|
|     Uncased     |       |                |                         |                          |


### RESULTS
| Model/Score |   F1   |   Exact   | 
|----------------------|-----------|
|             |        |           |                                    



