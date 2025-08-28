### 📖 API Documentation 

[![My Skills](https://skillicons.dev/icons?i=python,fastapi,docker)](https://skillicons.dev) 




<details>
<summary>⚡ Status Codes</summary> 

| Code | Meaning                  | Usage Example |
|------|--------------------------|---------------|
| 200  | **OK**                   | Successful GET, PUT, or POST request |
| 201  | **Created**              | Resource successfully created (e.g., after POST) |
| 202  | **Accepted**             | Request accepted for processing but not completed yet |
| 204  | **No Content**           | Request succeeded but no content to return (e.g., after DELETE) |
| 400  | **Bad Request**          | Invalid request payload or missing parameters |
| 401  | **Unauthorized**         | Missing or invalid authentication credentials |
| 403  | **Forbidden**            | Authenticated but not allowed to access the resource |
| 404  | **Not Found**            | Requested resource does not exist |
| 409  | **Conflict**             | Resource conflict (e.g., duplicate data) |
| 422  | **Unprocessable Entity** | Validation error in request data |
| 500  | **Internal Server Error**| Generic server-side error |
| 503  | **Service Unavailable**  | Server temporarily down or overloaded |
</details> 

### 1. Login & Sign up Endpoints 
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




<details>
<summary> 📌 POST /sign_up/ </summary> 
  
### Sign up Endpoint   
* User sign up
  
> Request body: 
```json
{
  "name": "umidjon",
  "role_id": 0,
  "login": "umid",
  "password": "umid0210",
  "phone": "998933313348",
  "email": "user@example.com",
  "country": "Uzbekistan"
}
```

> Response (200): 
```json
{
 "message": "Successfully registered" 
}
```
</details>


<details>
<summary> 📌 POST /forget_password/ </summary> 

### Forget Password Endpoint  
* User forgot password

> Request body: 
```json
{
  ""
  "email": "example@gmail.com",
}
```

> Response (200): 
```json
{
 "message": "Email found & and sent" 
}
```
</details>

--- 


### 2. Main Page API Endpoints

<details>
<summary>📌 GET /main_statistics/</summary>
  
### Main Statistics Endpoint 
* Returns general statistics about the website: number of registered users, number of categories, number of registered businesses, etc. 

> Response (200): 
```json
{
  "n_users": 1250,
  "n_categories": 6,
  "n_businesses": 60,
  "n_articles": 20,
  "n_news": 45
}
```
</details>


<details>
<summary> 📌 GET /main_categories/ </summary>

### Categories Endpoint 
* Returns categories with some information: visa, restaurants, money transfers, etc. 

> Response (200): 
```json
{
  "1": {
    "name_en": "SIM card and phone",
    "name_uz": "Sim karta va telefon",
    "description_en": "Providing SIM cards, mobile phones, and top-up services for local and international use.",
    "description_uz": "Mahalliy va xalqaro foydalanish uchun SIM kartalar, mobil telefonlar va balans to‘ldirish xizmatlari",
    "icon": "<svg xmlns=\"http://www.w3.org/2000/svg\" height=\"24px\" viewBox=\"0 -960 960 960\" width=\"24px\" fill=\"#1f1f1f\"><path d=\"M280-200h80v-80h-80v80Zm0-160h80v-160h-80v160Zm160 160h80v-160h-80v160Zm0-240h80v-80h-80v80Zm160 240h80v-80h-80v80Zm0-160h80v-160h-80v160ZM240-80q-33 0-56.5-23.5T160-160v-480l240-240h320q33 0 56.5 23.5T800-800v640q0 33-23.5 56.5T720-80H240Zm0-80h480v-640H434L240-606v446Zm0 0h480-480Z\"/></svg>",
    "posts_count": 2,
    "businesses_count": 2
  },
}
```
</details>


<details>
<summary> 📌 GET /latest_news/ </summary>

### Latest News Endpoint 
* Returns the latest posted news 

> Response (200): 
```json
{
  "1": {  "news_id": 23
          "news_title_en": "The rules for getting E-7 have changed",
          "news_title_uz": "E-7 olish qoidalari o'zgardi",
          "news_image_link": "https:sffgsfggsgdsgssg",
       }
}
```
</details>


<details>
<summary> 📌 GET /latest_articles/ </summary>

### Latest Articles Endpoint 
* Returns the latest posted articles 

> Response (200): 
```json
{
  "1": {  "article_id": 24
          "article_title_en": "How to open a bank account in Korea",
          "article_title_uz": "Qanday qilib bank hisob raqam ochish",
          "article_image_link": "https:sffgsfggsgdsgssg",
       }
}
```
</details>


<details>
<summary> 📌 GET /featured_businesses/ </summary>

### Latest Businesses Endpoint 
* Returns the latest posted businesses 

> Response (200): 
```json
{
  "1": {  "name": "B",
          "short_info_en": "Professional immigration legal services for foreign nationals",
          "short_info_uz": "Chet ellik fuqarolar uchun professional immigratsiya-huquqiy xizmatlar",
          "logo_link": "https://globallawexperts.com/wp-content/uploads/2023/07/8004_OpenVisaKorea_firm_logo.jpg"
       }
}
```
</details>

--- 


### 3. All Categories Page Endpoints 

<details>
<summary> 📌 GET /all_categories/ </summary>

### Categories Endpoint 
* Returns all categories with some information: visa, restaurants, money transfers, etc. 

> Response (200): 
```json
{
  "1": {  "category_name_en": "SIM card and phone",
          "category_name_uz": "Sim karta va telefon",
          "description_en": "Providing SIM cards, mobile phones, and top-up services for local and international use.",
          "description_uz": "Mahalliy va xalqaro foydalanish uchun SIM kartalar, mobil telefonlar va balans to‘ldirish xizmatlari",
          "icon": "<svg xmlns=\"http://www.w3.org/2000/svg\" height=\"24px\" viewBox=\"0 -960 960 960\" width=\"24px\" fill=\"#1f1f1f\"><path d=\"M280-200h80v-80h-80v80Zm0-160h80v-160h-80v160Zm160 160h80v-160h-80v160Zm0-240h80v-80h-80v80Zm160 240h80v-80h-80v80Zm0-160h80v-160h-80v160ZM240-80q-33 0-56.5-23.5T160-160v-480l240-240h320q33 0 56.5 23.5T800-800v640q0 33-23.5 56.5T720-80H240Zm0-80h480v-640H434L240-606v446Zm0 0h480-480Z\"/></svg>",
          "businesses_count": 2,
          "post_count": 2
       }
}
```
</details>


--- 

### 4. Categories Page Endpoints 
<details>
<summary> 📌 POST /category_businesses/ </summary>

### Category Businesses Endpoint 
* Returns the list of registered businesses

> Request body: 
```json
{
  "category_id": 1 
}
```

> Response (200): 
```json
{
  "1": {  "business_id": 12
          "name": "How to open a bank account in Korea",
          "short_info_en": "Qanday qilib bank hisob raqam ochish",
          "short_info_uz": "Qanday qilib bank hisob raqam ochish",
          "phone": "998933313348"
          "email": "example@gmail.com"
          "location": "101 Daehak-ro, Jongno-gu, Seoul"
          "logo_link": "https://ahfkjasfjafgkls"
       }
}
```
</details>



<details>
<summary> 📌 POST /category_articles/ </summary> 
  
### Category Articles Endpoint 
* Returns the list of articles related to the selected category 

> Request body: 
```json
{
  "category_id": 1 
}
```

> Response (200): 
```json
{
  "1": {  "article_id": 12
          "article_title_en": "Understanding Korean Health Insurance System",
          "article_title_uz": "Qanday qilib bank hisob raqam ochish",
          "article_image_link": "Qanday qilib bank hisob raqam ochish",
          "article_user": "Umidjon Juraqulov",
          "article_tags": "{maqola, Sog'liq}"
       }
}
```
</details>


<details>
<summary> 📌 POST /category_news/ </summary> 
  
### Category News Endpoint 
* Returns the list of news related to the selected category 

> Request body: 
```json
{
  "category_id": 1 
}
```

> Response (200): 
```json
{
  "1": {  "news_id": 12
          "news_title_en": "Understanding Korean Health Insurance System",
          "news_title_uz": "Qanday qilib bank hisob raqam ochish",
          "news_image_link": "Qanday qilib bank hisob raqam ochish",
          "news_user": "Umidjon Juraqulov",
          "news_tags": "{maqola, Sog'liq}" 
       }
}
```
</details>

--- 


### 5. Business Page Endpoints 
<details>
<summary> 📌 POST /business_details/ </summary>

### Businesses Details Endpoint 
* Returns business's details 

> Request body: 
```json
{
  "business_id": 1 
}
```

> Response (200): 
```json
{
   "business_id": 12
   "business_name": "Professional immigration legal services for foreign nationals",
   "business_short_info_en": "Professional immigration legal services for foreign nationals",
   "business_short_info_uz": "Chet ellik fuqarolar uchun professional immigratsiya-huquqiy xizmatlar",
   "business_phone": "998933313348"
   "business_email": "koreada-viza4@gmail.com"
   "business_location": "101 Daehak-ro, Jongno-gu, Seoul"
   "business_full_description_en": "Our firm provides comprehensive immigration legal services tailored to the unique needs of foreign nationals. We assist individuals, families, and businesses in navigating complex immigration laws with professionalism, precision, and care. From visa applications and permanent residency to work permits, citizenship, and legal representation, we ensure every step of the process is handled efficiently. With in-depth knowledge of immigration regulations and a client-focused approach, we are committed to protecting your rights and achieving the best possible outcome. Whether you are relocating for work, education, investment, or family reunification, our expert team offers personalized strategies and reliable guidance to make your transition seamless."
   "business_full_description_uz": "Biz jismoniy shaxslar, oilalar va biznes vakillariga murakkab immigratsiya qonunlarini yengib o‘tishda professional, aniq va g‘amxo‘rlik bilan yordam beramiz. Viza arizalaridan boshlab doimiy yashash huquqi, ish ruxsatnomalari, fuqarolik olish va huquqiy vakillikka qadar bo‘lgan barcha jarayonlarni samarali amalga oshirishni ta’minlaymiz. Immigratsiya qonunlari bo‘yicha chuqur bilim va mijozlarga yo‘naltirilgan yondashuv orqali biz sizning huquqlaringizni himoya qilish va eng yaxshi natijaga erishishga intilamiz. Ish, ta’lim, investitsiya yoki oila birlashuvi maqsadida ko‘chib o‘tayotgan bo‘lsangiz, bizning mutaxassislar jamoamiz sizning ehtiyojlaringizga moslashtirilgan strategiyalar va ishonchli yo‘l-yo‘riqlar bilan o‘tishingizni silliq va oson qiladi."
   "business_logo_link": "https://globallawexperts.com/wp-content/uploads/2023/07/8004_OpenVisaKorea_firm_logo.jpg"
   "business_background_image_link": "https://globallawexperts.com/wp-content/uploads/2023/07/8004_OpenVisaKorea_firm_logo.jpg"
   "business_services": ["visa xizmatlari", "trajima"] 
}
```
</details>



<details>
<summary> 📌 POST /business_comments/ </summary>

### Businesses Comments Endpoint 
* Returns business's comments  

> Request body: 
```json
{
  "business_id": 1 
}
```

> Response (200): 
```json
{
  "1": {  "comment_id": 12
          "comment_author_name": "Firuz Juraev",
          "comment_rating": 4.5, 
          "comment_date": "2025-08-12",
          "comment_content": "Norm company"
       }
}
```
</details>



<details>
<summary> 📌 POST /business_comment_upload/ </summary>

### Business Comment Upload Endpoint 
* Uploads a new comment for the business 

> Request body: 
```json
{
  "comment_upload_business_id": 1,
  "comment_upload_user_id": 23,
  "comment_upload_rating": 4,
  "comment_upload_content": "Telefonga javob bermas ekan" 
}
```

> Response (200): 
```json
{
   message: "Successfully uploaded!"
}
```
</details>

--- 


### 6. News Page Endpoints 
<details>
<summary> 📌 POST /news_details/ </summary>

### Businesses Details Endpoint 
* Returns business's details 

> Request body: 
```json
{
  "news_id": 1 
}
```

> Response (200): 
```json
{

  "news_id": 9,
  "news_title_en": "Discovering Halal Kitchens in Korea",
  "news_title_uz": "Discovering Halal Kitchens in Korea",
  "news_content_en": "A guide to finding authentic halal restaurants and eateries for Muslim residents and travelers",
  "news_content_uz": "Musulmon rezidentlar va sayohatchilar uchun haqiqiy halal restoran va oshxonalarni topish bo‘yicha qo‘llanma.",
  "news_author": "Kimsanboy",
  "news_date": "2025-08-19 11:59:38",
  "news_header_image_link": null,
  "news_views": 0,
  "news_tags": [],
  "news_images": []
}
```
</details>


<details>
<summary> 📌 POST /post_comments/ </summary>

### Post  Details Endpoint 
* Returns business's details 

> Request body: 
```json
{
  "post_id": 1 
}
```

> Response (200): 
```json
{
  "1": {  "comment_id": 12
          "comment_author_name": "Firuz Juraev",
          "comment_rating": 4.5, 
          "comment_date": "2025-08-12",
          "comment_content": "Norm news"
       }
}
```
</details>


<details>
<summary> 📌 POST /post_comment_upload/ </summary>

### Post Comment Upload Endpoint 
* Uploads a new comment for the post  

> Request body: 
```json
{
  "comment_upload_business_id": 1,
  "comment_upload_user_id": 23,
  "comment_upload_rating": 4,
  "comment_upload_content": "Telefonga javob bermas ekan" 
}
```

> Response (200): 
```json
{
   message: "Successfully uploaded!"
}
```
</details>

--- 



### 7. Article Page Endpoints 
<details>
<summary> 📌 POST /article_details/ </summary>

### Article Details Endpoint 
* Returns article's details 

> Request body: 
```json
{
  "article_id": 1 
}
```

> Response (200): 
```json
{
   "article_id": 12,
    "article_title_en": "A New Way to Explore Ethical Shopping",
    "article_title_uz": "Etik Savdo Bozori Tomon Yangi Qadam",
    "article_content_en": "The demand for halal products has grown rapidly in recent years. \"Halal and Shop\" is more than just a marketplace – it is a lifestyle choice. Shoppers today seek products that align with their values, including ethical sourcing, cleanliness, and religious compliance.\r\n\r\nHalal-certified items include food, cosmetics, clothing, and even finance. This growing interest reflects not only religious needs but also a broader shift toward healthier and more transparent consumption. Many non-Muslim consumers also choose halal products for their quality and hygiene standards.\r\n\r\nOnline halal marketplaces are making it easier than ever to discover, review, and buy halal-certified products from anywhere in the world. With the power of digital tools, “Halal and Shop” connects customers to trustworthy brands and local producers. It’s not just about shopping – it’s about conscious living.",
    "content_uz": "So‘nggi yillarda halol mahsulotlarga bo‘lgan talab keskin oshdi. “Halol va Xarid” nafaqat bozor maydonchasi, balki turmush tarzini aks ettiruvchi konsepsiyadir. Bugungi xaridorlar o‘z e’tiqodlari va qadriyatlariga mos mahsulotlarni izlayapti – bu esa etik ishlab chiqarish, poklik va diniy talablar bilan uyg‘unlikda bo‘lgan mahsulotlarni anglatadi.\r\n\r\nHalol sertifikatiga ega mahsulotlar faqat oziq-ovqat bilan cheklanmaydi – kosmetika, kiyim-kechak, hatto moliyaviy xizmatlar ham bu ro‘yxatga kiradi. Bu nafaqat diniy talablarni qondiradi, balki sog‘lom va shaffof iste’mol madaniyatiga bo‘lgan umumiy ehtiyojni ham ifodalaydi. Ko‘plab musulmon bo‘lmagan xaridorlar ham halol mahsulotlarni sifat va gigiyena mezonlari tufayli tanlaydilar.\r\n\r\nOnlayn halol bozorlar orqali endi halol mahsulotlarni istalgan joydan topish, ularni solishtirish va xarid qilish osonlashdi. “Halol va Xarid” loyihasi ishonchli brendlar va mahalliy ishlab chiqaruvchilarni xaridorlar bilan bog‘lab beradi. Bu shunchaki xarid emas – bu ongli hayot tarzidir.",
   
    "article_created_at": "2025-08-05 00:00:00",
    "article_tags":" [
      "halal food",
      "halal restaurants"
    ]"
   "article_aothor": "umidjon juraqulov"
   "article_header_image_link": "https://fajhgajhgajgnjg.jpg"
   "article_views": 16
   "article_images: [image1, image2]
}
```
</details>

--- 


### 8. All News Page Endpoints 

<details>
<summary> 📌 GET /all_news/ </summary>

### All News Endpoint 
* Returns all news with some information 

> Response (200): 
```json
{
  "1": {
          "news_id": 12
          "news_title_en": "Understanding Korean Health Insurance System",
          "news_title_uz": "Qanday qilib bank hisob raqam ochish",
          "news_image_link": "Qanday qilib bank hisob raqam ochish",
          "news_user": "Umidjon Juraqulov",
          "news_tags": {maqola, Sog'liq} 
       }
}
```
</details>


---  


### 9. All Articles Page Endpoints 

<details>
<summary> 📌 GET /all_articles/ </summary>

### All Articles Endpoint 
* Returns all articles with some information

> Response (200): 
```json
{
  "1": {  "article_id": 12
          "article_title_en": "Understanding Korean Health Insurance System",
          "article_title_uz": "Qanday qilib bank hisob raqam ochish",
          "article_image_link": "Qanday qilib bank hisob raqam ochish",
          "article_user": "Umidjon Juraqulov",
          "article_tags": {maqola, Sog'liq}
       }
}
```
</details>


--- 



### 10. Main Search Page Endpoints 

<details>
<summary> 📌 POST /search_businesses/ </summary>

> Request body: 
```json
{
  "search_text": "E-7 visa" 
}
```

### Search Businesses Endpoint 
* Returns all articles with some information

> Response (200): 
```json
{
  "1": {  "business_id": 12
          "business_name": "How to open a bank account in Korea",
          "business_short_info_en": "Qanday qilib bank hisob raqam ochish",
          "business_short_info_uz": "Qanday qilib bank hisob raqam ochish",
       }
}
```
</details>



<details>
<summary> 📌 POST /search_news/ </summary>

### Search News Endpoint 
* Returns all articles with some information

> Request body: 
```json
{
  "search_text": "E-7 visa" 
}
```

> Response (200): 
```json
{
  "1": { "news_id": 12
          "news_title_en": "Understanding Korean Health Insurance System",
          "news_title_uz": "Qanday qilib bank hisob raqam ochish",
          "news_image_link": "Qanday qilib bank hisob raqam ochish",
          "news_user": "Umidjon Juraqulov",
          "news_tags": "{maqola, Sog'liq}" 
       }
}
```
</details>



<details>
<summary> 📌 POST /search_articles/ </summary>

### Search Articles Endpoint 
* Returns all articles with some information

> Request body: 
```json
{
  "search_text": "E-7 visa" 
}
```

> Response (200): 
```json
{
  "1": {  "article_id": 12
          "article_title_en": "Understanding Korean Health Insurance System",
          "article_title_uz": "Qanday qilib bank hisob raqam ochish",
          "article_image_link": "Qanday qilib bank hisob raqam ochish",
          "article_user": "Umidjon Juraqulov",
          "article_tags": "{maqola, Sog'liq}"
       }
}
```
</details>

--- 
