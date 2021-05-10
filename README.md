# PLAYCHEAPER API
---




## Why playcheaper?
playcheaper is a **free** public API with pricing steam games and deals.
Get access to discounts, pricing, game meta data like metacritic or screenshots. 

## What you are allowed to?
* Build competitive API
* Create commercial app
* Change data provided by playcheaper
* You don't have to provide link to playcheaper

## Rate limits
There is no monthly limit. You are allowed to make up to 3 requests per second.



# Endpoints
---
* ## Deals
  Endpoint for listing discounted games
  
* **URL**

  `http://playcheaper.com/api/v1/deals`

* **Method:**
  
  `GET`
  
*  **URL Params**

   **Optional:**
 
   `page=[int]`<br>
   `page_size=[int]   max value=50` <br>
   `discount=[int]`
   
* **Success Response:**
```json
"deals": [{
  "id":37,
  "link":"https://store.steampowered.com/app/40990",
  "title":"Mafia",
  "cover_url":"https://cdn.akamai.steamstatic.com/steam/apps/40990/header.jpg?t=1568743837",
  "discount":67,
  "price":494,
  "currency":"USD"
}]
```
*  **Examples**<br>
  `http://playcheaper.com/api/v1/deals`<br>
  `http://playcheaper.com/api/v1/deals?page=2`<br>
  `http://playcheaper.com/api/v1/deals?page=2&page_size=10`<br>
  `http://playcheaper.com/api/v1/deals?discount=60`
    * List all games where discount is higher or equal than 60

* ## Games
  Endpoint for listing all games
  
* **URL**

  `http://playcheaper.com/api/v1/games`

* **Method:**
  
  `GET`
  
*  **URL Params**

   **Optional:**
 
   `page=[int]`<br>
   `page_size=[int]   max value=50` <br>
   
* **Success Response:**
```json
"deals": [{
  "id":134,
  "link":"https://store.steampowered.com/app/257790",
  "title":"Riptide GP2",
  "cover_url":"https://cdn.akamai.steamstatic.com/steam/apps/257790/header.jpg?t=1447358948",
  "discount":0,
  "price":494,
  "currency":"USD"
}]

```
*  **Examples**<br>
  `http://playcheaper.com/api/v1/games?page=2`<br>
  `http://playcheaper.com/api/v1/games?page=2&page_size=10`<br>





