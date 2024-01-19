# Decoratir haqida

### 1) Decoratir nima, aslida  nima uchun kerak va undan qanday foydalanamiz kabi yechimlarga javob shu yerda !
 [GitHubga Follow bo'ling ](https://github.com/fayzullohblog)  

<p align="center">
<img alt="Types-of-OOPS-2" height="500" src="https://miro.medium.com/v2/resize:fit:1400/0*D8Nc0Dyu2iOUdNok" width="1000">
</p>

***Etibor bering ! bu decoratir mavzusini o'rganishlik uchun , oldin funksiyalar bilan ishlashni o'rganib chiqgan bo'lish kerak bo'ladi, ammo shu decoratir mavzusida ham murakkab funskiyalar hosil qilishga bir nechta misol yozib ketamiz chunki bu holatlarni bilish decoratir mavzusi uchun muxim***

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

### 4) endi esa, bir funskiya parametriga boshqa funksiyani berib yuboramiz va codemizning qiladigan asosiy ishi yuqoridagi 2 va 3 - holatlar bilan bir hil bo'ladi,lekin yullar turlicha.

```sh
def add_number(number):
    return number+1

def make(function):
    number=2

    return function(number)
result=make(add_number)
result

```

#### Natija
```sh
3
```

> [!NOTE]
4-holatda, make() funskiyasi o'zining parametri sifatida add_number() funskiyasini qabul qildi, shu add_number() funksiyasining parametrini berishlik uchun esa make() funskiyasi ichida number=2 yozib, return ga qaytarib yubordek va natija esa birxil, ishlash yullar harxil.



### 5) make() funksiyani chaqirganda name() funksiyani qaytarish.


```sh

def make():
    def name():
        return 'Fayzulloh'

    return name
result=make()
result

```


#### Natija
```sh
Fayzulloh
```

> [!NOTE]
funskiyaga qavis quyish quymaslik haqida.


### 6) Ichki funskiya, o'zi joylashgan tashqi funskiyasining parametri va o'zgaruvchilaridan foydalanish huquqiga ega.


```sh

def make(ism):
    def name():
        print(" name bu ichki funksiya,make funskiyaga nisbatan ")
        return ism

    name()
result=make("Fayzulloh")
result

```


#### Natija
```sh
Fayzulloh
```

> [!NOTE]
6-holatdagi tushuncha decoratir mavzusi uchun muhim tushuncha sanaladi, ya'ni yuqorida make() funskiyasining ichiga name() funksiyaini yozdek, ism parametri name() funskiyasida foydalanildi.

## Yuqoridagi o'rganib chiqgan holatlarimizni yaxshi tushungan bo'lsangiz, endi Decoratir yaratishni boshlaymiz.

### 8) Decoratir yaratish


```sh
def uppercase_decorator(function):
    def wrapper():
        func = function()
        make_uppercase = func.upper()
        return make_uppercase

    return wrapper

```


#### Natija
```sh
Fayzulloh
```

> [!NOTE]
6-holatdagi tushuncha decoratir mavzusi uchun muhim tushuncha sanaladi, ya'ni yuqorida make() funskiyasining ichiga name() funksiyaini yozdek, ism parametri name() funskiyasida foydalanildi.



***`@abstractmethod` - bu decoratirni Abstract classning harqanday methodida foydalanishlik shart bo'ladi, 
sababi boshqa classlarda ya'ni subclasslarda aynan shu methodlar override qilinadi. Abstract classdagi methodalar nima uchun kerak, aynan subclasslarning interficelarini yaxshilash va codeni sodda ko'rinishga olib kelish uchun***



#### Vedio orqali ko'rish
[ ![My](https://user-images.githubusercontent.com/57800056/245666234-e0c3afd8-9ca1-44fd-8595-47ec0f6c4cfc.png) ](https://www.youtube.com/@webmaster_py)   

#### quyidagi social tarmoqlarda kuzating
[ ![My](https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white) ](https://github.com/fayzullohblog) [ ![My](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white) ](https://www.linkedin.com/in/fayzullohblog/)  [ ![My](https://img.shields.io/badge/Instagram-E4405F?style=for-the-badge&logo=instagram&logoColor=white) ](https://www.instagram.com/fayzullohblog/)   [ ![My](https://patrolavia.github.io/telegram-badge/chat.png) ](https://t.me/webmasterpy)  [ ![](https://patrolavia.github.io/telegram-badge/follow.png) ](https://t.me/suniy_intelekt_uzb) [ ![My](https://github.com/paulrobertlloyd/socialmediaicons/blob/main/facebook-48x48.png) ](https://www.facebook.com/fayzullohblog/)  [ ![My](https://github.com/paulrobertlloyd/socialmediaicons/blob/main/youtube-48x48.png) ](https://www.youtube.com/@webmaster_py) 


