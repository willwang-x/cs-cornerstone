# Blackjack

![blackjack](https://i.imgur.com/ElNFO9w.jpg)

## What 

source: [wiki](https://www.wikiwand.com/en/Blackjack)

Blackjack is the American variant of a globally popular banking game known as Twenty-One, whose relatives include Pontoon and Vingt-et-Un.[1] It is a comparing card game between usually several players and a dealer, where each player in turn competes against the dealer, but players do not play against each other. It is played with one or more decks of 52 cards, and is the most widely played casino banking game in the world.[2]:342 The objective of the game is to beat the dealer in one of the following ways:

* Get 21 points on the player's first two cards (called a "blackjack" or "natural"), without a dealer blackjack;
* Reach a final score higher than the dealer without exceeding 21; or
* Let the dealer draw additional cards until their hand exceeds 21 ("busted").


## How 

* Identifying the classes, 
* Identifying the classes’ responsibilities,
* identifying the collaborations


### a. Identifying the Blackjack Classes

Generally, a class is a noun, like people, place or things. One way is to find a noun by descripting the story. We don't have to be correct at first. We list them all and delete the unnecessary later. For exmaple, we got some basic classes for Blackjack:

- `GameRoom`：initialize the game
- `Gamer`: there are 2 kinds of gamer: player and dealer. There is a **Is-a** relationship between the two and the gamer. Thus, we can see the two as a subclass of gamer.
- `Card`: There is no blackjack without cards.
- `CardBox`: We need a deck of cards that palyers and dealers can take. For blackjack, there are 6 six deck of cards normally. Here, we make one decks of cards as a class.

### b.  Identifying the Classes' Responsibilities

- GameRoom:
	- Dealer * mDealer
	- list<Player*> mPlayList
	- JoinPlayer(Player*)
	- LeavePlayer(Player*)
	- OpenGameRoom()
- Gamer:
	- ID, Name, Money, Hands
	- Players: insurance 
	- Dealer: Cardbox 
	- makeDecision
	- caculate 
	- Dealer: start, reset, whoIsWinner
	- strategy
- Strategy
	- Gamer	 
		- int mID
		- string mName
		- list<Card> mHandCards
		- Strategy* mStrategy 
		- MakeDecision(Question)
		- CaculateHandScore() 
	- Player
		- mStrategy = new PlayStrategy()
		- double mBet 
		- double mDouble
		- double mInsurance
	- Dealer 
		- mStrategy = newDealerStrategy()
		- Cardbox mCardBox
		- int mGameState  
- Card
	- suit, value, isUp
- CardBox
	- Card 
		- int mType
		- int mValue
		- string mName
		- bool mFace
	- Deck  
		- list<Card> mCardList
		- initial()
	- CardBox
		- list<Card> mCardList
		- initial()
		- AppendDecks()
		- Shuffle()
		- PopCard()

### c. Identifying the Collaborations

Go through the game flow to see if we miss anything.

1. Dealer shuffles deck
1. Player makes bet
1. Dealer deals initial cards
1. Player adds cards to player's hand
1. Dealer adds cards to dealer's hand
1. Hand returns value of player's hand to player
1. Hand returns value of dealer's hand to dealer
1. Dealer asks player whether player wants another card
1. Dealer deals player another card
1. Player adds the card to player's hand
1. Hand returns value of player's hand to player
1. Dealer asks player whether player wants another card
1. Dealer gets the value of the player's hand
1. Dealer sends or requests bet value from players
1. Player adds to/subtracts from player's bet attribute  

### d. Further optimization 

- add a attribute to add history (cards and strategy)

![](https://i.imgur.com/UW608lF.png)