# Rust Card Deck Library

This Rust library provides types and functions for working with a standard deck of playing cards. It includes definitions for `Suit`, `Value`, `Card`, and `Deck` types, along with various methods for interacting with decks.

## Installation

```sh
cargo add small-card-deck
```

## Usage

```rust
use small-card-deck::{Deck, Suit, Value};

fn main() {
    // Create a new deck
    let mut deck = Deck::new();

    // Shuffle the deck
    deck.shuffle();

    // Peek at the top card
    if let Some(top_card) = deck.peek() {
        println!("Top card: {}", top_card);
    } else {
        println!("The deck is empty!");
    }
}
```

Types
Suit

Represents the suit of a playing card.
Variants:

    Hearts
    Diamonds
    Clubs
    Spades

Value

Represents the value of a playing card.
Variants:

    Ace
    Two
    Three
    Four
    Five
    Six
    Seven
    Eight
    Nine
    Ten
    Jack
    Queen
    King

Card

Represents a single playing card, consisting of a suit and a value.
Methods:

    new(suit: Suit, value: Value) -> Self: Creates a new Card instance.
    to_string() -> String: Converts the card to a string representation.

Deck

Represents a deck of playing cards.
Methods:

    new() -> Self: Creates a new Deck instance with a standard 52-card deck.
    shuffle(): Shuffles the cards in the deck.
    peek() -> Option<&Card>: Returns a reference to the top card of the deck.
