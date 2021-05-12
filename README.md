# lab09-lab4-group-11
lab09-lab4-group-11 created by GitHub Classroom

How many cards are drawn from the deck? What are the cards? 
How do you retrieve deck_id from the response? Write your code using JavaScript.
How do you print information about each card? Write your code using JavaScript.


Exercise 1

GET is one of the HTTP request methods. What is a GET method? Give an example of how you can use GET with the Deck Of Cards API.
* Its a way of requesting the API and using the functions. An example of how u can use it:  resp = requests.get('https://deckofcardsapi.com/api/deck/new/shuffle/?deck_count=1') in order to create a deck of cards

List all available features that you can use from Deck of Cards. For example, one of the APIs you can use is to shuffle cards.
* Shuffle, draw, reshuffle, get a new deck, get a partial deck, add to a pile, shuffle piles, list the cards in piles, draw from piles.

What is the API for getting a brand new deck that also includes two jokers?
* https://deckofcardsapi.com/api/deck/new/?jokers_enabled=true

Looking at the following example response from the Deck of Cards API (Links to an external site.).

* How many cards are drawn from the deck? What are the cards? 2 cards King of Hearts, 8 of Clubs

* How do you retrieve deck_id from the response? Write your code using JavaScript. 
  fetch("https://deckofcardsapi.com/api/deck/new/shuffle/?deck_count=1")
      .then(response => response.json())
      .then(data => {
          // handle the response
          deckID = data.deck_id;
          console.log(deckID);
      })
      
      var json_example = {
    "success": true,
    "cards": [
        {
            "image": "https://deckofcardsapi.com/static/img/KH.png",
            "value": "KING",
            "suit": "HEARTS",
            "code": "KH"
        },
        {
            "image": "https://deckofcardsapi.com/static/img/8C.png",
            "value": "8",
            "suit": "CLUBS",
            "code": "8C"
        }
    ],
    "deck_id":"3p40paa87x90",
    "remaining": 50
}

console.log(json_example.deck_id);

* How do you print information about each card? Write your code using JavaScript.
console.log(json_example.cards)
    
   
