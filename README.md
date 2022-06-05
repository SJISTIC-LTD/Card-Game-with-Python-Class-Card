# Card-Game-with-Python-Class-Card
 I’ll walk you through how to make a card game with Python. In this card game, each player draws a card from the deck and the player with the highest card wins. I’m going to build this card game by defining classes representing a card, a deck, a player and finally the game itself.The first class in our card game with Python is a Card class, which has two class variables, suits and values. Suits is a tuple of strings representing all the suits a card can be: spades, hearts, diamonds, clubs. value is a tuple of strings representing the different numeric values a card can be: 2–10, Jack, Queen, King, and Ace.

The elements of the first two indexes of the value tuple are None, so the strings in the tuple match the index they represent. So the string “2” in the tuple of values is at index 2.Card objects have two instance variables: suit and value, each represented by an integer. Together, the instance variables represent the card type of the Card object. For example, you create a 2 of hearts by creating a Card object and passing it the parameters 2 (for color) and 1.

The code for these magic methods can also handle whether the cards have the same value, for example, if both cards have a value of 10. If this happens, the methods use the value of the combinations to break the tie.

The combinations are ranked in order of strength in the combination tuple – with the strongest combination last, and thus assigned to the highest index, and the less powerful combination to the lowest index.When you initialize the Deck object, the two for loops of __init__ create Card objects representing all the cards in a 52-card deck and add them to the card list. The first loop goes from 2 to 15 because the first value of a card is 2 and the last value of a card is 14 (the ace).

Each time around the inner loop, a new card is created using the integer from the outer loop as the value (i.e. 14 for an ace) and the integer from the inner loop as the suit. This process creates 52 cards – one card for each combination of suit and value.

After the method creates the cards, the shuffle method of the shuffle module randomly rearranges the items in the card list; imitating the shuffle of a deck of cards.

Our deck has another method called rm_card which removes and returns a card from the card list, or returns None if it is empty.
