# Design a Deck of Cards

![a deck of cards](https://i.imgur.com/Upuy21L.jpg)

## Constraints and assumptions

* Is this a generic deck of cards for games like poker and black jack?
	* Yes, design a generic deck then extend it to black jack
* Can we assume the deck has 52 cards (2-10, Jack, Queen, King, Ace) and 4 suits?
	* Yes
* Can we assume inputs are valid or do we have to validate them?
	* Assume they're valid


## Code 

### Java

- Class Suit

``` java
Public enum Suit {
	SPADE,
	HEART,
	CLUB,
	DIAMOND
}
```

- Class Card 

```java
public class Card {
	int faceValue;
	Suit suite;
	
	public Card(int faceValue, Suit suite){
	this.faceValue = faceValue;
	this.suite = suite;
	}
}
```

- Class Deck 

``` java
public class Deck {
	List<Card> cardDeck;
	
	public Deck(){
		this.cardDeck = newArrayList<Card>();
		for (int value = 1; value <= 13; value++){
		for (Suit: suite: Suit.values()){
			cardDeck.add(new Card(value, suite));
			}
		}
	}
	
}
```

### Python 

[Design a deck of cards](https://github.com/donnemartin/system-design-primer/blob/master/solutions/object_oriented_design/deck_of_cards/deck_of_cards.ipynb)