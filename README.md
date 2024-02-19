**Postman Nedir ? Ben neden buradayım ?**

Postman API istekleri oluşturmamızı ve bu istekleri test etmemizi sağlayar. Her API isteği bir HTTP methodunu kullanır. En çok kullanılan methodlar ise GET, POST, PATCH, PUT ve DELETE’dir.

En çok kullanılan metodlar hakkında kısa bir bilgi vererek daha sonra repoda yer alan postman collectiondaki requestler ve kullanılanlar hakkında bilgi vereceğim.


**GET Metodu**

"GET" request method'u, belirtilen URL'den veri almak için kullanılır. 
Genellikle bir web sayfası veya API üzerindeki verilere erişmek için kullanılır. 
"GET" request method'u, URL üzerinden parametrelerle birlikte veri talep etmek için kullanılır 
ve genellikle veri göndermez, sadece veri alır.


**POST Metodu**

"POST" metodu sunucuya yeni bir kaynak oluşturmak için kullanılır. POST isteği gönderildiğinde, sunucu yeni bir kaynak oluşturur ve bu kaynağın URI'sini yanıt olarak döndürür.

**DELETE Metodu**

"DELETE" metodu sunucu üzerinde belirtilen bir kaynağı silmek için kullanılır. Yani, delete metodu kullanılarak bir kaynağın sunucu tarafından kalıcı olarak silinmesi sağlanır.
RESTful API'lerde, delete metodu genellikle kaynakları silmek için kullanılır. Örneğin, bir kullanıcının hesabını silmek veya belirli bir kaydı veritabanından kaldırmak için delete metodu kullanılabilir.


**PATCH Metodu**

"PATCH" metodu, sunucu üzerinde mevcut bir kaynağın kısmi olarak güncellenmesi için kullanılır. Yani, kaynağın tamamını değiştirmek yerine sadece belirli alanlarının güncellenmesini sağlar.  
Patch metodunun kullanımı, kaynağın güncellenecek alanlarını ve bu alanların değerlerini içeren bir isteği sunucuya göndererek gerçekleştirilir.

**Get Metodu - status with baseUrL**
![image](https://github.com/ahmetvatansever/MyPostmanCollection/assets/24367205/76399083-a1b0-4941-89c4-946ab381fcc9)

Collectiona ait {{baseURL}} isminde bir setVariable tanımlandı. Bu variable değerleri collection seçildiğinde "Variables" sekmesinde görüntülenir.
Bu tanımladığımız variable collection içinde kullanılabilecek şekilde tanımlandı.

Postman workspace içerisinde ***birden fazla collectionda ortak kullanılacak ise*** bu durumda Environments tanımlanmalıdır.

**Get Metodu - tools category with params**
![image](https://github.com/ahmetvatansever/MyPostmanCollection/assets/24367205/c4cdcea0-7505-409b-81b1-9a6be0ee4a3d)

Request seçildiğinde açılan sekmelerden "Params" içerisine where koşulu gibi çalışan, servise parametre geçmeye yarayan bir kısım var. Burada category için bir örnek oluşturuldu.

Servisin zorunlu olarak beklediği bir parametre eksik gönderilirse 400-Bad Request hatası dönecektir.

* Anahtar/Değer çifti içerir.
* Adres içerisinde ? işaretinden sonra yer alır.
* Zorunlu veya isteğe bağlı olabilirler.

![image](https://github.com/ahmetvatansever/MyPostmanCollection/assets/24367205/b8caefc4-3af8-4f16-bbae-cdaa943c10c3)

**Get Metodu - request path variables**

Servis urlinde yer alan değişken değerler için path variable kullanılabilir.
:degiskenAdi şeklinde urle tanımlanır. Aşağıdaki iki adres birbirine eş değerdir. Toolid bilgisini değişken üzerinden takip etmemizi sağlar.  
https://simple-tool-rental-api.glitch.me/tools/4643 = https://simple-tool-rental-api.glitch.me/tools/:toolId

![image](https://github.com/ahmetvatansever/MyPostmanCollection/assets/24367205/e855482b-5107-4db6-bdf7-51cb72a89a6b)


**POST Metodu - post request with token-create order**

Random isim oluşturmak için randomFullName kullanıldı.
Random bilgiler oluşturmak için {{$... formatı kullanılır. 
Email, image url, fullname gibi bilgiler json içerisinde takip edilebilecek şekilde random oluşturulabilir.

![image](https://github.com/ahmetvatansever/MyPostmanCollection/assets/24367205/725c0c80-c381-4920-b7c4-ad1899754178)


