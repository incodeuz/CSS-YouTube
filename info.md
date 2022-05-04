# **_Transitionlar_** haqida batafsil

[Youtube kanalga **Obuna** bo'ling](https://www.youtube.com/channel/UCB0Ryoxqhqu_h_FBEY233Xg)

<div style="display:flex; justify-content:space-between">inCode Product<span>k_abdullah</span></div>

<hr>

- ## Transition o'zi nima?

  Transition bu **"o'tish"** degan ma'noni bildirib malumotlarimizni holat **_(pseudo element yoki classlari bilan)_** belgilaganimizdan so'ng aytilgandek ko'rinishda **sekin** yoki **tez** o'zgarishini o'zgartirib beradigan hususiyat

      transition
      transition-delay
      transition-duration
      transition-property
      transition-timing-function

  - **transition** - tepadagi hamma malumotni birlashtirib bitta transition propertyga bir qatorda yozsa bo'ladi

  - **transition-delay** - effectni qancha kutib turishi

  - **transition-duration** - effect davomiyligi

  - **transition-property** - nima o'zgarishi, masalan width, agar ko'p style o'zgaradigan bo'lsa **all** deb yozamiz
  - **transition-timing-function** - bu, effectning ko'rinishi, ease, linear va boshqalari

## Example:

### **HTML - code**

    <body>
      <div class="item">Hello Coders!<div>
    </body>

### **CSS - code**

    body {
      width: 100%;
      height: 100%;
    }

    .item {
      background-color: red;
      width: 200px;
      height: 200px;
      transition: width 2s;
    }

    .item:hover {
      width: 400px;
    }

- ## Transitionni qanday ishlatamiz?

  - ### **_Qaysi elementimizga transition ishlatmoqchi bo'lsak o'shanga :_**

        transition: "nima o'zgarishi" 2s;

    berishimiz kerak, bu kodimizda **nima harakatga kirishi**, va **qancha muddat davom etishini** aytib o'tganmiz!

  - ### **_Harakatga keltirish uchun itemimizga style qo'shamiz_**

        .item:hover {
          width: 400px;
          background-color: red;
          border-radius: 50%;
        }

    endi bu holatimizda biz

         transition: "nima o'zgarishi" 2s;

    emas, balki bizga **ko'p elementlar** o'zgaryotganligi uchun **all** degan kalit so'zidan foydalanamiz!

          transition: all 2s;

- ## **_Transition o'tish turlari!_**
  - **linear** - effect _bir hil_ tezlikda o'zgaradi
  - **ease** - effect _sekin_ boshlanib _tez_ boladi, va _sekin_ tugaydi
  - **ease-in** - _effect_ sekin boshlanadi
  - **ease-in-out** - _effect_ sekin boshlanib _sekin_ tugaydi
  - **ease-out** - _effect_ sekin tugaydi
  - **cubic-bezier(x,y,z,k)** - ushbu function orqali ko'rsatilgan _egri chiziq effectiga_ ega boladi va _x,y,z,k_ o'rniga qiymat ko'rsatiladi!

bularni biz kodimizda shunday ko'rinishda ishlatamiz:

     transition: all 2s linear;

**yoki**

       transition: all;
       transition-duration: 2s;
       transition-timing-function: linear;

- ## Transtion Delay

  - bu effectni qancha **kechikishini belgilab** beradi, u o'ziga _sekund_ yoki _milisekund_ ko'rinishida qiymat qabul qiladi va u quyidagicha yoziladi

        transition-delay: 2s;
