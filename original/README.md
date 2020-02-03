
# ÇOKLU DİL DESTEĞİ OLAN STATİK HTML SAYFA HAZIRLAMA


## Hazırlamadan önce 

* static-i18n ve serve npm araçları kurulmuş olmalıdır.
  * ```npm i -g static-i18n```
  * ```npm i -g serve```


## Yeni çeviri ekleme

* landing/original sayfasındaki html dosyalarında istenilen HTML tag'ın içine **data-t** attribute eklenir. 
* **data-t** değeri olarak eklenen key değeri locales altındaki dil dosyalarına ilgili çeviri eklenir. 
* **data-t** key değeri çevirisi dosylarda bulunmaz ise tag içindeki default değer tüm diller için kullanılır, o yüzden her zaman default değer olması iyidir.

  * ```<title data-t="title">DEFAULT Title</title>```

## Çeviriler içeren statik sayfaların hazırlanması

* komut satırından /original dizinine gelip aşağıdaki komut çalıştırılırsa public klasörüne çevirisi yapılan **en** ve **tr** .html dosyaları oluşturulur

  * ```static-i18n -l en -i en -i tr -o ../ . ```

* **tr** çeviri tr klasörüne oluşturulmaktadır.


## Hazırlanan sayfaları göre

* komut satırından ana dizine gidip aşağıdaki komutu çalıştırarak http://localhost:5000 adresinde uygulamayı görebilirsin.

  * ```serve . ```