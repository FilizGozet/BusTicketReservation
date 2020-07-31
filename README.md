## Biz kimiz ?
Merhaba biz Adnan Menderes Üniversitesi Bilgisayar Mühendisliği Bölümünden 2020 yılı itibariyle mezun olmuş üç arkadaşız. Adlarımız sırasıyla Okan Çifti, Uğurcan Kök ve Filiz Gözet. Üçümüz de bölüme girdiğimizden beri Doğal Dil İşleme üzerine çalışmaktayız. Bu yüzden Türkiye Açık Kaynak Platformu'nun Türkçe Doğal Dil İşleme konusunda farkındalık oluşturmak amacıyla düzenlediği bu yarışmaya katılarak biz de çalışmalara katkı sağlamak istedik.


## Ne yaptık ?
Yarışma için verilen metne bağlı sorulan soruların cevaplandırılması konusu üzerinde çalıştık. Fakat bunu yapmadan önce ilk olarak hem kendimizin kullanabileceği hem de başka çalışmalarda da kullanabilecek bir veri seti hazırlamakla işe başladık. Konu bütünlüğünü sağlayabilmek için soru-cevaplarımızı Osmanlı Tarihi üzerine oluşturduk ve bu bağlamda toplam “” kadar soru çıkarttık. Bu verileri modelimize verebileceğimiz en uygun hale getirerek JSON formatında tuttuk.

```json
{
    "title": "Boğazlar Sözleşmesi",
    "paragraphs": [{
            "qas": [{
                    "question": "Boğazlar Sözleşmesi ne zaman imzalandı ?",
                    "id": 308,
                    "answers": [{
                            "answer_start": 0,
                            "text": "13 Temmuz 1841 tarihinde"
                        }
                    ]
                }, {
                    "question": "Boğazlar Sözleşmesi nerede imzalandı ?",
                    "id": 309,
                    "answers": [{
                            "answer_start": 25,
                            "text": "Londra kentinde"
                        }
                    ]
                }
            ],
            "context": "13 Temmuz 1841 tarihinde Londra kentinde imzalanan bu sözleşme ile boğazların tarafsız hale gelmesi de amaçlandı. 1841 Boğazlar Sözleşmesi ile barış zamanında herhangi bir devlete ait olan savaş gemilerinin geçişine izin verilmemesi garanti edilmiş olacaktı. Yalnız boğazların sadece savaş döneminde bu tür bir kapalı durumda yer alması da sağlanacaktı. Osmanlı Devleti; herhangi bir savaş halinde yer alması halinde ise boğazları istediği biçimde kullanma hakkına sahip olacaktı. Osmanlı Devleti savaşa girdiği için boğazlar üzerindeki savaş gemilerinin geçişi üzerine tasarruf hakkını kullanmıştır. Müttefikleri Fransa ve İngiltere’nin geçişine izin vermiştir."
        }
    ]
}

```

## Veri Seti

|               |  Başlık/Title  |   Paragraf/Context   | Question-Answer / Soru-Cevap |
| ------------- |----------------|----------------------|------------------------------|
|     Train     |                |                      |                              |
|     Test      |                |                      |                              |

Bir sonraki aşamada bu elde ettiğimiz soru ve cevap ikililerini BERT ve ELECTRA algoritmalarına vererek modelimizi eğittik.
BERT kelimeleri tek tek değerlendirmek yerine, önündeki ve arkasındaki kelimeler ya da benzer ve eş anlamlı kelimeler ile birlikte değerlendirme yapmaktadır. Bu da bize karmaşık soruların çok daha iyi anlaşılıp, çözümlenme olanğı sağlamaktadır. Bu iki algoritmayı kullanarak ve parametrelerini değiştirerek modelimizi en iyi şekilde eğitmeyi hedefledik.

## Kullanılan Modeller
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


## Gereksinimler

## Referanslar
Çalışma esnasında kullandığımız kaynaklar aşağıda yer almaktadır.
- https://github.com/stefan-it/turkish-bert
- https://github.com/TQuad/turkish-nlp-qa-dataset
- https://rajpurkar.github.io/SQuAD-explorer/
- https://arxiv.org/abs/1806.03822
- https://arxiv.org/abs/1810.04805
- https://arxiv.org/abs/2003.10555
- https://huggingface.co/transformers/


![alt text](https://github.com/FilizGozet/BusTicketReservation/blob/master/image/kedi.png?raw=true)


