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
"games": [{
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
  
* ## Free games
  Endpoint for listing only free games
  
* **URL**

  `http://playcheaper.com/api/v1/games/free`

* **Method:**
  
  `GET`
  
*  **URL Params**

   **Optional:**
 
   `page=[int]`<br>
   `page_size=[int]   max value=50` <br>
   
* **Success Response:**
```json
"games": [{
  "id":3944,
  "link":"https://store.steampowered.com/app/608990",
  "is_free":true,
  "title":"The Archotek Project",
  "cover_url":"https://cdn.akamai.steamstatic.com/steam/apps/608990/header.jpg?t=1587933591"
}]

```
*  **Examples**<br>
  `http://playcheaper.com/api/v1/games/free?page=2`<br>
  `http://playcheaper.com/api/v1/games/free?page=2&page_size=10`<br>


* ## Game details
  Endpoint for getting more details about the game
  
* **URL**

  `http://playcheaper.com/api/v1/game/{id}`

* **Method:**
  
  `GET`
   
* **Success Response:**
```json
"games": [{
  "id":6,
  "link":"https://store.steampowered.com/app/550",
  "is_free":false,
  "title":"Left 4 Dead 2",
  "genres":[{"id":3,"name":"Action"}],
  "cover_url":"https://cdn.akamai.steamstatic.com/steam/apps/550/header.jpg?t=1601578341",
  "discount":80,
  "initial_price":999,
  "final_price":199,
  "currency":"USD",
  "desc":"Set in the zombie apocalypse, Left 4 Dead 2 (L4D2) is the highly anticipated sequel to the award-winning Left 4 Dead, the #1 co-op game of 2008. This co-operative action horror FPS takes you and your friends through the cities, swamps and cemeteries of the Deep South, from Savannah to New Orleans across five expansive campaigns."
 }]

```
*  **Examples**<br>
  `http://playcheaper.com/api/v1/game/6`
  


