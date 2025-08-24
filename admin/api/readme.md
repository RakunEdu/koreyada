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
<summary> 📌 GET /edit_user/ </summary>

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
<summary> 📌 GET /delete_user/ </summary>

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
<summary> 📌 GET /add_user/ </summary>

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
          "category_id": 1,
          "category_name_en": "Visa & Law" 
          "category_name_uz": "Viza & Qonun"
          "n_comments": 12  
        }
}
```
</details>



<details>
<summary> 📌 GET /edit_user/ </summary>

### Edit User Endpoint 

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
<summary> 📌 GET /add_category/ </summary>

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



--- 
### 5. Businesses Endpoints  

<details>
<summary> 📌 GET /businesses_list/ </summary>

### Businesses List Endpoint 

> Response (200): 
```json
{
   "1": {
          "business_id": 1,
          "category_name_en": "Visa & Law" 
          "category_name_uz": "Viza & Qonun"
          "n_comments": 12  
        }
}
```
</details>


