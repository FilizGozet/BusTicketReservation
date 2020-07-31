## Biz kimiz ?
Merhaba biz Adnan Menderes Üniversitesi Bilgisayar Mühendisliği Bölümünden 2020 yılı itibariyle mezun olmuş üç arkadaşız. Adlarımız sırasıyla Okan Çifti, Uğurcan Kök ve Filiz Gözet. Üçümüz de bölüme girdiğimizden beri Doğal Dil İşleme üzerine çalışmaktayız. Bu yüzden Türkiye Açık Kaynak Platformu'nun Türkçe Doğal Dil İşleme konusunda farkındalık oluşturmak amacıyla düzenlediği bu yarışmaya katılarak biz de çalışmalara katkı sağlamak istedik.


## Ne yaptık ?
Yarışma için verilen metne bağlı sorulan soruların cevaplandırılması konusu üzerinde çalıştık. Fakat bunu yapmadan önce ilk olarak hem kendimizin kullanabileceği hem de başka çalışmalarda da kullanabilecek bir veri seti hazırlamakla işe başladık. Konu bütünlüğünü sağlayabilmek için soru-cevaplarımızı Osmanlı Tarihi üzerine oluşturduk ve bu bağlamda toplam “” kadar soru çıkarttık.

```json
"title": "Fatih Sultan Mehmed (II. Mehmed)",
"paragraphs": [{
        "qas": [{
                "question": "II. Mehmed 'in bilinen adı nedir?",
                "id": 1600,
                "answers": [{
                        "answer_start": 26,
                        "text": "Fatih Sultan Mehmed"
                    }
                ]
            }, {
                "question": "Fatih Sultan Mehmed nasıl tanınırdı?",
                "id": 1609,
                "answers": [{
                        "answer_start": 1092,
                        "text": "Sultanü'l-Berreyn ve Hakanü'l-Bahreyn 'İki karanın ve iki denizin Hükümdarı' olarak"
                    }
                ]
            }
        ],
        "context": "II. Mehmed bilinen adıyla Fatih Sultan Mehmed; kısaca Fâtih; Avrupa'da tanınan adıyla: Grand Turco 'Büyük Türk' veya Turcarum Imperator 'Türk İmparatoru'; 30 Mart 1432 – 3 Mayıs 1481 Osmanlı İmparatorluğu'nun yedinci padişahı. Tarihî kaynaklarda ismi, Mehmed isimli diğer padişahlarınki gibi, Muhammed şeklinde geçer. İlk olarak 1444 - 1446 yılları arasında kısa bir dönem, daha sonra 1451'den 1481 yılında ölümüne kadar 30 yıl boyunca hüküm sürdü. II.Mehmed, 21 yaşında İstanbul'u fethederek 1000 yıllık Bizans İmparatorluğu'na son verdi ve bu olay birçok tarihçi tarafından Orta Çağ'ın sonu Yeni Çağ'ın başlangıcı olarak kabul edildi. Fetih'ten sonra Fethin Babası anlamına gelen Ebû'l - Feth, daha sonraki dönemlerde ise Çağ Açan Hükümdar ve Kayser-i Rûm yani Roma İmparatoru unvanları ile anıldı. Fatih, İslam peygamberi Muhammed'in Konstantiniyye elbet fetholunacaktır. Onu fethedecek komutan ne güzel komutan, onu fetheden ordu ne güzel ordudur. Hadisine nâil olduğu için günümüzde Türkiye ve İslam dünyasının geniş bir kesiminde Kahraman olarak kabul edilmektedir. Fatih Sultan Mehmed Sultanü'l-Berreyn ve Hakanü'l-Bahreyn 'İki karanın ve iki denizin Hükümdarı' olarak tanınırdı."
}
```



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
|-------------|--------|-----------|
|             |        |           |                                    



