## 📖 Admin API Documentation 

[![My Skills](https://skillicons.dev/icons?i=python,fastapi,docker)](https://skillicons.dev) 

### 1. Login Endpoints 
<details>
<summary> 📌 POST /login/ </summary>

### Login Endpoint 
* User login page 

> Request body: 
```json
{
  "login": "fjuraev",
  "password": "Ewing0605"
}
```

> Response (200): 
```json
{
 "user_id": 233
 "user_name": "Firuz Juraev"
}
```
</details>
 
--- 

### 2. Dashboard Endpoints 
<details>
<summary> 📌 GET /general_statistics/ </summary>

### General Statistics Endpoint 

> Response (200): 
```json
{
 "n_active_users": 1230, 
 "n_active_businesses": 89, 
 "n_new_businesses": 3, 
 "n_posts": 125,
 "n_post_comments": 200,
 "n_business_comments": 56  
}
```
</details>


<details>
<summary> 📌 GET /business_categories/ </summary>

### Business Categories Endpoint 

> Response (200): 
```json
{
   "Visa & Law": 25,
   "Money Transfer": 12, 
}
```
</details>



<details>
<summary> 📌 GET /posts_categories/ </summary>

### Posts Categories Endpoint 

> Response (200): 
```json
{
   "Visa & Law": 63,
   "Money Transfer": 25, 
}
```
</details>



<details>
<summary> 📌 GET /posts_types/ </summary>

### Posts Types Endpoint 

> Response (200): 
```json
{
   "News": 100,
   "Articles": 25, 
}
```
</details>



<details>
<summary> 📌 GET /users_trend/ </summary>

### Users Trend Endpoint 

> Response (200): 
```json
{
   "August": 23,
   "July": 26,
   "June": 30,
   "May": 36,
   "April": 21,
   "March": 25, 
}
```
</details>



<details>
<summary> 📌 GET /businesses_trend/ </summary>

### Businesses Trend Endpoint 

> Response (200): 
```json
{
   "August": 23,
   "July": 26,
   "June": 30,
   "May": 36,
   "April": 21,
   "March": 25, 
}
```
</details>


--- 
### 3. Users Endpoints  

<details>
<summary> 📌 GET /users_list/ </summary>

### Users List Endpoint 

> Response (200): 
```json
{
   "1": {
          "user_id": 1,
          "user_name": Firuz Juraev,
          "user_status": True,
          "n_comments": 12  
        }, 
   "3": {
          "user_id": 3,
          "user_name": Umid  Juraev,
          "user_status": True,
          "n_comments": 12    
        } 
}
```
</details>


<details>
<summary> 📌 PUT /edit_user/ </summary>

### Edit User Endpoint 

> Request body: 
```json
{
  "user_id": 23,
  "status": False,
  "block": True,
  "role": 1   
}
```


> Response (200): 
```json
{
   "message": Successfully edited! 
}
```
</details>



<details>
<summary> 📌 DELETE /delete_user/ </summary>

### Delete User Endpoint 

> Request body: 
```json
{
  "user_id": 23
}
```


> Response (200): 
```json
{
   "message": Successfully deleted! 
}
```
</details>



<details>
<summary> 📌 POST /add_user/ </summary>

### Delete User Endpoint 

> Request body: 
```json
{
  "user_name": "Firuz Juraev",
  "user_email": "example@gmail.com",
  "user_role": 3, 
  "user_phone": "+821042989697",
  "user_location": "Uzbekistan",
  "user_login": "fjuraev",
  "user_password": "Ewing@0001"
}
```


> Response (200): 
```json
{
   "message": Successfully added! 
}
```
</details>


--- 
### 4. Categories Endpoints  

<details>
<summary> 📌 GET /categories_list/ </summary>

### Categories List Endpoint 

> Response (200): 
```json
{
   "1": {
          "id": 5,
          "category_name_en": "Halal Kitchen and Shop",
          "category_name_uz": "Halol oshxona va do‘kon",
          "description_en": "Offering freshly prepared halal meals and a variety of certified halal grocery products.",
          "description_uz": "Yangi tayyorlangan halol taomlar va sertifikatlangan halol oziq-ovqat mahsulotlari taklifi.",
          "comments_count": 0
  },
}
```
</details>



<details>
<summary> 📌 PUT /edit_category/ </summary>

### Edit Categoty Endpoint 

> Request body: 
```json
{
  "category_id": 1,
  "category_name_en": "Visas & Laws",
  "category_name_uz": "Vizalar & Qonunlar"
  "status": False   
}
```


> Response (200): 
```json
{
   "message": Successfully edited! 
}
```
</details> 



<details>
<summary> 📌 POST /add_category/ </summary>

### Edit User Endpoint 

> Request body: 
```json
{
  "category_name_en": "Visas & Laws",
  "category_name_uz": "Vizalar & Qonunlar", 
  "description_en": "blabla", 
  "description_uz": "blabla"   
}
```


> Response (200): 
```json
{
   "message": Successfully added! 
}
```
</details> 

<details>
<summary> 📌 DELETE /delete_category/ </summary>

### Delete Category Endpoint 

> Request body: 
```json
{
  "Category_id": 23
}
```


> Response (200): 
```json
{
   "message": Successfully deleted! 
}
```
</details>


--- 
### 5. Businesses Endpoints  

<details>
<summary> 📌 GET /businesses_list/ </summary>

### Businesses List Endpoint 

> Response (200): 
```json
{
    {
    "id": 3,
    "name": "B",
    "short_info_en": "Authentic Korean halal dishes made with care, offering home-style meals prepared by Gim Soensaeng. A taste of Korea with full halal compliance.",
    "short_info_uz": "Gim Soensaeng tomonidan tayyorlangan halol va uy uslubidagi koreys taomlari. Halollik talablariga to‘liq javob beruvchi Koreya ta’mi.",
    "category_name_en": null,
    "category_name_uz": null,
    "manager_name": "Kimsanboy",
    "Joined_date": "2025-08-05T08:05:20.244000"
  }
}
```
</details>
<details>
<summary> 📌 PUT /edit_businesses/ </summary>
### Edit Business Endpoint 

> Request body: 
```json

 {
  "business_id": 3,
  "name": "Plov",
  "short_info_en": "Authentic Korean halal dishes made with care, offering home-style meals prepared by Gim Soensaeng. A taste of Korea with full halal compliance.",
  "short_info_uz": "Gim Soensaeng tomonidan tayyorlangan halol va uy uslubidagi koreys taomlari. Halollik talablariga to‘liq javob beruvchi Koreya ta’mi.",
  "manager_id": 3,
  "category_id": 5
}

```


> Response (200): 
```json
{
   "message": Successfully edited! 
}
```
</details> 



<details>
<summary> 📌 POST /add_business/ </summary>

### Add Business Endpoint 

> Request body: 
```json
{
  "name": "Plov",
  "short_info_en": "Authentic Korean halal dishes made with care, offering home-style meals prepared by Gim Soensaeng. A taste of Korea with full halal compliance.",
  "short_info_uz": "Gim Soensaeng tomonidan tayyorlangan halol va uy uslubidagi koreys taomlari. Halollik talablariga to‘liq javob beruvchi Koreya ta’mi.",
  "full_info_en": "Experience the warmth of traditional Korean home cooking with a halal twist. At Gim Soensaeng’s Halal Korean Restaurant, we specialize in authentic, freshly prepared dishes that follow halal dietary standards while preserving the rich flavors of Korea.
Our meals are lovingly made using high-quality ingredients, carefully sourced to ensure both authenticity and halal compliance. From classic dishes like bibimbap, bulgogi, and kimchi stew to unique home-style specialties, each plate offers a genuine taste of Korean culture.
Whether you are a local, a traveler, or part of the Muslim community seeking delicious halal options, our restaurant welcomes everyone looking for wholesome, comforting Korean food.
Highlights:
100% halal-certified ingredients
Traditional Korean home-cooked recipes
Cozy, family-friendly atmosphere
Vegetarian options available
Friendly service with a personal touch
Come and enjoy the true essence of Korea — prepared with heart, served with respect.",
  "full_info_uz": "Halollik talablariga mos, an’anaviy koreys uy taomlarining iliqligini his eting. Gim Soensaeng’ning Halol Koreys Restorani sizga Koreya taomlarini asl ta’mi bilan, halol qoidalariga rioya qilgan holda taqdim etadi.
Taomlarimiz sevgi bilan, yuqori sifatli va halol ekanligiga ishonch hosil qilingan mahsulotlardan tayyorlanadi. Bibimbap, bulgogi, kimchi sho‘rva kabi klassik koreys taomlaridan tortib, noyob uy sharoitida tayyorlangan maxsus retseptlargacha — har bir taomda koreys madaniyatining haqiqiy ta’mini topasiz.
Agar siz mahalliy bo‘lsangiz, sayohatchi yoki halol ovqat izlayotgan musulmon bo‘lsangiz – barchangizni bu mazali va qulay muhitdagi restoranimizda kutib qolamiz.
Afzalliklarimiz:
100% halol sertifikatlangan mahsulotlar
An’anaviy koreys uy retseptlari
Iliq va oilaviy muhit
Vegetarianga mos variantlar mavjud
Samimiy va e’tiborli xizmat
Koreya taomlarining asl mohiyatini his eting — qalbdan tayyorlangan, hurmat bilan taqdim etiladi.",
  "location": "Республика Корея, Seoul, Yongsan District, Itaewon-dong, 34-19",
  "phone": "+82-2132-2246",
  "email": "koreada-halal4@gmail.com",
  "logo_link": "[string](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQuuDzgLmGrDbSADW1-t1MF-Rril9XWHOanhA&s)",
  "background_image_link": "[string](https://cdn.prod.website-files.com/5ec561ed25beadc20eb206da/5ede8343f7025523a6e9432e_header19_600x900.jpg)",
  "category_id": 5,
  "manager_id": 2
}
```


> Response (200): 
```json
{
   "message": Successfully added! 
}
```
</details> 

<details>
<summary> 📌 DELETE /delete_business/ </summary>

### Delete Business Endpoint 

> Request body: 
```json
{
  "business_id": 3
}
```


> Response (200): 
```json
{
   "message": Successfully deleted! 
}
```
</details>


--- 
### 6. Post Endpoints  

<details>
<summary> 📌 GET /posts_list/ </summary>

### Posts List Endpoint 

> Response (200): 
```json
{
   {
    "id": 7,
    "title_en": "Opening Your First Korean Bank Account",
    "title_uz": "Koreyada birinchi bank hisobingizni ochish",
    "content_uz": "Xorijiy rezident sifatida Koreyada bank hisobini ochish bo‘yicha bosqichma-bosqich qo‘llanma.",
    "content_en": "Step-by-step guide to opening a bank account in Korea as a foreign resident.",
    "author": "string",
    "post_date": "2025-08-19T11:48:43.264756",
    "post_type": "news"
  }
}
```
</details>
<details>
<summary> 📌 POST /add_post/ </summary>
### Add Post Endpoint 


> Request body: 
```json

 {
  "title_en": "A New Way to Explore Ethical Shopping",
  "title_uz": "Etik Savdo Bozori Tomon Yangi Qadam",
  "content_en": "The demand for halal products has grown rapidly in recent years. "Halal and Shop" is more than just a marketplace – it is a lifestyle choice. Shoppers today seek products that align with their values, including ethical sourcing, cleanliness, and religious compliance.
Halal-certified items include food, cosmetics, clothing, and even finance. This growing interest reflects not only religious needs but also a broader shift toward healthier and more transparent consumption. Many non-Muslim consumers also choose halal products for their quality and hygiene standards.
Online halal marketplaces are making it easier than ever to discover, review, and buy halal-certified products from anywhere in the world. With the power of digital tools, “Halal and Shop” connects customers to trustworthy brands and local producers. It’s not just about shopping – it’s about conscious living.",
  "content_uz": "So‘nggi yillarda halol mahsulotlarga bo‘lgan talab keskin oshdi. “Halol va Xarid” nafaqat bozor maydonchasi, balki turmush tarzini aks ettiruvchi konsepsiyadir. Bugungi xaridorlar o‘z e’tiqodlari va qadriyatlariga mos mahsulotlarni izlayapti – bu esa etik ishlab chiqarish, poklik va diniy talablar bilan uyg‘unlikda bo‘lgan mahsulotlarni anglatadi.
Halol sertifikatiga ega mahsulotlar faqat oziq-ovqat bilan cheklanmaydi – kosmetika, kiyim-kechak, hatto moliyaviy xizmatlar ham bu ro‘yxatga kiradi. Bu nafaqat diniy talablarni qondiradi, balki sog‘lom va shaffof iste’mol madaniyatiga bo‘lgan umumiy ehtiyojni ham ifodalaydi. Ko‘plab musulmon bo‘lmagan xaridorlar ham halol mahsulotlarni sifat va gigiyena mezonlari tufayli tanlaydilar.
Onlayn halol bozorlar orqali endi halol mahsulotlarni istalgan joydan topish, ularni solishtirish va xarid qilish osonlashdi. “Halol va Xarid” loyihasi ishonchli brendlar va mahalliy ishlab chiqaruvchilarni xaridorlar bilan bog‘lab beradi. Bu shunchaki xarid emas – bu ongli hayot tarzidir.",
  "author_id": 2,
  "post_type_id": 1,
  "category_id": 5,
  "post_header_image_link": "[string](https://hometownrealty.co.kr/wp-content/uploads/2023/11/bank-account.jpg)",
  "post_image_id": 1
}

```


> Response (200): 
```json
{
   "message": Successfully edited! 
}
```
</details>
<details>
<summary> 📌 PUT /edit_post/ </summary>
### Edit Post Endpoint 

> Request body: 
```json

 {
  "post_id": 3,
  "title_en": "A New Way to Explore Ethical Shopping",
  "title_uz": "Etik Savdo Bozori Tomon Yangi Qadam",
  "content_en": "The demand for halal products has grown rapidly in recent years. "Halal and Shop" is more than just a marketplace – it is a lifestyle choice. Shoppers today seek products that align with their values, including ethical sourcing, cleanliness, and religious compliance.
Halal-certified items include food, cosmetics, clothing, and even finance. This growing interest reflects not only religious needs but also a broader shift toward healthier and more transparent consumption. Many non-Muslim consumers also choose halal products for their quality and hygiene standards.
Online halal marketplaces are making it easier than ever to discover, review, and buy halal-certified products from anywhere in the world. With the power of digital tools, “Halal and Shop” connects customers to trustworthy brands and local producers. It’s not just about shopping – it’s about conscious living.",
  "content_uz": "So‘nggi yillarda halol mahsulotlarga bo‘lgan talab keskin oshdi. “Halol va Xarid” nafaqat bozor maydonchasi, balki turmush tarzini aks ettiruvchi konsepsiyadir. Bugungi xaridorlar o‘z e’tiqodlari va qadriyatlariga mos mahsulotlarni izlayapti – bu esa etik ishlab chiqarish, poklik va diniy talablar bilan uyg‘unlikda bo‘lgan mahsulotlarni anglatadi.
Halol sertifikatiga ega mahsulotlar faqat oziq-ovqat bilan cheklanmaydi – kosmetika, kiyim-kechak, hatto moliyaviy xizmatlar ham bu ro‘yxatga kiradi. Bu nafaqat diniy talablarni qondiradi, balki sog‘lom va shaffof iste’mol madaniyatiga bo‘lgan umumiy ehtiyojni ham ifodalaydi. Ko‘plab musulmon bo‘lmagan xaridorlar ham halol mahsulotlarni sifat va gigiyena mezonlari tufayli tanlaydilar.
Onlayn halol bozorlar orqali endi halol mahsulotlarni istalgan joydan topish, ularni solishtirish va xarid qilish osonlashdi. “Halol va Xarid” loyihasi ishonchli brendlar va mahalliy ishlab chiqaruvchilarni xaridorlar bilan bog‘lab beradi. Bu shunchaki xarid emas – bu ongli hayot tarzidir.",
  "author_id": 2,
  "post_type_id": 2,
  "category_id": 5,
  "post_header_image_link": "[string](https://www.korvia.com/wp-content/uploads/2017/03/Background-of-mobile-with-icons.png)",
  "post_image_id": 1
}

```

> Response (200): 
```json
{
   "message": Successfully edited! 
}
```
</details>

<details>
<summary> 📌 DELETE /delete_post/ </summary>
### Delete Post Endpoint 
  
> Request body: 
  
```json
{
  "post_id": 3
}
```


> Response (200): 
```json
{
   "message": Successfully deleted! 
}
```

</details> 
