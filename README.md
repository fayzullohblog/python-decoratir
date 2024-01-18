# Decoratir haqida

### 1) Decoratir nima, aslida  nima uchun kerak va undan qanday foydalanamiz kabi yechimlarga javob shu yerda !
 [GitHubga Follow bo'ling ](https://github.com/fayzullohblog)  

<p align="center">
<img alt="Types-of-OOPS-2" height="500" src="https://miro.medium.com/v2/resize:fit:1400/0*D8Nc0Dyu2iOUdNok" width="1000">
</p>


> [!NOTE]
Decoartir nima? Python dasturlash tilidagi funksiyalar orqali  boshqa funksiyalarga o'zgartirishlar kiritish uchun foydalaniladigan maxsus sintaksisdir(belgi). Decorator, biror funksiyani o'z ichiga oladi va unga qo'shimcha funksiyalarni qo'shish, o'zgartirish yoki funksiya ishlashni boshlaganini  va tugaganini tekshirish imkoniyatini beradi.

<p align="center">
<img alt="Types-of-OOPS-2" height="500" src="https://miro.medium.com/v2/resize:fit:1400/1*PCrgNdMFnOGF5FHhaLAwJg.png" width="1000">
</p>

***Etibor bering yuqoridagi rasimda bir g'isht, qandaydir decoratir nomli mashina(zavut) ichida o'tib boshqacha ko'rinishga ega bo'lib qoldi, xuddi shunday g'ishtni funksiya deb rasimda ko'rsatgan va unga qo'shimcha o'zgartirish keritish uchun decoratirdan foydalangan, qolgan tushunchani code yozish orqali tushunib olamiz***

### 2) main.py faylga birinchi , oddiy funskiya yozaman berilgan qiymatni bir soniga oshirib qo'yadi.

```sh
def add_number(number):
    return number+1

result=add_number(5)
result
```


#### Natija
```sh
6
```




### 3) yuqoridagi add_number()  funskiyasini boshqa funskiya ichiga yozib qo'yaman , ammo doimdi ishdi qiladi, yani berilgan qiymatga 1 sonini qo'shib quyadi.


```sh
def make(number):
    def add_number(number):
        return number+1

    add_one=add_number(number)
    return add_one

result=make(3)
result

```
***add_number() funksiyasi qiymantini, boshqa make() nomli fnskiya orqali olayabdi va natija......**

#### Natija
```sh
4
```

### 4) endi esa, bir funskiya parametriga boshqa funksiyani berib yuboramiz va qiladigan sihi esa, yuqoridagi 2 va 3 holatdagi bilan birxil bo'ladi.


```sh
def add_number(number):
    return number+1

def make(function):
    number=2

    return function(number)
result=make(add_number)
result

```
***Etibor bering ! bu decoratir mavzusini o'rganishlik uchun , oldin funksiyalar bilan ishlashni o'rganib chiqgan bo'lihs kerak bo'ladi***

#### Natija
```sh
3
```

> [!NOTE]
4-holatda, make() funskiyasi o'zining parametri sifatida add_number() funskiyasini qabul qildi, shu add_number() funksiyasining parametrini berishlik uchun esa make() funskiyasi ichida berib return ga qaytarib yubordek va natija esa birxil, ishlash yullar harxil


***`@abstractmethod` - bu decoratirni Abstract classning harqanday methodida foydalanishlik shart bo'ladi, 
sababi boshqa classlarda ya'ni subclasslarda aynan shu methodlar override qilinadi. Abstract classdagi methodalar nima uchun kerak, aynan subclasslarning interficelarini yaxshilash va codeni sodda ko'rinishga olib kelish uchun***



#### Vedio orqali ko'rish
[ ![My](https://user-images.githubusercontent.com/57800056/245666234-e0c3afd8-9ca1-44fd-8595-47ec0f6c4cfc.png) ](https://www.youtube.com/@webmaster_py)   

#### quyidagi social tarmoqlarda kuzating
[ ![My](https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white) ](https://github.com/fayzullohblog) [ ![My](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white) ](https://www.linkedin.com/in/fayzullohblog/)  [ ![My](https://img.shields.io/badge/Instagram-E4405F?style=for-the-badge&logo=instagram&logoColor=white) ](https://www.instagram.com/fayzullohblog/)   [ ![My](https://patrolavia.github.io/telegram-badge/chat.png) ](https://t.me/webmasterpy)  [ ![](https://patrolavia.github.io/telegram-badge/follow.png) ](https://t.me/suniy_intelekt_uzb) [ ![My](https://github.com/paulrobertlloyd/socialmediaicons/blob/main/facebook-48x48.png) ](https://www.facebook.com/fayzullohblog/)  [ ![My](https://github.com/paulrobertlloyd/socialmediaicons/blob/main/youtube-48x48.png) ](https://www.youtube.com/@webmaster_py) 


