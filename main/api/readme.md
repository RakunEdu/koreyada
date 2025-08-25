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

### Latest Articles Endpoint 
* Returns the latest posted articles 

> Response (200): 
```json
{
  "1": {  "article_id": 24
          "article_title_en": "How to open a bank account in Korea",
          "article_title_uz": "Qanday qilib bank hisob raqam ochish", 
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
  "1": {  "category_id": 1
          "category_name_en": "Visa",
          "category_name_uz": "Viza", 
          "category_description_en": "Visa applications, renewals, and immigration assistance",
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
          "article_title_en": "How to open a bank account in Korea",
          "article_title_uz": "Qanday qilib bank hisob raqam ochish", 
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
  "1": {  "business_id": 12
          "article_title_en": "How to open a bank account in Korea",
          "article_title_uz": "Qanday qilib bank hisob raqam ochish", 
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
  "1": {  "business_id": 12
          "article_title_en": "How to open a bank account in Korea",
          "article_title_uz": "Qanday qilib bank hisob raqam ochish", 
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
   "article_title_en": "How to open a bank account in Korea",
   "article_title_uz": "Qanday qilib bank hisob raqam ochish",

   "services": ["visa xizmatlari", "trajima"] 
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
   "news_id": 12, 
   "news_title_en": "How to open a bank account in Korea",
   "news_title_uz": "Qanday qilib bank hisob raqam ochish", 
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
   "news_title_en": "How to open a bank account in Korea",
   "news_title_uz": "Qanday qilib bank hisob raqam ochish", 
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
  "1": {  "category_id": 1
          "category_name_en": "Visa",
          "category_name_uz": "Viza", 
          "category_description_en": "Visa applications, renewals, and immigration assistance",
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
  "1": {  "category_id": 1
          "category_name_en": "Visa",
          "category_name_uz": "Viza", 
          "category_description_en": "Visa applications, renewals, and immigration assistance",
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
  "1": {  "category_id": 1
          "category_name_en": "Visa",
          "category_name_uz": "Viza", 
          "category_description_en": "Visa applications, renewals, and immigration assistance",
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
  "1": {  "category_id": 1
          "category_name_en": "Visa",
          "category_name_uz": "Viza", 
          "category_description_en": "Visa applications, renewals, and immigration assistance",
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
  "1": {  "category_id": 1
          "category_name_en": "Visa",
          "category_name_uz": "Viza", 
          "category_description_en": "Visa applications, renewals, and immigration assistance",
       }
}
```
</details>

--- 
