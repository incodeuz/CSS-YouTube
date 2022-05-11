# Animations 2-dars

## Dars rejasi:

- ### **animation-direction**
- ### **animation-timing-function**
- ### **animation-fill-mode**
- ### **animation-play-state**
- ### **animation**

---

## 💡 **animation-direction** : Animatsiya yo‘nalishi xususiyati _oldinga_, _orqaga_ yoki _ikkala_ ko'rinishdaham yurishi kerakligini belgilaydi.

<br>

### **❗Qiymatlari:**

| Qiymat            | Vazifasi                                                  | Default                 |
| ----------------- | --------------------------------------------------------- | ----------------------- |
| normal            | _Default_. Animatsiya odatdagidek ijro etiladi (oldinga)  | <input type="checkbox"> |
| revesre           | Animatsiya teskari yo'nalishda o'ynaladi (orqaga)         | <input type="checkbox"> |
| alternate         | Animatsiya avval oldinga, keyin esa orqaga o'ynaladi      | <input type="checkbox"> |
| alternate-reverse | Animatsiya avval orqaga, keyin oldinga qarab ijro etiladi | <input type="checkbox"> |

<br>

### **✅Ko'rinishi :**

```CSS
.selector-name {
    animation-direction: alternate;
}
```

### **🟢Misollar :**

```CSS
.box {
    width: 200px;
    height: 200px;
    background: red;
    animation-name: box-hover 2s infinite 2s;
    /* animation-direction: alternate; */
}

---- ---- ---- ----

@keyframes box-hover{
    from{
        width: 300px;
        background: blue;
    }
    to{
        width:500px;
        background:black
    }
}
```

```HTML
<div class="box">Animation direction</div>
```

<br>
<hr>
<br>

## **💡animation-timing-function** : animatsiyaning tezlik egri chizig'ini belgilaydi. Tezlik egri chizig'i CSSda animatsiya uslublarining bir styledan boshqasiga o'tishni belgilaydi. Tezlik egri chizig'i o'zgarishlarni oson, muammosiz bajarish uchun ishlatiladi.

<br>

### **❗Qiymatlari:**

| Qiymat         | Vazifasi                                                                                             | Default                 |
| -------------- | ---------------------------------------------------------------------------------------------------- | ----------------------- |
| linear         | Animatsiyamiz davomida bir hil ko'rinishda bo'ladi                                                   | <input type="checkbox"> |
| ease           | _Default_. Sekin boshlanadi, tezlashib, yana sekin tugaydi                                           | <input type="checkbox"> |
| ease-in        | Animatsiyamiz sekin boshlanadi                                                                       | <input type="checkbox"> |
| ease-in-out    | Animatsiyamiz sekin tugaydi                                                                          | <input type="checkbox"> |
| cubic-bezier() | O'zingiz qiymatlaringizni aniqlang. Mumkin qiymatlar 0 dan 1 gacha bo'lgan sonlar oralig'ida boladi. | <input type="checkbox"> |

<br>

### **✅Ko'rinishi :**

```CSS
.selector-name {
    animation-timing-function: ease-in-out;
}
```

### **🟢Misollar :**

```CSS
.box {
    width: 200px;
    height: 200px;
    background: red;
    animation-name: box-hover 2s infinite 2s;
    animation-direction: alternate;
    /* animation-timing-function: ease-in-out; */
}

---- ---- ---- ----

@keyframes box-hover{
    from{
        width: 300px;
        background: blue;
    }
    to{
        width:500px;
        background:black
    }
}
```

```HTML
<div class="box">Animation timing function</div>
```

<br>
<hr>
<br>

## **💡animation-fill-mode** : animatsiyamiz boshlanishidan oldin yoki tugagandan so'ng oldingi ko'rinishiga qaytib qoladi, ushbu xossa orqali bu holatni o'zgartirish mumkin.

<br>

### **❗Qiymatlari:**

| Qiymat    | Vazifasi                                                                                           | Default                 |
| --------- | -------------------------------------------------------------------------------------------------- | ----------------------- |
| none      | _Default_. Animatsiya tugagandan so'ng _oldingi_ holatida turadi.                                  | <input type="checkbox"> |
| forwards  | Animatsiyamiz **oxirgi** @keyframe interval qiymatiga ega bo'ladi                                  | <input type="checkbox"> |
| backwards | Animatsiyamiz **birinchi** @keyframe interval qiymatiga ega bo'ladi                                | <input type="checkbox"> |
| both      | element animatsiyaning birinchi va oxirgi @keyframe intervalida berilgan qiymatlarga teng bo'ladi. | <input type="checkbox"> |

### **✅Ko'rinishi :**

```CSS
.selector-name {
    animation-fill-mode: both;
}
```

### **🟢Misollar :**

```CSS
.box {
    width: 200px;
    height: 200px;
    background: red;
    color: white;
    animation: box-hover 2s infinite 2s;
    animation-direction: alternate;
    animation-timing-function: ease-in-out;
    /* animation-fill-mode: both; */
}

---- ---- ---- ----

@keyframes box-hover{
    from{
        width: 300px;
        background: blue;
    }
    to{
        width:500px;
        background:black
    }
}
```

```HTML
<div class="box">Animation fill mode</div>
```

 <br>
 <hr>
 <br>

## 💡 **animation-play-state** : animatsiyamiz qaysi holatda ekanini belgilab beradi. Odatda holat (pseudo) qoshilganda ishlaydi

### **❗Qiymatlari:**

| Qiymat  | Vazifasi                             | Default                 |
| ------- | ------------------------------------ | ----------------------- |
| running | animatsiyamiz davaom etayotgan holat | <input type="checkbox"> |
| paused  | animatsiyamiz to'xtatilgan holati    | <input type="checkbox"> |

### **🟢Misollar :**

```CSS
.box {
    width: 200px;
    height: 200px;
    background: red;
    color: white;
    animation: box-hover 2s infinite 2s;
    animation-direction: alternate;
    animation-timing-function: ease-in-out;
    animation-fill-mode: both;
}
.box:hover {
    /* animation-play-state: paused; */
}

---- ---- ---- ----

@keyframes box-hover{
    from{
        width: 300px;
        background: blue;
    }
    to{
        width:500px;
        background:black
    }
}
```

```HTML
<div class="box">Animation play state</div>
```

## 💡 **animation** - hozirgacha animatsiyada yozgan kodlarimizni bir qatorda yozishimiz mumkin

```CSS
.box {
    width: 200px;
    height: 200px;
    background: red;
    color: white;
    animation-name: box-hover;
    animation-duration:2s;
    animation-iteration-count:infinite;
    animation-delay:2s;
    animation-direction: alternate;
    animation-timing-function: ease-in-out;
    animation-fill-mode: both;
}
.box:hover {
    /* animation-play-state: paused; */
}
```

**yoki**

```CSS
.box{
    width: 200px;
    height: 200px;
    background: red;
    color: white;
    animation: box-hover 2s infinite 2s alternate linear both
}
.box:hover {
    /* animation-play-state: paused; */
}
```
